> "If little else, the brain is an educational toy." - Tom Robbins
> 

Well, there is about 6 hours worth of learnable content that I've attached this week. Most of it I've been able to race through. 

## Tyler Hobbs Interview

Being the first interview I've done this way. I am a little overwhelmed and self conscience but I decided that the beauty of generative is that sometimes the mistakes are just part of the output and should be kept. I thoroughly enjoyed the conversation that we had as we talked through the following questions... 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/616f10b0-301d-40f3-a555-568e8b952ef5/voronoi.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/616f10b0-301d-40f3-a555-568e8b952ef5/voronoi.png)

# Programming Library: [Mesh](http://leebyron.com/mesh/#newdelaunay)

> Mesh is a library for creating Voronoi, Delaunay and Convex Hull diagrams in Processing. After searching online for a Java package for creating Voronoi diagrams and failing to find anything simple enough to fit my needs I decided to make my own as simple as possible. I did find the wonderfully useful QuickHull3D package, which the algorithms for creating these diagrams are based on. These complete in O(n log n) time.
> 

If you haven't been able to figure out how to use the library, heres a little template code that will help you further step into using the power of other algorithms to take your work to another level. If you do, let me know and send me your work so that 

```java
/*
Programing: Wiggling Voronoi 
 Name: Chris Ried
*/

Voronoi myVoronoi; 
int cnt = 100; 
float[][] points = new float[cnt][2];
float[][] myEdges;
MPolygon[] myRegions; 
void setup() 
{
  background(255); 
  strokeWeight(.5); 
 size(1000,1000);  
 for(int x = 0; x < cnt; x++)
 {
   for(int y = 0; y < 2; y++)
   {
     points[x][y] = random(0,width); 
   }
 }
}

void draw() {
 background(255); 
 Voronoi myVoronoi = new Voronoi( points );
 myRegions = myVoronoi.getRegions();

for(int i=0; i<myRegions.length; i++)
{
// fill(getColor());
  myRegions[i].draw(this); // draw this shape
}

 for(int x = 0; x < cnt; x++)
 {
   for(int y = 0; y < 2; y++)
   {
     points[x][y] += random(-3,3); 
   }
 }

//stop(); 
}

void saveImage() {
  int seed = 100; 
  String timestamp = year() + nf(month(), 2) + nf(day(), 2) + "-"  + nf(hour(), 2) + nf(minute(), 2) + nf(second(), 2); 
  saveFrame(timestamp+"-"+seed+".png");
}

// Color Functions 
int colors[] = {#FFB401, #072457, #EF4C02, #ADC7C8, #FE6567};

int rcol() {
  return colors[int(random(colors.length))];
}

int getColor() {
  return getColor(random(colors.length));
}

int getColor(float v) {
  v = abs(v); 
  v = v%(colors.length); 
  int c1 = colors[int(v%colors.length)]; 
  int c2 = colors[int((v+1)%colors.length)]; 
  return lerpColor(c1, c2, pow(v%1, 0.1));
} 

```

## Genuary 2021: A Week After...

Its fun to see some of the pieces after January is already over; so I decided to just display a few more from the entire month of Genuary for your enjoyment. These are all beautiful in their own right and I do look forward to next year. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56e373a3-ad08-4e17-84a3-63a8f285df4e/canvas.51_1609770914_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56e373a3-ad08-4e17-84a3-63a8f285df4e/canvas.51_1609770914_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0b652c4d-5638-49d5-b309-b92096a6d0be/gengeomergence_1609798785_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0b652c4d-5638-49d5-b309-b92096a6d0be/gengeomergence_1609798785_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8c5c2884-afb8-49d8-9dca-776be71e0244/ruuddotorg_1612110296_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8c5c2884-afb8-49d8-9dca-776be71e0244/ruuddotorg_1612110296_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9033a646-4abb-42a1-8320-c2fc57a17587/juhani.haikomaki.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9033a646-4abb-42a1-8320-c2fc57a17587/juhani.haikomaki.png)

**Source**: [canvas.51](https://www.instagram.com/canvas.51/), [juhani.halkomaki,](https://www.instagram.com/juhani.halkomaki/) [ruuddotorg](https://www.instagram.com/ruuddotorg/), [gengeomergence](https://www.instagram.com/gengeomergence/) 

# Inspirations

---

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b302890c-6a35-4dc2-8eda-7eb982302a69/Screen_Capture_-_Feb_13__7_59_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b302890c-6a35-4dc2-8eda-7eb982302a69/Screen_Capture_-_Feb_13__7_59_AM.png)

# [Creativity Driven by R&D](https://www.youtube.com/watch?v=MJULayyg4sU&feature=emb_title)

> In this lecture, artist and creative technologist Raven Kwok talks about his workflow, that is, starting a feasibility study on one subject, exploring its possibilities in various directions, then pushing up complexity to get the final results.
> 

Raven Kwok, I have found much of his work inspiring and this video doesn't let you down in terms of how intricate his work is. I would highly recommend taking the time to watch the hour lecture (use the link, as the embed doesn't work otherwise)  

