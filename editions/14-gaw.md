> The art of resting the mind and the power of dismissing from it all care and worry is probably one of the secrets of our great men. - ***Captain J. A. Hatfield***
> 

My apologies for not being able to put together a newsletter last week. There was so much going on in the week that I hadn't found the bandwidth to put it together and then needed a little R&D over the weekend. 

So rather than write here, I am going to share one of the submissions from Genuary 2021. Though this is simple, the process framework that you have here is rather powerful as it gives you some flexibility on what you may want to do with each of the lines that are were used to generate the following output.  

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/132f4256-9899-4c79-aa31-9c608c5bf32c/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/132f4256-9899-4c79-aa31-9c608c5bf32c/Untitled.png)

```python
// Genuary 2021 Day 24 - 500 Lines 

float x, y, div, r; 
float[] l;
int lines; 
LineSwing ls[];

void setup()
{
  size(1000,1000); 
  background(255); 
  
  // Variables

  lines = 100; 
  div = (width+50)/lines;
  l = new float[lines]; 
  r =300; 

  ls = new LineSwing[lines]; 
  for(int i = 0; i < lines; i++) 
  {
      y = (i+1)*div;  
      ls[i] = new LineSwing(y,getColor()); 
     // div = div - div/200;
  }
    for(int i = 0; i < lines; i++) { l[i] = random(-r,r) }
}

void draw() {

  for(int i = 0; i < lines; i++)
  {
     ls[i].draw(); 
     ls[i].update(); 
  }
DrawMargin(50);
} 

class LineSwing  {
 
  
  float x, y, noise_factor, len_init, len, alpha;
  color c; 
  LineSwing(float _y,  color _c) 
  {
    y = _y; 
    x = 0; 
    c = _c; 
    len_init = 25; 
    len = len_init;
    noise_factor = 0.002; 
    alpha = 100;
  } 
  
  
  void draw() {

      stroke(c); 
      noFill(); 
     //  fill(c,100); 
      
      beginShape(); 
    for(int i = 0; i < lines; i++)
    {
      if(frameCount == 1 ) {l[i] -= l[i]/80; }
       pushMatrix(); 
     // circle(0,0,1);  
      curveVertex(i*div,y+l[i]*sin(frameCount*0.02)); 
      popMatrix();
    }
    endShape(); 
  }
  
  void update() { 
    //len = len_init*map(sin(frameCount*0.02),-1,1,1,2); 
  } 
}

void saveImage() {
  int seed = 50; 
  String timestamp = year() + nf(month(), 2) + nf(day(), 2) + "-"  + nf(hour(), 2) + nf(minute(), 2) + nf(second(), 2); 
  saveFrame(timestamp+"-"+seed+".png");
}

// Color Functions 

 int colors[] = {#0F0F0F, #7C7C7C, #4C4C4C};

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

void DrawMargin(float m) {
  noStroke();
fill(255); 
rect(0,0,width,m);  // Top
rect(0,0,m,height); // left side 
rect(width-m, 0, width,height); // right side 
rect(0,height-m, width,height); // Bottom 
rect(width*0.2-10,0,20,height);
rect(width*0.4-10,0,20,height);
rect(width*0.6-10,0,20,height);
rect(width*0.8-10,0,20,height);
}
```

## Update!

I've also yet to finish the interview that I had with Tyler Hobbs which I really am excited to share with you all. But I think that if all goes well, I will be releasing our conversation next week!

# Genuary 2021 Week 3-4

I have not been able to complete every single one of the days, however, I have been quite happy with the results and the daily learning of really putting the nose to the grindstone and trying to learn new skills combined with what I had already used. The hashtag is used 4K which does have some noise but it has been a success.  

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1af3d95c-ffea-4a2b-ba8e-7d65fa769002/generate.collective_1611118033.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1af3d95c-ffea-4a2b-ba8e-7d65fa769002/generate.collective_1611118033.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a104b633-ce73-4451-98f0-3bd1bbc7ce1a/eclipse_generative_art_1611616061_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a104b633-ce73-4451-98f0-3bd1bbc7ce1a/eclipse_generative_art_1611616061_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d7143be5-78bd-4921-9d49-a200102a26cb/piterpasma_1611412077_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d7143be5-78bd-4921-9d49-a200102a26cb/piterpasma_1611412077_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9c34b57-686e-4d2c-a209-8dde8d5ae158/iso.hedron_1611297577_1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9c34b57-686e-4d2c-a209-8dde8d5ae158/iso.hedron_1611297577_1.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1ca0dd8b-e0e3-459f-84b2-da5dff7b3d76/thomasp85__1611828590.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1ca0dd8b-e0e3-459f-84b2-da5dff7b3d76/thomasp85__1611828590.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/de3bf854-b1ac-4d7a-9a16-5d05e6f677a4/rvig.art_1611424661.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/de3bf854-b1ac-4d7a-9a16-5d05e6f677a4/rvig.art_1611424661.jpg)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c475812b-5b4a-4d08-9155-0a58534bdeed/inf0bil_1611573917.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c475812b-5b4a-4d08-9155-0a58534bdeed/inf0bil_1611573917.jpg)

