---
layout: post
title: "Python Image Manipulation"
date: "2021-03-26 17:40:56 +0000"
author: Miles Berry
permalink: /2021/03/python-image-manipulation/
comments: true
image:
        feature: 250321.jpg
---

I have fond memories of getting primary school pupils to explore the image filters in Photoshop substitutes such as [GIMP](https://www.gimp.org/) and [Pixlr](https://pixlr.com/), producing some Warhol-esque grids of portraits with different effects applied to each. Since them, image filters have become pretty much ubiquitous thanks to [Instagram](https://www.instagram.com/mgberry/?hl=en-gb) and the like, and so pupils' familiarity with the idea can now be taken (almost) for granted, but I wonder how many of them pause and think about what's happening behind the touchscreen? 

I was quite taken with Mark Guzdial's '[MediaComp](http://coweb.cc.gatech.edu/mediaComp-teach)' ideas as a way into programming for those who were inexplicably more interested in working with digital media than finding the sum of all the multiples of 3 or 5 less than 1000. 

I've subsequently used image manipulation in whole cohort lectures to our BA Primary Education students, demonstrating how digital images are represented as red, green and blue colour values, and using [GP](https://gpblocks.org/) as a block-based language to illustrate what happens when these values are changed.

![GP code to make a grey scale image](/images/scriptImage.png)

You can do a similar thing in Excel, using Andrew Taylor's rather brilliant [JPEG -> Excel converter](https://www.think-maths.co.uk/spreadsheet), as demosntrated by [Matt Parker](https://www.youtube.com/watch?v=UBX2QQHlQ_I). 

More recently, I've included similar exercices in Processing for our BA Digital Media students as part of their Software Studies module. There's more of a learning curve here, but this is quite an accessible project once you're used to Processing's way of doing things.

## Pillow Talk

In secondary schools, (almost) everyone is learning to code in Python, and almost everyone is learning how images are represented digitally as bitmap graphics. I think the former often gets taught through rather dull exercises which appear to involve doing things with integers and strings; the latter seems to involve colouring in on squared paper. I think there's a quick win here: give pupils a real understanding of how actual images are actually represented using red, green and blue colour values, and have them coding in Python to do something that they wouldn't have been able to do back in primary school using Scratch. 

From what I've seen, the simplest way into image manipulation in Python is using the [Pillow](https://pillow.readthedocs.io/en/stable/), the 'friendly' fork of the Python Image Libary (PIL). Rather than working in the (really quite unpleasant) IDLE, I'd recommend using a [Jupyter Notebook](https://jupyter.org/) for this, to encourage a *dialogic* style of programming: ask the interpreter to do something, then look at how it responds. Now ask it to do something else. You can install and run Jupyter on your own machine via the browser (or [Nteract](https://nteract.io/), or in [VSCode](https://code.visualstudio.com/docs/python/jupyter-support)), or just use the free, hosted [Colab version](https://colab.research.google.com/) of this from Google. If you'd like to follow though my examples, open [my Notebook](https://colab.research.google.com/drive/1apbnlrdj01zWs9TUJdHl45H9AJtRjbvh) in another browser window. 

Pillow comes with some image manipulation methods built in - it's easy enough to rotate an image:

```python
rotated_image = image.rotate(-12)
```

![rotated image](/images/rotated.png)

Or to resize and/or reshape the image, which would be useful for building a thumbnail gallery in a webapp.

```python
resized_image = image.resize((200, 200))
```

![resized image](/images/resized.png)

And to crop in on a particular part of the image:

```python
cropped_image = image.crop(box = (200, 150, 800, 550))
```

![cropped image](/images/cropped.png)

## Coding is the new Instagram

The fun starts though when you start playing with the `getpixel` and `putpixel` methods to start manipulating the red, green and blue values of each pixel. 

In all of the examples here, the pattern is pretty much the same: iterate over each pixel, determine it's current RGB value, change those according to some mathematical operation, and then set that as the new RGB pixel value. 


We might start by increasing the red, green and blue values of each pixel by the same amount, to make a brighter image:

```python
brightness = 1.2
for x in range(width):
  for y in range(height):
    oldpixel = image.getpixel((x, y))
    newpixel = (int(min(oldpixel[0] * brightness, 255)),
              int(min(oldpixel[1] * brightness, 255)),
              int(min(oldpixel[2] * brightness, 255))) 
    image2.putpixel((x, y), newpixel)
```

![brighter image](/images/brighter.png)

The colour balance can be changed - making a 'warmer' image involves increasing the red values whilst decreasing the blue:

```python
for x in range(width):
  for y in range(height):
    oldpixel = image.getpixel((x, y))
    newpixel = (int(min(oldpixel[0] * 1.1, 255)),
              oldpixel[1],
              int(oldpixel[2] * 0.9)) 
    image2.putpixel((x, y), newpixel)
```

![warmer image](/images/warmer.png)

You'll notice that in both of these examples, I'm doing a little extra maths to keep colour values constrained as whole numbers in the range 0 to 255. It might be more elegant to write a function to do that, but I'm inclined for an exercise like this to expose a bit more of the how the magic works. Abstraction has its place, but there are occasions when you want to show pupils what happens inside at least the first black box.

Some readers will be old enough to remember when photos were taken using chemicals on transparent plastic (no, really, I'm not making this up), and getting the origial, developed 'negative' as well as the printed photo. You can recreate this digitally by taking each of the colour values away from 255, although I'm not quite sure why you would want to.

```python
for x in range(width):
  for y in range(height):
    oldpixel = image.getpixel((x, y))
    newpixel = (255 - oldpixel[0],
              255 - oldpixel[1],
              255 - oldpixel[2]) 
    image2.putpixel((x, y), newpixel)
```

![negative image](/images/negative.png)

A similarly freaky effect can be achieved by swapping the data around between colour chanels. Here red becomes green, green becomes blue and blue becomes red. Again, I'm not sure that this will get you *lots* of likes on 'stagram. 

```python
for x in range(width):
  for y in range(height):
    oldpixel = image.getpixel((x, y))
    newpixel = (oldpixel[2], oldpixel[0], oldpixel[1]) 
    image2.putpixel((x, y), newpixel)
```

![channel swapping](/images/freaky.png)

A mirror image involves taking the pixels from the right hand side of the rows and putting them at the left hand side of the new rows, and vice versa. Whatch out for the potential for an off-by-one error here. A left-right inversion still looks like a cat. A top-bottom one just looks like an upside down cat. You'll have noticed that gravity works downwards. By definition. 

```python
for x in range(width):
  for y in range(height):
    newpixel = image.getpixel((width - x - 1, y))
    image2.putpixel((x, y), newpixel)
```

![mirror image](/images/mirror.png)

If the red, green and blue channels are all set to the same value, we get a grey-scale image. Here, I'm setting all three values to the mean of the red, green and blue values, but there are other ways to do this. I have a soft spot for moody black and white pictures...

```python
for x in range(width):
  for y in range(height):
    average = sum(image.getpixel((x, y))) // 3
    image2.putpixel((x, y), (average, average, average))
```

![grey scale](/images/grey.png)

We've reduced the colour depth from c 16 million colours here (24 bits) to just 256 shades of grey (8 bits). We can reduce it further still, to just one bit per pixel:

```python
threshold = 192
for x in range(width):
  for y in range(height):
    average = sum(image.getpixel((x, y))) // 3
    if average >= threshold:
      value = 255
    else:
      value = 0
    image2.putpixel((x, y), (value, value, value))
```

![black and white](/images/bandw.png)

Increasing or decreasing the saturation is a bit more complicated, but essentially this is about increasing or decreasing the difference between each of the channels and the average grey scale values. Again, the code is made a bit more complicated by the need to constrain values to integers in the 0 to 255 range. The eagle eyed will spot that I'm iterating across a mutable list of colour values at each pixel, but then casting the list as a required tuple for setting the pixels of the new image. 

```python
saturation = 1.5
newpixel = [0, 0, 0]
for x in range(width):
  for y in range(height):
    oldpixel = image.getpixel((x, y))
    average = sum(oldpixel) // 3
    for i in range(3):
      newpixel[i] = int(
          max(
              min((oldpixel[i] - average) * saturation + average, 
                  255),
              0))
    image2.putpixel((x, y), tuple(newpixel))
```

![increased saturation](/images/saturation.png)

One way of blurring the image is to replace the values of each pixel with the average of those in the box around them - in this case the 3x3 grid, but a bigger box gives a more blurry image.

```python
for x in range(1, width - 1):
  for y in range(1, height - 1):
    newpixel=[0, 0, 0]
    for dx in range(-1, 2):
      for dy in range(-1, 2):
        nearby=image.getpixel((x + dx, y + dy))
        for j in range(3):
          newpixel[j] = newpixel[j] + nearby[j]
    newpixel = tuple([x // 9 for x in newpixel])
    image2.putpixel((x, y),newpixel)
```

![blurred image](/images/boxblur.png)

## It's convoluted

Another way of doing this is through a *convolution* with a simple matrix. For each of the colour chanels, we multiply the values in the 3x3 box around our target pixel with the corresponding number in the 'kernel' matrix, adding together these products.

$$\frac{1}{9}\begin{bmatrix}
1 & 1 & 1\\
1 & 1 & 1\\
1 & 1 & 1\\
\end{bmatrix}$$

Whilst this is harder to explain (and moves us beyond Key Stage 3 maths, and possibly beyond what would normally be expected in Key Stage 3 computing), it's a more flexible approach with wider applications, as we'll see. 

In code, we first define the kernel matrix:

```python
kernel = [[1, 1, 1],
          [1, 1, 1],
          [1, 1, 1]]
```
and then we can write a function to scale the kernel down (forgive the list comprehension here) and do the convoluted product and sum:

```python
def convolve(kernel,image):
  weight = sum([sum(row) for row in kernel])
  if weight != 0:
    kernel = [[cell / weight for cell in row] for row in kernel]

  image2 = Image.new("RGB", (image.width, image.height))
  
  for x in range(1, width - 1):
    for y in range(1, height - 1):
      newpixel = [0, 0, 0]
      for dx in range(-1, 2):
        for dy in range(-1, 2):
          nearby = image.getpixel((x + dx, y + dy))
          for j in range(3):
            newpixel[j] = newpixel[j] + 
            nearby[j] * kernel[1 + dy][1 + dx]
      newpixel=tuple(map(int, newpixel))
      image2.putpixel((x, y), newpixel)
  
  return(image2)
  ```

With the above kernel, we just get another blurry cat, as we're still just taking an average of the nine pixels in the surrounding box, but this approach comes into its own when we change the kernel. For example, increasing the weighting of the middle pixel, whilst decreasing that of the ones around it, i.e. a kernel of

$$\begin{bmatrix}
-1 & -1 & -1\\
-1 & 9 & -1\\
-1 & -1 & -1\\
\end{bmatrix}$$

produces an impressive sharpening effect:

![sharp](/images/sharp.png)

But then reducing the weighting of the middle pixel by just one, so that it balances the edge pixels exactly, gives us an edge detection convolution.

$$\begin{bmatrix}
-1 & -1 & -1\\
-1 & 8 & -1\\
-1 & -1 & -1\\
\end{bmatrix}$$

![edges](/images/edges.png)

In the classroom, edge detection could be a nice example of the 'hiding complexity' approach to teaching abstraction, showing just the parts of the image where things change, so essentially the outline. It's also important in computer vision machine learning based on [convolution neural networks](https://en.wikipedia.org/wiki/Convolutional_neural_network). 

There's an interactive version of the code for all the above in [a Jupyter Notebook hosted on Google Colab](https://colab.research.google.com/drive/1apbnlrdj01zWs9TUJdHl45H9AJtRjbvh?usp=sharing). I'd encourage you to play around with the parameters, and do let me know if you try any of this out with your students. 