![https://live.staticflickr.com/65535/49844292783_3e99244e09_z.jpg](https://live.staticflickr.com/65535/49844292783_3e99244e09_z.jpg)

![http://farm4.staticflickr.com/3726/12122488093_f6ab9b69ea_z.jpg](http://farm4.staticflickr.com/3726/12122488093_f6ab9b69ea_z.jpg)

 

![https://live.staticflickr.com/65535/49022566252_5277601d14_z.jpg](https://live.staticflickr.com/65535/49022566252_5277601d14_z.jpg)

[Twitter](https://twitter.com/RavenKwok) / [Website](https://ravenkwok.com/) 

# 🏛️ Exhibits / Installations

## Exploring generative spaces: a quickstart to generative art - GitHub Universe 2020

[https://www.youtube.com/watch?v=meqHPIOzk-U](https://www.youtube.com/watch?v=meqHPIOzk-U)

> In this talk, Sabine "bleeptrack" Wieluch will give a quick introduction on how to create your own generative art using paper.js. She'll also share insights to common techniques and explain possible pitfalls. She's excited to code art with you!
> 

It is really nice to see the many different artists in the generative space. Sabine takes an interesting maker approach to her generative installations which are always so fascinating to watch and learn. Plotters of course are one step toward this, but then when you get into CNC routers, it becomes another level of materials and technical skills which I admire. (Protip: If you haven't checked out [Nervous](https://www.instagram.com/nervous.system/) instagram or their [website](https://n-e-r-v-o-u-s.com/shop/) please do! ) 

# 🔖 Articles and Tutorials

[https://www.youtube.com/watch?v=O3gLBhC353Y](https://www.youtube.com/watch?v=O3gLBhC353Y)

## [Blender Procedural Nodes](https://www.youtube.com/watch?v=O3gLBhC353Y)

A 2 Hour tutorial on using [Blender](https://www.blender.org/) (An open source 3D animation workflow tool) and diving into the interesting task of Procedural Nodes. Procedural Nodes are similar to software  such as [Touch-Designer](https://derivative.ca/), or [vvvv](https://vvvv.org/). You will find that this is a great starting point if you want to take a pass on using a 3D software (open source) to create materials that are generative. 

If you want to get a sense of what Blender is capable to do, please check out their latest short film. I'm always extremely impressed that there is such a big community that is willing to put something this incredible together. 

[https://www.youtube.com/watch?v=4YA9LSBLOB0](https://www.youtube.com/watch?v=4YA9LSBLOB0)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41b737ad-8709-47d0-a442-30f20c6cd45e/self_organizing_textures.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41b737ad-8709-47d0-a442-30f20c6cd45e/self_organizing_textures.png)

## [Self Organizing Textures](https://distill.pub/selforg/2021/textures/)

> Neural Cellular Automata (NCA 1 ) are capable of learning a diverse set of behaviours: from generating stable, regenerating, static images, to segmenting images, to learning to “self-classify” shapes. The inductive bias imposed by using cellular automata is powerful. A system of individual agents running the same learned local rule can solve surprisingly complex tasks. Moreover, individual agents, or cells, can learn to coordinate their behavior even when separated by large distances. By construction, they solve these tasks in a massively parallel and inherently degenerate 2 way. Each cell must be able to take on the role of any other cell - as a result they tend to generalize well to unseen situations.
> 

I found the article quite intriguing for a few reasons. One it takes patterns and generates interesting interpolations of them when interacting with them. Also it takes these patterns and uses deep learning to generate an iterative creating new results that you just don't see in most work. It's a lengthy read, but it is work at least working through the examples at the top of the page. 

# **Courses**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/92eb6f4b-f2c6-4796-9802-43ebe0033980/Screen_Capture_-_Feb_13__9_31_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/92eb6f4b-f2c6-4796-9802-43ebe0033980/Screen_Capture_-_Feb_13__9_31_AM.png)

## [Kinetic Typography Animation in After Effects](https://skl.sh/3amcNsd)

> On this 90 minutes course you will learn how to create some kinetic typography animation in After Effects. After I show you some Fonts, We will start with some simple effects, like stretching effects, echo and scale wipe.
Then we will learn some distortion effects, 3D perspective and create a grid text, as a base for the other animations. We will explore some effects that will help you create more than 20 variations of kinetic typography animation.
Finally you will learn how to mask an object and create a gradient animation.
> 

Generally, I am not really into using more static tools when generating the motion pieces that I've created. However I have been seeing some really neat typographical pieces lately on instagram and decided I wanted to see how it was being created. I came across the course and found it quite fascinating as I saw the variations and techniques that were used. In my process, one of the ways I've gained insight was to be able to create works static images in After Effects, Flash or Photoshop and then go through the same process of clicks in an application and translate them into Processing. 

# Books

![https://pup-assets.imgix.net/onix/images/9780691161730.jpg?w=640&auto=format](https://pup-assets.imgix.net/onix/images/9780691161730.jpg?w=640&auto=format)

# Creating Symmetry: The Artful Mathematics of Wallpaper Patterns

> This lavishly illustrated book provides a hands-on, step-by-step introduction to the intriguing mathematics of symmetry. Instead of breaking up patterns into blocks—a sort of potato-stamp method—Frank Farris offers a completely new waveform approach that enables you to create an endless variety of rosettes, friezes, and wallpaper patterns: dazzling art images where the beauty of nature meets the precision of mathematics.
> 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1058b617-57fd-470f-8f02-6dcd835d8381/patterns_1.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1058b617-57fd-470f-8f02-6dcd835d8381/patterns_1.png)

I just started reading the book but I have found it quite useful as it is full of beautiful patterns but then there is also the mathematics behind the patterns that are shown. These patterns then will find themselves in my work at some point for sure! 

# Send me your inspirations...