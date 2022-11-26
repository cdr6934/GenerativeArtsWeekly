---
title: #006 Generative Arts Weekly 
description: 
image: 
tags: generative, art
---
# #006 Generative Arts Weekly

# Cloud Fractals, Blooms and Spinning Parametrics

> "The greatest value of a picture is when it forces us to notice what we never expected to see." -John Tukey
> 

Hello friends, 

I hope that you all have had another amazing week being creative. 

A bunch of you have left feedback that you want to see more code; and so I have added a section called "Snippet of the Week" in which I will highlight shorter pieces of code that inspire me to further play with it and mutate it to being something else. 

$x=u(sin(v)cos(u))$

 I have spent much of my free time reading, playing with new codebases to find more intuition and various ways to express beauty through art. 

You will find a number of articles using different frameworks that will help you find the right tool to express oneself. May it be through Go Lang, R, or Rust. 

There is always a language for you. 

That being said, it is a wonderful time we live in that provides the tools of expression making it accessible to any developer in the language of their choice. 

Happy Creating!

Chris 

# Snippet of the Week

The following was written in Processing and is a set of parametric equations spinning in 3D space. All of the equations are coming out of the book [Morphing](https://amzn.to/2IKO1H2). I've also started a [little repo on Github](https://github.com/cdr6934/Morph-processing) that I'll be contributing to and slowly build into a library of shapes to use for inspiration and boiler for future projects.  

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3686f6c9-4131-4452-9460-edffb0748566/Screen_Capture_-_Nov_21__8_20_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3686f6c9-4131-4452-9460-edffb0748566/Screen_Capture_-_Nov_21__8_20_AM.png)

```java
float x, y, z, s, iter, deg_x, deg_y; 

void setup()
{
  size(1000,1000, P3D); 
  background(255); 
  iter = 0.02;
  deg_x = 1.25; 
  deg_y = 1.25;
  s = 50; 
  smooth(8);
  noFill(); 
}

void draw() {
    background(255);
  for(float u = 0; u < 12*PI; u += iter) 
  {
    for(float v = (2*PI)/3; v < PI; v += iter) 
    {
      pushMatrix(); 
      translate(height/2, width/2); 
      rotateX(deg_x); 
      rotateY(deg_y); 
      x = v*((-3/2)*cos(3*u)+cos(1-u)); 
      y = v*(sin((3/2)*sin(3*u)+cos(1-u)/3)); 
      z = u/4; 
      //stroke(0,z*30); 
      point(x*s,y*s,z*s); 
      popMatrix(); 
    }
  }
  deg_x += iter; 
  deg_y += iter/2; 
 // stop(); 
} 
```

# Inspirations

---

**Caleb Ogg**

I've been a fan of Caleb's work for a while now. He has a muted palette of colors that he uses and will generally always plots the works that he has done.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0d0c9eb8-42b1-4f7d-a447-8fa9829e1773/2246585074061406790_2246585070856754005.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0d0c9eb8-42b1-4f7d-a447-8fa9829e1773/2246585074061406790_2246585070856754005.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f6adf3ef-5b08-4bf0-9057-865e75178160/2278484027551519239_2278484024045226123.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f6adf3ef-5b08-4bf0-9057-865e75178160/2278484027551519239_2278484024045226123.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c03c51aa-2d13-48c9-90df-e378d4710f38/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c03c51aa-2d13-48c9-90df-e378d4710f38/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2cf2083-b44c-4dc2-9f37-ede04faab83b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2cf2083-b44c-4dc2-9f37-ede04faab83b/Untitled.png)

