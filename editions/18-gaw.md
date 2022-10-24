[Website](https://www.generativecollective.com/) | [Patreon](https://www.patreon.com/generatecollective) | [Instagram](https://www.instagram.com/generate.collective/) | [Youtube](https://www.youtube.com/channel/UCBOYyqA-mqyoTSJ8pO9sQiA) | [Behance](https://www.behance.net/generatecoll) | [Twitter](https://twitter.com/generatecoll) | [BuyMeACoffee](https://www.buymeacoffee.com/generatecoll)

> "Creativity is not so much a boundless well, but an all-you-can-eat buffet of elements for your creative endeavor." - ***Vera Nazarian***
> 

**Exciting news!** 

It's been a little less than two weeks since I posted the [talk with Tyler](https://www.youtube.com/watch?v=pTesZREe73c) and we have just shy 700 views! That is WAY more than I had ever expected to see on a channel with one other video. But it comes to show how wonderful Tyler is respected in the community, and how much interest there is in the world of Generative Art has become in the last years. 

In the coming weeks, I will continue to line up more wonderful conversations for you all to enjoy so we can learn together and muse in our fascinations in the practice of generative mediums. The next couple interviews will be in the generative music space so do stay tuned. 

Also, if you have any interest to be featured, let me know. 

**Coding fun..**

This week I have been having fun deconstructing various simple shapes to come up with some blocks in a new system that I am working on. I decided that instead of writing to much, here is a little thing on playing around with arcs. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9baef125-9b44-468f-98f1-ef35982b6553/20210226-085440-100.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9baef125-9b44-468f-98f1-ef35982b6553/20210226-085440-100.png)

```java
/*
Programing: Explorations in the Arc Realm 
 Name: Chris Ried 
*/

ArcLine[][] al; 
float start_arc, stop_arc, r, diff, margin, x, y, nf;
float noise_factor; 
int n; 
void setup()
{
  size(1000,1000); 
  background(255);
  n = 1; 
  r = 2000; 
  noise_factor = 0.002; 
  diff = width / float(n); 
  margin = (diff) / 2; 
  al  = new ArcLine[n][n]; 
  for(int i = 0; i < n; i++)
  {
    for(int j = 0; j < n; j++)
    {
      x =  (i * diff)+margin; 
      y =  (j * diff)+margin; 
      nf = noise(x*noise_factor,y*noise_factor); 
      
     al[i][j] = new ArcLine(x,y+random(-5,5)*(x/width), r*nf);  
    }
  } 
}

void draw() {
  
    for(int i = 0; i < n; i++)
  {
    for(int j = 0; j < n; j++)
    {
       al[i][j].draw(); 
       al[i][j].update(); 
    }
  } 

} 

void saveImage() {
  int seed = 100; 
  String timestamp = year() + nf(month(), 2) + nf(day(), 2) + "-"  + nf(hour(), 2) + nf(minute(), 2) + nf(second(), 2); 
  saveFrame(timestamp+"-"+seed+".png");
}

class ArcLine {
 float x, y, r; 
 float start_arc, stop_arc; 
  color c;
  
   ArcLine(float _x, float _y, float _r) 
  {
    x = _x; 
    y = _y; 
    r = _r; 
    start_arc = random(TWO_PI); 
    stop_arc =  random(start_arc, TWO_PI); 
  }
  
  void draw() 
  {
      while(r > 0)
      {
        fill(color(int(random(255))); 
        stroke(0,200); 
        pushMatrix();
        translate(x,y); 
        rotate(random(TWO_PI)); 
        arc(0,0, r,r,start_arc,stop_arc); 
        popMatrix(); 
        r -= random(5);     
          start_arc = random(TWO_PI); 
        stop_arc =  random(start_arc, TWO_PI); 
    }
  } 
  
  void update() 
  { 
  } 
}

```

Also, I'll be [giving out the code](https://gum.co/GLHcB) for some of the work that I have done on my Instagram. 

# Inspirations

---

