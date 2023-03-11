---
layout: post
title: "Practical cryptography"
date: "2022-07-19 18:00:00 +0000"
author: Miles Berry
permalink: /2022/7/practical-cryptography/
comments: true
image:
        feature: 220719.JPG
---

## Cryptography and the school curriculum

Cryptography (encoding information so that it can be stored or communicated in secret) lies at the foundation of much of cybersecurity - digital identity, privacy and security all draw directly on the science of secrecy. It's also a great cross-curricular topic in school, making links between computing, languages, mathematics and ethics or PHSE. Back in my school teaching days I'd cover this over a couple of weeks of maths lessons, and I included this as a half-term unit in Switched On Computing. 

I think it's implicit in the secondary computing curriculum: at Key Stage 3, pupils should be taught to:

> Understand a range of ways to use technology safely, respectfully, responsibly and securely, including protecting their online identity and privacy.

And at Key Stage 4 all pupils (not just those taking GCSE Computer Science) should be taught to:

> Understand how changes in technology affect safety, including new ways to protect their online privacy and identity.

It's not clear what these 'new ways' are, but I'd want to discuss VPNs, TOR, man in the middle attacks for SSL and end-to-end encryption here, amongst much else.  

Cryptography does make it onto the specification for A Level computer science, with mentions of the Caesar and Vernam (one time pad) ciphers, as well as a non-technical grasp of public / private key cryptography. There are useful teaching materials for all this from [Isaac CS](https://isaaccomputerscience.org/topics/encryption?examBoard=all&stage=all).

These topics are typically covered in theory lessons, or perhaps using 'unplugged' demonstrations away from computers. However, I think much is gained through demonstrating different cryptography techniques using programming as a medium - this gives students the chance to experiment with encryption themselves, and provides a motivating, practical context for reinforcing many of the programming constructs and techniques that students have studied.

A practical, programming-based unit on cryptography could comfortably fit in towards the end of Key Stage 3, where there's a good chance to make the cross-curricular connections which really bring something like this to life. If it were me, I'd take a chronological approach, from simple ciphers that can be cracked by hand, through to more complex approaches which draw more deeply on pupils' mathematical and linguistic understanding.

## The Caesar Cipher

I'd start with the Caesar cipher, in which each character of the plain text is shifted along the alphabet a certain number of places. Thus, with a shift of 1, 'hello' becomes 'IFMMP'. I think it's reasonable enough to set pupils the challenge of implementing this as code themselves, perhaps with some hints or jumbled up lines of code ([Parsons's Problems](https://www.researchgate.net/profile/Patricia-Haden/publication/262160581_Parson's_programming_puzzles_A_fun_and_effective_learning_tool_for_first_programming_courses/links/5593212508ae5af2b0eb6da3/Parsons-programming-puzzles-A-fun-and-effective-learning-tool-for-first-programming-courses.pdf)) for those who might need more scaffolding. If I were live-coding this in front of a class (and [there's much to be said for this](https://dl.acm.org/doi/pdf/10.1145/2445196.2445388)), I'd start by writing a function to shift just one character a certain number of places:

```python
def shift1(c, k):
    pos = ALPHABET.find(c)
    if pos != -1:
        return ALPHABET[(pos + k) % 26]
    else:
        return c
```

Then I can build up the function I actually want through a list comprehension:

```python
def shift(plain, k):
    return ''.join([shift1(c, k) for c in plain])
```

I think it adds much interest to have pupils learn about cracking ciphers as well as using them, linking to Bletchley Park, Turing and the birth of computing. A brute force approach works well enough for the Caesar cipher, as there are only 26 possible keys - the number of places the cipher shifts the plain text.  

## Substitution Ciphers

By Tudor times cryptography had moved from such an easy to crack cipher. By then substitution ciphers were used, in which each letter of the plain text alphabet was swapped for another character, without any discernible pattern. Brute force attacks would not work here, as the key space is huge: 26 x 25 x 24 x ... x 2 x 1. However, the properties of the English language give much away - common letters in English are E, T, A and I (helpful for Wordle...), and common words might include the, of, and, a and to - if the same plain text letters are always swapped for the same cipher text letters, this gives an easy way in to cracking the code used.  

As well as implementing a substitution cipher as a function, pupils could write a function to count up how many times each character occurs in a cipher text. As well as list comprehensions, Python offers a dictionary comprehension, which is well suited for a task like this:

```python
def freq_table(plain):
    return {c:plain.count(c) for c in ALPHABET.upper()}
```
Asking pupils to decrypt passages from familiar books encrypted using a random substitution cipher is both engaging and accessible.

## Polyalphabetic Ciphers

The use of the wired and particularly wireless telegraphy from Victorian times on increased the need for cryptography, just as the Internet has done more recently. The vulnerability of substitution ciphers to frequency analysis led to the use of polyalphabetic ciphers, in which a series of Caesar shift (or more complex) ciphers would be used in some pre-determined order - perhaps using the letters of a key word, or a known passage of text, or some mechanical process (as in the German Enigma and British Typex machines), or even a unique sequence of random numbers (as in the theoretically uncrackable one time pad or Vernam cipher). In class, we could introduce pupils to a pseudo Vernam cipher using Python's own random number function combined with the Caesar shift cipher from above:

```python
def vernam(plain, key):
    seed(key)
    return ''.join([shift1(c, randint(0, 25)) for c in plain])
```

This provides a great starting point for a discussion of how Python's pseudorandom number generator might work, and whether a true one time pad could ever be created using a computer.

## Pubic / private key cryptography

Whilst the one time pad guarantees security, it's impractical for most purposes as a unique key as long as any message has to be exchanged in advance, and cannot be reused without compromising security: if there's a secure channel for exchanging such a key, then why not use it for exchanging the message itself?

The Internet's cryptographic infrastructure rests instead on ciphers with *two* keys, typically introduced as a public key for encryption, and a private key for decryption. The maths here is non-trivial and beyond what gets covered in school. However, we can introduce some of the foundational ideas by having pupils explore prime factorisation for themselves - given a couple of prime numbers, it's easy to multiply them together, but given a product of two large primes, it's hard to recover the factors: 709 x 919 is easy, but finding two numbers whose product is 641,889 is much harder. 

I'd start by asking pupils to write a function that finds all the factors of a number, such as this:

```python
def factors(n):
    return [f for f in range(1, n + 1) if n % f == 0]
```

Pupils could use this to write a function that checks if a number is prime, i.e. has exactly two factors:

```python
def is_prime(p):
    return len(factors(p)) == 2
```

We can then get the prime factors of a number by just filtering the list of factors:

```python
def prime_factors(n):
    return [p for p in factors(n) if is_prime(p)]
```

I should admit that this isn't a particularly efficient method, which suggests a nice extension task to refactor these functions. 

There's a rather nice toy implementation of prime number based encryption [here](https://stackoverflow.com/questions/8539441/private-public-encryption-in-python-with-standard-library/8539470#8539470), but I'd be reluctant to use this with all but the most curious pupils at school.

## Further resources

I've uploaded [a Jupyter notebook](https://colab.research.google.com/drive/1rl4MretvZDVJi1ZbfhAOl944oHotX9pw?usp=sharing) with some example programs for the above systems. NCSC's [Cyber First Girls](https://www.ncsc.gov.uk/cyberfirst/girls-competition) is an excellent competition, and uses GCHQ's own [Cyber Chef](https://gchq.github.io/CyberChef/) tool, to bypass the heavy lifting of having to program. I'd also recommend [Simon Singh's The Code Book](https://www.amazon.co.uk/Code-Book-Secret-History-Code-breaking/dp/1857028899/ref=pd_lpo_1?pd_rd_i=1857028899&psc=1) to give a not too technical treatment of some of the history of cryptography, and [resources from CIMT](https://www.cimt.org.uk/resources/codes/). Do consider organising a trip to [Bletchley Park](https://bletchleypark.org.uk/) or [The National Museum of Computing](https://www.tnmoc.org/) (located at BP), and [The Imitation Game](https://en.wikipedia.org/wiki/The_Imitation_Game) is an enjoyable watch, even if not *entirely* accurate.  


*Based on [a lightning talk](https://colab.research.google.com/drive/1rl4MretvZDVJi1ZbfhAOl944oHotX9pw?usp=sharing) I gave at Cyber Education 2022, University of Roehampton*