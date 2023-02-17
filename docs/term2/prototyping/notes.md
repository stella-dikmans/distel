##

🗓 Week 14 / 01 February -  2023

#prototyping for design

theorizing about it

`with Edu, Victor and Santi`

(somehow) unexpectadly this course turned out to be a series of intense lectures with subsequent (self-)explorative adapation trials. theoretically we are introduced to the huge fields of advanced manufacturing, rapid prototyping and other new design methodologies by victor and edu that really did their best to hold us up motivated. we are very much encouraged to play around with the various tools accessible to us and make up some (hands-on? - the computer) experiences with digital fabrication tools. when we come to the **[micro-challenge-week](https://stella-dikmans.github.io/distel/term2/prototyping/microchallenge/)** we actually explorer what it means to physicalize digital realities... 


## about electronics and codings
`with Victor`

with victor we party continued our conversation of **[transparentizing blackboxes](https://stella-dikmans.github.io/distel/term1/techbeyondthemyth/techbeyondthemyth/#about-transparentizing-blackboxes)** we started off last term. 

similarly in in the coding world, a lot of things are kept in the dark and made complicated so users use user-oriented-design products that prevent individual agency through mystifying easy things. 

arduino is one of these projects that work for a 
**[transparent electronics](https://stella-dikmans.github.io/distel/term1/techbeyondthemyth/techbeyondthemyth/#about-transparentizing-blackboxes)** as they aim to make coding more accessible to public and are all in for collective knowledges. we often consider Arduino being the wired-board that allows us to physicalize our codes yet actually arduino is a small organization that exists off tree complementary parts: the hardware, the software, and the community. their easy-to-handle softwares, can be used with any kind of hardware and thus allows all kinds of people to try out their ideas.

the best approach to prototype electronics is go with an already built prototyping electronics board – we will use ESP32 Feather board (hardware) with Arduino (software).

there is a think about languages here, there are very complex coding languages but we will try to keep it easy and use the arduino standard language for used for programmings of microcontrollers which is C and C++

a very helpful other tool are tthe arduino libraries

libraries: (arduino) libraries are *folders* of existing codes that are shared, it is a way to organize and contribute to the coding-functions. 

### challenge one - making music
first things first. get the arduino (which is actually not an Arduino but a feather [board])to work. the hooking up to the system works somehow with the help of us all... the the right pins into the right holes. bueno, therefore I need to find the descriptions of the holes in the **[Adafruit ESP32 feather](https://hackmd.io/OcD2aBtRTG2pRfJKVV8CBg#Pinout)**  BECAAAUSE, it does not show on the thing itself...

<img src="../board.png" alt="drawing" width="800"/>

well having done this, I check the working of my code and its relation to my microcontroller...

IMPORTANT TO REMEMBER HERE:
choose the right *port*: in this case: "/dev/cu.usbserial-0264F311"
and the right *board*: in this case: "Adafruit ESP32 Feather"

ok well. with some simple codes (found in the arduino internet) I'll make it to sing some songs for me. e.g. pink panther(in a very queery high tone but whatever), happy birthday and some irrelevant other note-compositions.

<img src="../arduino.png" alt="drawing" width="800"/>

alright, to be honest, it is getting quite soon quite boring playing all the pre-set songs through copy paste and hitting enter.

so I extetnt my Arduino... with a research on libraries...

to include a new library, I open a new Arduino file, then in its menu bar I search for "Sketch" and then *Include Library* > *Manage Libraries*.

the *mozzi* library (nickname for Mozart???). from the GitHub page, I download via the *code* a zip file and follow the instructions to **[install](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries)** it within my existing libraries.

bueno thats done. yet nothing of the codes to adapt sonic output makes a sound ... ?! trying my best to solve the wiring 

another nice application I would like to share here is our dear friend's birthday party. to avoid the typical party moment where everyone starts singing so loudly that they might drown out the others, we thought it would be nice to use our little music-making machiene instead. so we exposed the party guests to the queer sounds of the little featherboard.

<img src="../bday.png" alt="drawing" width="800"/>


(well, after that little warm up we ended up singing anyways)


## about the basic design tools 
(of digital fabrication e.g. 2D,3D,CAD, and CAM)

`with Edu`

what do we know as a class? our swarm intelligence: 

<img src="../miromap.jpg" alt="drawing" width="800"/>


when we are talking abuot CAD and CAM, we are talking about digitalizing realities and realizing digitalities. in 3D modelling we talk about *CAD (computer aided design)* softwares (e.g. Rhino, grasshopper, fusion, inventor, Autodesk…) and *CAM (computer aided manufacturing /machining)*. Overall, the digital industry is a MESS – there has for a long time not been a sharing of files, a sharing of a same language. therefore, we have a lot of different programs and languages that are used. but nowadays, different CAD softwares can output standard models that can be read by many other softwares.


talking about the basics of computing, the basics I should understand to design and print digitally on various axes.

what makes a computer is the CPU and the GPU...

CPU (central processing unit) very smart in doing heavy difficult mathematical equation, one after another: one operation that is very heavy 

and GPU (graphic processing unit) on the other hand is not so smart but can calculate a lot of small operations 

further vocabularies:

Vector = a mathematical equation a geometric description of an image = it is one operation (read by CPU)
No need for a lot of storage because what is being storage is just the equation

Pixel = is a square, located in a x-y grid. One image is actually a lot of pixels that are being put together (read by GPU) – each pixel is made up of RGB sub-pixels… 
You need a lot of data because all the pixels in the raster have to be stored


WHEN TO USE WHAT?

a capturing device (camera for photo or movie) will always make pixel-raster. rather than when you 2D/ 3D-model, you always try to model in vector – why? because here we can enlarge and reduce the image in all directions infinitely (whereas if you zoom into pixels, at one point the pixels will show)

SO to summarize: vectors are light files that can be enlarged and reduced without losing quality 
BUT often it needs to be translated into pixels so we can actually see it


even more wordings: 

sRGB: color space of red, green and blue – currently the defined standard in the web. (1999 by HP and Microsoft)

Adobe RGB space: especially suitable for editing high-quality images and photos for subsequent conversion to CMYK (CYAN, MAGENTA, YELLOW ,  BLACK that is used for printing the colors that computer screens display in RGB values)

resolution: how many pixels define your image in horizontal and in vertical

PPI: pixel per inch: 1 inch = 2,54 cm. So the PPI describe the amount of pixels in a 2,54 cm square.

NURBS modelling (Non Uniform Rational B-Splines: defines vectors, we can built a surface through lines between points – curves. Control points in space that define shape – good for fluid shapes with a lot of complexity and at the same time easy to modify (through the points)
CPU – you need a powerful CPU

Mesh modelling: a collection of vertices (points in space), edges, and faces
GPU – you just need a fast-pace operation tool able to handle a lot 
3D scanners are always meshes, because they measure points and faces in the space
Preferred modelling-method for manufacturing


A story… that I must research. Historically, male persons where hunting behind mammoth and needed to orient themselves in space, the females were searching for fruit and nuts and needed to separate colors so they could define better healthy and nutritious food sources over those that are old and rotten. I am not so sure about that...

ARE THESE TOOLS HELP US MODELLING FOR THE FUTURE?

*topology optimization (TO)* is a mathematical method, a way to design with a set of rules (very complex mathematical equations) for a structural calculation.

here, we start with a mass of material and take out everything that is not necessary
Strong as possible by being light as possible. the goal here is to maximum force, minimal material, shortened design process

what is topology? the term network topology refers to the arrangements, either physical or logical, of nodes and connections within a network *“Topology studies properties of spaces that are invariant under any continuous deformation. It is sometimes called "rubber-sheet geometry" because the objects can be stretched and contracted like rubber, but cannot be broken. For example, a square can be deformed into a circle without breaking it, but a figure 8 cannot”* 

e.g. a highly opotimized frame of a **[motorbike](https://formlabs.com/blog/topology-optimization/)** will looke like full of holes:

another method used in future design is:

*generative design* where we start not from a design but from nothing. here, we let the computer make the design to propose the design; we set up parameters for the design-proceess and the program proposes a design process to design. algorithms are used here to set up the parameters
e.g. all WeWork spaces are interior-designed with the aid of generative design to assure the best conditions for users

this *generative design* is even more optimized than *topology optimization*. the results might be similar but the *generative design* is faster and consumes less resources (energy).

what is a *parametric design*?  

a **[parametric design](https://stella-dikmans.github.io/distel/term2/prototyping/notes/#challenge-two-parametrizing-a-croissant)** is a type of design in which the shape, size, or other aspects of the design can be easily adjusted or modified by changing a set of parameters or variables. here, a design can be customized based on specific inputs or requirements (@grasshopper. this is made possible by using computer-aided design (CAD) software that allow you to specify a set of parameters and relationships between them as for example:

    Tinkercad: simple interface, variety of shapes and components

    Fusion 360: more advanced 3D design tool, robust set of features, great for creating complex designs

    OpenSCAD: open-source 3D modeling software that is primarily used for creating parametric designs, uses a script-based approach, which makes it great for creating repetitive shapes or objects

### challenge two - parametrizing a croissant

parametrize means to describe or represent in terms of choosen variables (parameters)

grasshopper for example is a parametric program that makes rhino models parametrically adaptable

<img src="../croissant2.0.png" alt="drawing" width="800"/>

great, my handsrawing are quick and easily understandable. to geta grip on something digital, I played with grasshopper (in rhino) to translate my sketches into (possibly) a printed (for sure plantbased) edition of my croissant? 

<img src="../rhinocroissant.png" alt="drawing" width="1200"/>




## closer into bidimensional (2D) fabrication
`with edu, josep, petra and others`

Light Amplification by Stimulated Emission of Radiation (LASER)

what can you do with a laser cutter? it heats materials through directing high power through optics.

various kinds of applying later-fabrications are: **[pressfit](http://fab.cba.mit.edu/classes/863.12/people/coleman.james/index.html)** (hold the pieces together just by pressure), stacking, interlocking (waffle), living hinge (pure geometry that makes something hard very flexible), material welding, origami, electronics, 


what **[materials](http://wiki.atxhs.org/wiki/Laser_Cutter_Materials)**. does the laser handle? low density materials such as plastics, wood, cardboard, fabrics, in general all organic materials and (non-organic) plastics

there are three (actually two) laser cutting processes

1. Engrave (burning a lot of material next to each other) and 
2. Marking (burning a line of material) are actually the same  - burning a bit if material
3. cutting

I always have to make a digital fabrication to get from CAD to CAM

<img src="../CADCAM.png" alt="drawing" width="800"/>

from laser cut to vinyl cut

what is tthe difference? on a vinyl cutter, we dont have a x-y axis like in the laser cutte, here we have a right-left movement where the material is being applied onto. but here there exist other parameters we can adapt: speed, force, and durance of application.

### challenge three - lasercut

make a parametric design, design and test a pressfit to hold the pieces together just by pressure

OR

make molds with stacking layers to cast a material ontop

## about embedded codings (or how to use input and output sensors)
`with Victor`

how can all this codings and electronics in the end serve us? there is one project that started in the FabLab / MDEF environment some years ago which presents this very clearly - the **[smart citizen](https://smartcitizen.me/)** platform makes citizens use sensors to invesitgate their immediate environments (well still thats not a purspose but it might still as well as inspire some interests). so what we are talking about today is how to connect the elcetronic means in ways that we understand the information shown. meaning in other words to **[sense and input and make us observe and output](https://hackmd.io/ECgw7zCkR7WbD5SkcVvcwg?view)** as an example and excercies, we are playing with **[light sensors](https://learn.adafruit.com/photocells)** and try to code in a way so we know the amount (or strenght?) of the light, reaching the sensor. so in a way we can dimm the light once we would add a controll function.  but for now it is just about setting up the featherboard in a way that a photo receptive sensor which receives light information (thus a **[light sensors](https://learn.adafruit.com/photocells)**) and translates that into elecrticity that therefore gives another sign/ output (such as the lightening of an LED light or the making of a sound).

so in the end we connect a LED and a button and a photo receptive sensor. then we make the light signal appeearing as a "morse code" and connect the LED sensor with the photo recepting sensor. 

### challenge four - till the enlightment

all of this works similar to the **[ghost machiene](https://stella-dikmans.github.io/distel/term1/techbeyondthemyth/techbeyondthemyth/#engaging-with-techmyths-in-groups)**)