![https://themethod.in/wp-content/uploads/2020/06/Alida-Sun-Interview-Method-1-e1592628566459.jpeg](https://themethod.in/wp-content/uploads/2020/06/Alida-Sun-Interview-Method-1-e1592628566459.jpeg)

## **[Life on the Internet: From Nowhere and Everywhere](https://themethod.in/life-on-the-internet-from-nowhere-and-everywhere/)**

> in particular. Her art is much the same – ever changing, undefined, and all-encompassing. Alida gave Method a slight glimpse into her world of creation which involves many moving parts, quite literally. And for all hopeful new media artists, she gives direct and indirect advice, the foremost of which is that you don’t need a lot of expensive tech to make meaningful new media artwork.
> 

And here are a few of her works! 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/97972a9d-65e3-4a94-b00c-a59402a24292/alidasun_1610727900_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/97972a9d-65e3-4a94-b00c-a59402a24292/alidasun_1610727900_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e3f210c3-7ed8-45cc-8b29-cdff0349b79b/alidasun_1612803439.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e3f210c3-7ed8-45cc-8b29-cdff0349b79b/alidasun_1612803439.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4f4bf57c-582d-4a37-ba49-7c72ef3d558b/alidasun_1612888399_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4f4bf57c-582d-4a37-ba49-7c72ef3d558b/alidasun_1612888399_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f9fdac75-edb5-4306-b4d8-2656747e4082/alidasun_1613760513_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f9fdac75-edb5-4306-b4d8-2656747e4082/alidasun_1613760513_1.jpg)

