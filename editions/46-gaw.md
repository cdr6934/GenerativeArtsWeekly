# #046 - Creative Coding / Generative Arts Weekly

[Website](https://www.generativecollective.com/) |  [Instagram](https://www.instagram.com/generate.collective/) | [Youtube](https://www.youtube.com/channel/UCBOYyqA-mqyoTSJ8pO9sQiA) | [Behance](https://www.behance.net/generatecoll) | [Twitter](https://twitter.com/generatecoll) | [BuyMeACoffee](https://www.buymeacoffee.com/generatecoll)

> “If you're not prepared to be wrong, you'll never come up with anything original.” -Ken Robinson
> 

I’ve had a number of requests and personal interest where 3D imagery is used to create generative art. So I hope that this is beneficial. 

Generative art can be done in almost every application. You will find that it can be done in [Photoshop](https://www.openpicture.art/), using code, using simply code in the browser, or just by hand as one of my fellow generative artists (Dan Gries) has done. 

[https://twitter.com/RectangleWorld/status/1534171286859042821?s=20&t=TGFqRPIKtHPByIxfhFyUCw](https://twitter.com/RectangleWorld/status/1534171286859042821?s=20&t=TGFqRPIKtHPByIxfhFyUCw)

In this writeup, I want to explore 3D generative art using Blender. First, I thought I’d start out by providing a bit of the landscape of what software is out there and what else one might be able to use to create generative art. 

### 3D Real Time Engines

There are other 3D environment platforms which are built for realtime interaction. Use cases for these engines are generally used in the creation of games and VR experiences. A few examples of these engines are [Unreal](https://www.unrealengine.com/en-US/?utm_source=GoogleSearch&utm_medium=Performance&utm_campaign=an*3Q_pr*UnrealEngine_ct*Search_pl*Brand_co*US&utm_id=17086214833&sub_campaign=&utm_content=July2020_Generic_V1&utm_term=unrealengine) Engine and [Unity](https://unity.com/). There are a few generative projects, one example is the work of [M](https://www.mpkoz.com/projects/oneofone-artwork)ichael Kozlowski which some of his work was done using Unity. 

[https://vimeo.com/674336844?embedded=true&source=vimeo_logo&owner=94735906](https://vimeo.com/674336844?embedded=true&source=vimeo_logo&owner=94735906)

### Graphical 3D Engines

Then there are the commercial “Blenders” which include Cinema4D, Maya, 3DS Max and Lightwave. All of these products have many of the same features except some have an easier learning curve, more efficient render algorithms, and what someone is comfortable because of what they learned in school or in a job. These do have programming languages that help extend the outputs in order to provide more generative outputs. 

Much of the 3D work done for commercials, Instagram and movies are done using these software pages. Some of the larger movie studios do have their own internal workflows but these are going to be the tools used for most of it. 

[Facebook](https://www.facebook.com/684443282/videos/461149089178842/)

### Procedural 3D Engines

I do think that it is good to point out one tool which specializes in procedural 3D animation from SideFX called [Houdini](https://www.sidefx.com/).  It has been used to create a number of amazing outputs. I am a huge fan, of its outputs as they have helped create some amazing work.

[https://vimeo.com/270339002](https://vimeo.com/270339002)

### 3D Programming Frameworks

These 3D frameworks will include things such as OpenFrameworks, Three.js, or AFrame.js.  Most of these are going to start with code and no GUI. However, they are built on top of core graphics libraries making it easier not to have to write boiler code or building a cohesive library around them. It is up to the imagination of the user to generate interesting compositions of the work that comes from it. 

### Graphics Languages

Then there are the core technologies that have built the  Most of these are going to start with code and no GUI. It is up to the imagination of the user to generate interesting compositions of the work that comes from it. A pure generative example of this is PiterPasma’s [Skulptuur](https://www.artblocks.io/project/173) project or the recent work of [Monotau](https://www.fxhash.xyz/generative/slug/cradle) on FxHash 

![Piter Pasma - Skulptuur Testmint 2021](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d2ed8060-040a-435a-b4df-c23a4bee9e4e/Untitled.png)

Piter Pasma - Skulptuur Testmint 2021

![Monotau - Cradle 2022](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/52314594-5c42-45d8-8286-fcb5d063c611/Untitled.png)

Monotau - Cradle 2022

### Programming Language Libraries

As you can see, the landscape for generating generative works in 3D is a rather large ecosystem of frameworks.  that are currently being used to create 3D content in a variety of different pieces. 

![Screen Shot 2022-07-07 at 1.59.02 PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/45c21e8c-1daa-42ba-a616-eb9733824190/Screen_Shot_2022-07-07_at_1.59.02_PM.png)

[https://docs.google.com/spreadsheets/d/105k6JNqRG9j_vQVXZZ_klzyvHF930JGyfm4bbopc8YU/edit?usp=sharing](https://docs.google.com/spreadsheets/d/105k6JNqRG9j_vQVXZZ_klzyvHF930JGyfm4bbopc8YU/edit?usp=sharing)

So let’s focus on [Blender](https://capture.dropbox.com/ellS7VBFaKvEkOXS). 

![Screen Shot 2022-07-11 at 10.46.51 AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6476d53c-a4f2-45f5-b6bf-a737c09e0881/Screen_Shot_2022-07-11_at_10.46.51_AM.png)

### W**hy learn Blender?**

- Open source
    - In the generative art community, there has been always an openness of sharing code and knowledge. This has become a limited due to the NFT craze of 2021 and the blantant plagurism from the $$ of the market.
    - Open source breeds innovation, community and quality feedback. In the case of Blender, it has one of a many great number of communities that have made some beautiful software.
- Easy entry-level workflow
    - I might be wearing rose colored glasses here, but I really do find that once overcoming the jargon of 3D development Blender is a tool that can be understood without months of practice.
    - Secondly, if you haven’t worked in 3D environments, its a great way to really dive into the world of creativity.
- Code based w/ Python but also node based
    
    [https://www.youtube.com/watch?v=r8hqLh_HE08](https://www.youtube.com/watch?v=r8hqLh_HE08)
    
    - It could be that I am not plugged into the community quite enough to have found many of the generative blender artists, I think there is some fascinating work that comes out of it such as the work in the video by David Mignot.
- Extensible - the plugins within Blender provide some powerful ways to extend its usage. Just to show some of the power of procedural / generative work check out the following plugins.
    
    [https://camo.githubusercontent.com/6fba43ea371dddcadb71e70cab6ea47e18c361c5401a19e54ee6dd4d8e557eb2/687474703a2f2f7777772e636f2d64652d69742e636f6d2f776f726470726573732f77702d636f6e74656e742f75706c6f6164732f323031352f30372f7469737375655f67726170686963732e6a7067](https://camo.githubusercontent.com/6fba43ea371dddcadb71e70cab6ea47e18c361c5401a19e54ee6dd4d8e557eb2/687474703a2f2f7777772e636f2d64652d69742e636f6d2f776f726470726573732f77702d636f6e74656e742f75706c6f6164732f323031352f30372f7469737375655f67726170686963732e6a7067)
    
    - [Tissue](https://github.com/alessandro-zomparelli/tissue) - Computational Design Tool
    - [Sverchok](https://github.com/nortikin/sverchok) - parametric design tool (this is similar to Grasshopper in Rhino)
- Large supporting community
    - There are so many Youtube tutorials, Patreon accounts and tool makers in the space. I’d suggest and take the time and get to know some of the community. Even if you aren’t interested in 3D work, there is so much inspiration that can be gleaned from these communities.

**Why not use Blender?** 

- If you want to play boss mode, then don’t pick Blender, you probably should work with GLSL in order to really give it a go.

## Blender Usage in Creative Coding / Generative Art

So the first person I think of generative art and Blender is Yann Le Gall. You can find much of his work on [Instagram](https://www.instagram.com/ylegall/). He has a  playful and “mind mending” aesthetic as he uses flow fields, circle packing, and all the fundamental algorithms used in many generative artists toolkits. 

![Screen Shot 2022-07-11 at 10.27.26 AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/221557cd-4061-4140-b8b3-12ae749fcea3/Screen_Shot_2022-07-11_at_10.27.26_AM.png)

Matt Deslaurier used Blender in one of his earlier data art works called [Crystal Towers](https://www.behance.net/gallery/56908173/Crystal-Towers) which used Three.js to generate the models and then used Blender to render the images. 

![https://mir-s3-cdn-cf.behance.net/project_modules/1400_opt_1/628c1756908173.59c133d04b721.jpg](https://mir-s3-cdn-cf.behance.net/project_modules/1400_opt_1/628c1756908173.59c133d04b721.jpg)

And there are others as well who have used Blender in different ways to produce work that is generative or at least procedural in nature. 

![[https://humphreyhippo.wordpress.com/2017/12/13/adventures-in-sverchoks-generative-art-node/](https://humphreyhippo.wordpress.com/2017/12/13/adventures-in-sverchoks-generative-art-node/)](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3213991-9a38-46e4-b5c3-c4056a1da6d6/Untitled.png)

[https://humphreyhippo.wordpress.com/2017/12/13/adventures-in-sverchoks-generative-art-node/](https://humphreyhippo.wordpress.com/2017/12/13/adventures-in-sverchoks-generative-art-node/)

![[https://blender-brussels.github.io/articles/experimental-mesh-generation/](https://blender-brussels.github.io/articles/experimental-mesh-generation/)](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cabfb39f-1fcd-49c2-8d04-cfff7b481e9d/Untitled.png)

[https://blender-brussels.github.io/articles/experimental-mesh-generation/](https://blender-brussels.github.io/articles/experimental-mesh-generation/)

Of course there are plenty more examples of stellar work but I hope that this at least will help motivate new explorations in different tools to see what can come out of other amazing worlds. 

### Additional Generative Blender Resources

 A few articles I’d suggest reading as you venture into Blender is: 

- **[Grease Pencil, Scripting and Generative Art in Blender](https://towardsdatascience.com/blender-2-8-grease-pencil-scripting-and-generative-art-cbbfd3967590)**
- **[Creative Coding in Blender](https://behreajj.medium.com/creative-coding-in-blender-2-92-a-primer-7ac1b6fec3f)**
- **[Procedural Generative Techniques in Blender](https://blendersushi.blogspot.com/2013/05/procedural-random-generative-modeling.html)**

These have all been in various editions of the newsletter over the past couple of years. However I thought I might put it together here as these have definitely been the best tutorials that I’ve come across of the last couple of years. 

[https://www.youtube.com/watch?v=bWmnbEwEpqk](https://www.youtube.com/watch?v=bWmnbEwEpqk)

[https://www.youtube.com/watch?v=KQJYwHD5AB8](https://www.youtube.com/watch?v=KQJYwHD5AB8)

Hope this gives you some resources to further explore some more 3D generative work.

Hope all is well with you! 

Chris Ried 

P.S. I have had a hard time finding any 

# 📰 Happenings

- [Eyeo Festival](https://eyeofestival.com/) - June 14 - 17, 2022
- [School of Poetic Computation](https://sfpc.study/) - Multiple Courses
- [Anderson Ranch Art Center](https://www.andersonranch.org/workshops/) - Multiple Classes
    - [Processing and Laser](https://www.andersonranch.org/workshops/?pn=3): Creative Code to Wood Panel - June 27 - July 1, 2022
    - [Drawing with Machines](https://www.andersonranch.org/workshops/workshop/drawing-with-machines-p0735-22/) - July 18 - 22, 2022

# 🔖 Articles and Tutorials

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/661e793e-88c6-4188-827a-5bf40a0fb47e/Untitled.png)

## ****[Procedural music composition with Python](https://deepnote.com/@essia/Procedural-music-composition-with-arvo-9b35ebd7-63e0-47bc-a3d5-c503954a083d)****

> Code is poetry, of course, but it is also music. The *[music21](https://web.mit.edu/music21/)*  Python package for computer musicology not only allows to investigate musical scores with data science, but also to write your own scores with mathematical operations. [Georges Dimitrov](https://www.georgesdimitrov.com/), composer and professor at Concordia University (Montreal, Canada), created the *[arvo](https://github.com/georgesdimitrov/arvo)* package, which includes well-known minimalistic mathematical operations on notes to create no less rich musical scores. In this notebook, I explain how to compose the piece just below with *arvo* and *music21* with minimalistic procedural composition techniques. You will need to have intermediate understanding of the Python programming language and basic understanding of western music theory.
> 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0701d78f-0cfc-45f5-abad-71fa9943309e/Untitled.png)

## [Rorschach Mask Animation in Wolfram Language](https://community.wolfram.com/groups/-/m/t/2518279)

> In this notebook we show a method to make animations of Rorschach images and project those animations over 3D surfaces. The work is inspired by the visual effects of Rorschach's mask in the [2009 movie "Watchmen"](https://en.wikipedia.org/wiki/Watchmen_(film))
> 

![https://miro.medium.com/max/1400/0*dVb8aVzGcOeqfjyS.jpg](https://miro.medium.com/max/1400/0*dVb8aVzGcOeqfjyS.jpg)

## **[How does DALL-E2 Work?](https://medium.com/mlearning-ai/how-does-dall-e-2-work-b6a7f912fc5f)**

> DALL-E 2 is an AI system that is capable of generating realistic and high-resolution images using a description in the form of natural language. It can also edit existing images using captions in the form of natural language.
> 

[https://vimeo.com/424315654](https://vimeo.com/424315654)

## **[20 Creative Things To Try Out with GPT-3](https://towardsdatascience.com/20-creative-things-to-try-out-with-gpt-3-2aacee3e2abf)**

> It’s a fascinating journey into the mind of a machine. We, beta-tester of GPT-3, put this monstrum of an NLP through its paces, experimented with semantics, helped with presets and safety/risk topics, observed phenomena, etc. After soliciting feedback from our beta-tester community, OpenAI will begin charging for API usage based on the pricing tiers. Things are moving ahead, and that’s a good part.
> 

# Send me your inspirations...