Credits go to: 

- [inf0bil](https://www.instagram.com/inf0bil/)
- [piterpasma](https://www.instagram.com/piterpasma/)
- [rvig.art](https://www.instagram.com/rvig.art/)
- [thomasp85](https://www.instagram.com/thomasp85_/?hl=en)
- [topologen](https://www.instagram.com/topologen/)
- [eclipse_generative_art](https://www.instagram.com/eclipse_generative_art/)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/981c7442-52d3-4c21-b051-bb3631ad072e/topologen_1611762156.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/981c7442-52d3-4c21-b051-bb3631ad072e/topologen_1611762156.jpg)

# Inspirations

---

# 🖌️ Unconventional Media

![https://dam-prod.media.mit.edu/thumb/2017/10/13/silkPavilion_7.jpg.1400x1400.jpg](https://dam-prod.media.mit.edu/thumb/2017/10/13/silkPavilion_7.jpg.1400x1400.jpg)

## MIT **[Silk Pavilion](https://www.media.mit.edu/projects/silk-pavilion/overview/)**

> Inspired by the silkworm’s ability to generate a 3D cocoon out of a single multi-property silk thread (1km in length), the overall geometry of the pavilion was created using an algorithm that assigns a single continuous thread across patches providing various degrees of density. Overall density variation was informed by the silkworm itself deployed as a biological printer in the creation of a secondary structure. A swarm of 6,500 silkworms was positioned at the bottom rim of the scaffold spinning flat non-woven silk patches as they locally reinforced the gaps across CNC-deposited silk fibers.
> 

# 📸 Generative Graphics

[https://www.youtube.com/watch?v=KW2Fa23lxwM&t=317s](https://www.youtube.com/watch?v=KW2Fa23lxwM&t=317s)

## Generative Ocean Waves

> TitanOceans - is a module made in Pure Data in order to create oceanic like waves using various kinds of filtered noise. From methane oceanic waves to digital emotion oceanic waves.
> 

Its simple, yet there is something beautiful in being able to take the sounds of oceans and make them create such peaceful noise. 

# 🏛️ Exhibits / Installations

[https://vimeo.com/253178355](https://vimeo.com/253178355)

# [The Geometry of Artificial Intelligence](https://biogenic.design/project/intelligence)

The intention was to show how a digital thought evolves, how AI becomes self aware and re-structures its physiology, constructs layers of digital consciousness, creating a tapestry, architecting a new law of physics. Design is inspired by neural networks, spiderwebs and patterns in nature.

# 🔖 Articles and Tutorials

![http://www.citizen-statistician.org/post/2020-05-04-dipping-my-toes-in-generative-art-with-my-sister_files/figure-html/art-mine-1.png](http://www.citizen-statistician.org/post/2020-05-04-dipping-my-toes-in-generative-art-with-my-sister_files/figure-html/art-mine-1.png)

## [Dipping My Toes in Generative Art With My Sister](http://www.citizen-statistician.org/2020/05/dipping-my-toes-in-generative-art-with-my-sister/)

> For those of you who don’t speak Turkish, this translates to “WOAH so pretty, how did she make this?” So I linked to Danielle Navarro’s blog post on getting started with generative art, and my sister’s response was “I read this, and really wanted to understand it, but I can’t follow it. Should we try it together?” I should clarify that my sister doesn’t know R. She is a UX/UI designer and an illustrator, and she’s pretty technical, but she’s not a programmer. She obviously knows what R is since I won’t stop talking about it.
> 

![https://blog.nishtahir.com/content/images/size/w2000/2018/11/prague.jpg](https://blog.nishtahir.com/content/images/size/w2000/2018/11/prague.jpg)

## [On Generative Art and Impressionism](https://blog.nishtahir.com/generative-impressionism/)

> This idea doesn't seem too far fetched at the surface level; after all, it's easy enough to view programming as a craft when looking at fields like the video game industry or digital art careers such as modern art and special effects. However, these tend to focus more on the application of software as a medium for storytelling. I wanted to take this thought a step further by posing the question can programming or code be the primary medium through which artists express themselves?
> 

![https://www.cs.cmu.edu/~kmcrane/Projects/MonteCarloGeometryProcessing/teaser.png](https://www.cs.cmu.edu/~kmcrane/Projects/MonteCarloGeometryProcessing/teaser.png)

## [Monte Carlo Geometry Processing](https://www.cs.cmu.edu/~kmcrane/Projects/MonteCarloGeometryProcessing/index.html)

> This paper explores how core problems in PDE-based geometry processing can be efficiently and reliably solved via grid-free Monte Carlo methods. Modern geometric algorithms often need to solve Poisson-like equations on geometrically intricate domains.
> 

If you want to watch presentation of the paper, there is a great presentation of the Monte Carlo methods that he is using in order to better fit complex shapes using geometry processing.  

[https://www.youtube.com/watch?v=zl9GtPX0LjM&feature=emb_title](https://www.youtube.com/watch?v=zl9GtPX0LjM&feature=emb_title)

![https://northeastofnorth.com/wp-content/uploads/2018/09/Absolut-Cracking-02AB016-12k-04-Final-3000x3000-e1538337528413.png](https://northeastofnorth.com/wp-content/uploads/2018/09/Absolut-Cracking-02AB016-12k-04-Final-3000x3000-e1538337528413.png)

## [UCRACKING – GENERATIVE ART FROM MARIUS WATZ](https://northeastofnorth.com/ucracking-generative-art-from-marius-watz/)

> Marius Watz is a Norwegian artist and curator who works in the field of generative art. He will be exhibiting as part of the Weave by Abertay group show in the Wellgate centre for this year’s NEoN digital arts festival. He will also be exhibiting work in the café of the Dundee Science Centre as part of the Dundee Science Festival from 20 October, when there will be an interactive workshop inspired by his work
> 

[https://www.youtube.com/watch?v=AM60OPmrUG0](https://www.youtube.com/watch?v=AM60OPmrUG0)

---

## I[nteractive Controls for Live Performance](https://www.dropbox.com/s/xoi5bfvdzg5p8zh/TDSummit_Synthestruct_InteractiveControlWorkshop.87.toe?dl=0)

> in this workshop, we started experiencing audio problems in the recording for ~1 hour. The topic was OSC connections and intro to Kinect Studio Recorder. We have cut that part of the video out and made it available in this separate video if you are really eager to listen regardless of the audio problem. Thanks for your understanding.
> 

[https://www.youtube.com/watch?v=VBzIPLh-ECg&feature=emb_title](https://www.youtube.com/watch?v=VBzIPLh-ECg&feature=emb_title)

## [Creating Generative Visuals with Complex Systems](https://www.dropbox.com/s/3js3dnqq1wisidq/Complex%20Systems%20Example%20Files.zip?dl=0)

> This workshop will walk participants through the process of creating real-time generative visuals using two types of systems: reaction-diffusion and cellular automata. Both methods yield a variety of complex and often non-repeating patterns.
Reaction-diffusion systems model the changing of one or more chemical substances. The examples that will be addressed in the workshop include beginner level TOP-based methods and a brief discussion of intermediate level techniques using GLSL. Cellular automata are simulations consisting of grids of cells which change their state based on simple rules. Participants, along with the instructor, will build 1D and 2D cellular automata systems from scratch using GLSL and will look at examples which incorporate decaying cells (or the “generations” variation) along with methods for utilizing multiple rule-sets in one system.
These patterns, while compelling on their own, can also be used as the input to other systems. This session will help participants understand how to use their motion to drive particles systems and manipulate geometry, in addition to exploring how to add interactive elements to these systems, such as audio-reactivity and motion control from a Kinect or Leap Motion. Above all, the workshop will expose participants to an iterative approach to creating generative visuals, exploring ways of reusing concepts and techniques in new ways
> 

## The Book of Chaos

[https://www.youtube.com/watch?v=kZNTozzsNqk](https://www.youtube.com/watch?v=kZNTozzsNqk)

> Every artist has their tools - paint, pens, canvases, or film - that they use on a daily basis. Have you ever wondered what a generative artist's box of tools looks like? What algorithms do we use? How do we deal with color? How do we make code-generated artwork appear natural?
> 

# Courses

## [Programming Graphics: Introduction to Generative Art](https://www.skillshare.com/classes/Programming-Graphics-I-Introduction-to-Generative-Art/782118657?via=search-layout-grid)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7cac7b21-9094-48bd-a243-53c4e512d407/03aa88bf.jpeg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7cac7b21-9094-48bd-a243-53c4e512d407/03aa88bf.jpeg)

> Generative art is all about using programming to generate artwork that is algorithmically defined and created. In this project-based class, you'll learn how to create your own series of patterns using generative art techniques and computer programming!
> 

If you haven't done generative art before and you want to learn; this is another great course on giving you the power of taking on generative art and teaching the core concepts of generative art using a coding language. It is a Skillshare course; this is not free but if you use the following link it gives you a [14 day free access to the course.](https://skl.sh/3cklG6R) 

# Send me your inspirations...