[Instagram](https://www.instagram.com/alidasun/?utm_source=ig_embed) / [Twitter](https://twitter.com/alidasun) / [Patreon](https://www.patreon.com/alidasun) 

# Programming Packages

![https://d33wubrfki0l68.cloudfront.net/ad313c1b26a2a8f7dc4cff80b0a56cbaa7b2749e/cd3ce/images/score03.png](https://d33wubrfki0l68.cloudfront.net/ad313c1b26a2a8f7dc4cff80b0a56cbaa7b2749e/cd3ce/images/score03.png)

# [Alda](https://alda.io/tutorial/)

> Alda is a text-based programming language for music composition. It allows you to write and play back music using only a text editor and the command line.
> 

Speaking of generative music, take a look at the following DSL for music composition. Its a simple library to generate or compose some music.

 David demos his project Alda with Clojure to generate the music. 

[https://www.youtube.com/watch?v=6hUihVWdgW0&feature=emb_title](https://www.youtube.com/watch?v=6hUihVWdgW0&feature=emb_title)

# 📸 Generative Graphics

## Particle Series in Max / MSP

[https://www.youtube.com/watch?v=ZMxWdHKtF5A](https://www.youtube.com/watch?v=ZMxWdHKtF5A)

If you are a Max for Live user, [amazingmaxstuff](https://www.youtube.com/amazingmaxstuff) has a number of tutorials that will create motion graphics and sound materials very similar to TouchDesigner. It has been designed to be more for sound, you will find a number of tutorials and posts on his [instagram](https://www.instagram.com/amazingmaxstuff/) or [youtube](https://www.youtube.com/amazingmaxstuff) account. 

# 🏛️ Podcasts

[https://twitter.com/TANaudio/status/1365220756603478016/photo/1](https://twitter.com/TANaudio/status/1365220756603478016/photo/1)

## **[What are NFTs?](https://plinkhq.com/i/1280469178?to=page)**

> WTF are NFTs? We look at why crypto is dominating the art market right now. We hear from the artist @beepleand Jason Bailey, founder of @artnome
> 

# 🚤 Motion

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b524f7e6-dbf8-4f89-a7f2-868d433e798b/Screen_Capture_-_Feb_26__9_38_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b524f7e6-dbf8-4f89-a7f2-868d433e798b/Screen_Capture_-_Feb_26__9_38_PM.png)

## **[Introduction to Spark AR](https://www.gowaaa.com/post/best-thing-to-do-when-you-are-quarantined-at-home)**

> 2020 hasn’t been great for most of us, I truly wish that everything will go back to normal as soon as possible. But in the meantime, since we are all social distancing ourselves, we need to make the most out of the situation and what’s better than learning something new!

Since August 2019, Instagram has opened for everyone in the world to make Augmented Reality (AR) filter on Instagram and also Facebook. AR filters allow anyone who uses it to change the colour of their surrounding instantaneously, place a 3D object on real-world, do a virtual makeup on your face and many more all through our smartphone! Learning how to make AR filter is easy and it can become a creative hobby or even a skill that can earn you money if you become good at it.
> 

# 🔖 Articles and Tutorials

![https://miro.medium.com/max/1100/1*jAdw4vW-yTkVuJlyFAZjgw.png](https://miro.medium.com/max/1100/1*jAdw4vW-yTkVuJlyFAZjgw.png)

## Simple Square Packing Algorithm

> My initial read of the design was: largest value in the center, then increasingly smaller values packed around it. I knew that there would be fewer than about 7 distinct values. And the domain wouldn’t be too wide (all values between zero and one, roughly). Furthermore, these charts are rendered once each can be reviewed for correctness before the whole website is published. There was no need to have a fancy algorithm which would work for arbitrary input.
> 

The following algorithm was implemented on Observable [here](https://observablehq.com/@esperanc/rectangle-packing/2)...

---

[https://www.youtube.com/watch?v=NMpGmFNXSKI&feature=youtu.be](https://www.youtube.com/watch?v=NMpGmFNXSKI&feature=youtu.be)

## **Blender 2.8 Tutorial | Parametric Voronoi Sphere | 3d Modeling**

> In this tutorial for Blender 2.8, I'll show you a very quick and simple technique to generate a beautiful Voronoi style sphere from the basic cube using only the default modifiers in the software. The result will be a watertight mesh suitable for 3d printing or rendering.
> 

![https://github.com/villares/sketch-a-day/raw/master/2021/sketch_2021_02_04a/sketch_2021_02_04a.gif](https://github.com/villares/sketch-a-day/raw/master/2021/sketch_2021_02_04a/sketch_2021_02_04a.gif)

## **Sketch-A-Day Code**

> Welcome! My name is Alexandre Villares and since January, 2018 I have been coding sketches everyday, publishing the source code in the same repository that stores this page, [github.com/villares/sketch-a-day](http://github.com/villares/sketch-a-day).
> 

This is a great base of code that will help teach some techniques to be used as inspiration in one's own code. 

![https://i0.wp.com/www.danieldavis.com/wp-content/uploads/2020/02/BlueFull.jpg?w=1068&ssl=1](https://i0.wp.com/www.danieldavis.com/wp-content/uploads/2020/02/BlueFull.jpg?w=1068&ssl=1)

## **[Generative Design is Doomed to Fail](https://www.danieldavis.com/generative-design-doomed-to-fail/)**

> A concerned Autodesk representative pulled me aside at an event recently. “I read your article,” she began.

I tried to recall whether I’d said anything controversial. But my most recent article was relatively tame, just 1,300 words in Architect Magazine about algorithms generating building layouts. If anything, it was complimentary of Autodesk.

Around us, people at the conference were discussing the industry’s most pressing issues – robots, automation, climate change. The representative leaned in to reveal hers: “I noticed you didn’t mention generative design in your article.”
> 

# Courses

openFrameworks Tutorial Series 

[https://www.youtube.com/watch?v=NBpBR2gRPEE&list=PL4neAtv21WOlqpDzGqbGM_WN2hc5ZaVv7&index=70](https://www.youtube.com/watch?v=NBpBR2gRPEE&list=PL4neAtv21WOlqpDzGqbGM_WN2hc5ZaVv7&index=70)

I've found the following series of tutorials are a great beginning video series using [openFrameworks](https://openframeworks.cc/learning/). There are around 76  tutorials on the subject of using various features within the framework.  The following is the Circle Loop, but there is everything from Fonts to Audio. 

# Send me your inspirations...