[Instagram](https://www.instagram.com/iso.hedron/?hl=en)

[Twitter](https://twitter.com/caleb_ogg)

# 🖌️ Unconventional Media

[https://youtu.be/B5p2A5mazEs](https://youtu.be/B5p2A5mazEs)

> John Edmark's sculptures are both mesmerizing and mathematical. Using meticulously crafted platforms, patterns, and layers, Edmark's art explores the seemingly magical properties that are present in spiral geometries. In his most recent body of work, Edmark creates a series of animating “blooms” that endlessly unfold and animate as they spin beneath a strobe light.
> 

# 📸 Generative Graphics

[https://www.youtube.com/watch?v=1dPFgWT2Aio&t=93s](https://www.youtube.com/watch?v=1dPFgWT2Aio&t=93s)

## [Processing art tutorial Ep.2 | GRID 02](https://youtu.be/1dPFgWT2Aio)

> This video is part of the "How to draw with code" series. The Processing art tutorial uses for loops, arcs and stroke weight.
> 

# 🏛️ Exhibits / Installations

[https://vimeo.com/shuanghuo/stock](https://vimeo.com/shuanghuo/stock)

## Stock Exchange

> “Stock Exchange” is an artistic installation, which was commissioned by DIP INC, to setup in its art fund launch event in UCCA (Ullens Center for Contemporary Art) in Beijing. All three LED screens displayed the visual works purely generated by computer programs. Although the visual patterns are pre-set, the variations of the movement of the elements are randomly produced and will never be repeated. This piece represents the unpredictability of the ever-changing stock market and the excitement brought by it.
> 

# 🚤 Motion

[https://twitter.com/MacTuitui/status/1329815764312887296?s=20](https://twitter.com/MacTuitui/status/1329815764312887296?s=20)

Definitely check out @MacTuitui 

[https://twitter.com/SnowEsamosc/status/1329789122244878341?s=20](https://twitter.com/SnowEsamosc/status/1329789122244878341?s=20)

# 🎨 Functional Art

The following section I've added as I think it is really important to highlight that asethetic and functional can below in the same household. So moving forward you will see inspirations within the world of data vis and the like find its way into the following section. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13f708f6-c5a2-4cb9-b17f-29d32366e920/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13f708f6-c5a2-4cb9-b17f-29d32366e920/Untitled.png)

## [This burgeoning community helps people build stunning data visualizations](https://www.fastcompany.com/90578119/observable-data-visualization)

> Creating sophisticated data visualizations may not be for everyone, but a startup called Observable is trying to make the process a bit less impenetrable.

Observable provides a free website for creating complex graphs, charts, and other visual representations of data, such as face mask adoption in the United States or an Electoral College decision tree for the U.S. Presidential Election. While it requires some coding knowledge to use, it also lets anyone take an existing visualization and modify it for their own purposes, either by changing the visuals or plugging in their own data. That means people can start learning the ropes just by playing around with what’s already been made, and even the coding part scares you off, you can still visit Observable’s website to absorb its impressive graphics.
> 

From the creator of the javascript library [D3](https://d3js.org/), Observable is a l[ive coding platform](https://observablehq.com/) with the mindset of data analysis within a document called a notebook. I've found it a great way to practice working with Javascript libraries to tell a data story and giving the user the ability to work with the data in order to better understand. 

# 🔖 Articles and Tutorials

![https://ehmatthes.com/my_images/julia_plot_pil-4000-maxiter-500-cropped.png](https://ehmatthes.com/my_images/julia_plot_pil-4000-maxiter-500-cropped.png)

## Exploring fractals on a cloud computer

> I've always been curious about fractals, and the book  I'm reading uses fractals in an example. I started playing with the example, and found it a good chance to see how much faster a powerful cloud computer can render a fractal than a modest laptop.
> 

## [P5 (Processing) in Golang](https://github.com/go-p5/p5)

> p5 is a simple package that provides primitives resembling the ones exposed by the p5/processing library.
> 

Just to show the simplicity of the package; it will be more similar to OpenFrameworks and Nannou in terms of speed. However beware, this is an early stage piece. It has much work but it does appear in active development. Give them a shout out if you want to further support and help in the further development of the package. 

```go
package main

import (
	"github.com/go-p5/p5"
	"image/color"
	"math/rand"
)

func main() {
	p5.Run(setup, draw)
	
}

func setup() {
	p5.Canvas(1000,1000)
	p5.Background(color.Gray{Y: 220})

}
func draw() {
	p5.StrokeWidth(2)
	p5.Fill(color.Gray{Y: 110})
	p5.Ellipse(rand.Float64()*1000,rand.Float64()*1000,80,80)
}

```

The above code displays what a basic circle randomly jumping across the screen.  So it doesn't do anything but it provides an idea of what it can do. 

[https://www.youtube.com/watch?v=d9lsT4kJo44&feature=youtu.be](https://www.youtube.com/watch?v=d9lsT4kJo44&feature=youtu.be)

> Tutorial covering the Rust programming language and the the Nannou creative coding framework. We re-create the Mystify screensaver that appeared in Windows 3.1.
> 

Nannou is a newer creative coding framework written in Rust.   

[https://www.youtube.com/watch?v=LR5f3-5vB_U](https://www.youtube.com/watch?v=LR5f3-5vB_U)

## Animating with AI

> In this video, I use the AI systems Ganbreeder and GANtools to create psychedelic morphing animations. A generative adversarial network (GAN) is a class of machine learning systems
> 

![https://miro.medium.com/max/414/0*YeLJmbLfm-8KYlQ9.png](https://miro.medium.com/max/414/0*YeLJmbLfm-8KYlQ9.png)

## [Getting Started with Generative Art in R](https://medium.com/@vitgabrhel/getting-started-with-generative-art-in-r-3bc50067d34b)

> Generative art represents the involvement of a human-independent system (such as an algorithm) in a creative process. Such a system is a key element within the creative process, including its outputs .Unsurprisingly, there are many “tools” you can use if you want to delve into generative art. In case you want to have “hands-on” experience in R, there are two basic directions you can go.
> 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9f54e5d8-03d5-4d00-ba7b-e0c56df43691/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9f54e5d8-03d5-4d00-ba7b-e0c56df43691/Untitled.png)

## [Disc Transport](https://observablehq.com/@fil/disc-transport)

> A technique borrowed from Optimal Transport (OT) can help to compute force layouts much faster (and with less parameter tweaking) than the traditional multi-body repulsive approach.
> 

In order to find novel ways to create generative algorithms; one  useful skillset is to read through algorithms and then re-implement in one's own systems. Above is an example of using an algorithm to implement a more efficient repulsion system.

---

# Courses

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/51147e9b-1dbc-451b-8a23-f7be4c4f6f69/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/51147e9b-1dbc-451b-8a23-f7be4c4f6f69/Untitled.png)

## [Advanced Creative Coding with WebGL & Shaders](https://frontendmasters.com/courses/webgl-shaders/)

> Go deeper into creative coding and 3D graphics programming using WebGL, ThreeJS, and GLSL. In this course, you'll learn 3D vectors and shader effects. The skills you'll learn apply to many fields, including AR/VR, game development, interactive installations, media art, and more.
> 

# Books

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ec987d64-8bb7-4c22-b2ac-fa60ae0f2e03/https___bucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com_public_images_4066d867-97c1-476a-8f85-9978f5c6dd4f_701x593.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ec987d64-8bb7-4c22-b2ac-fa60ae0f2e03/https___bucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com_public_images_4066d867-97c1-476a-8f85-9978f5c6dd4f_701x593.png)

Earlier this week, I had put together a l[ist of generative art books](https://www.notion.so/688744517e8643f99b26afb1f9e49400)  in a format in which I continue to add new books as I come across them. So check them out regularly!

# Send me your inspirations...