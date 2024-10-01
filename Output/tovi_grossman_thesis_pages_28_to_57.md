 
 
14 
2. Background Literature 
 
“Ability is the art of getting credit for all 
the home runs somebody else hits.” 
-Casey Stengel
 
 
 
2.1 
Introduction 
In Section 1.2, we discussed the new affordances presented by volumetric displays. These 
affordances raise new human factors issues and interaction challenges. Once these new 
topics are better understood, applications, and the user interfaces and interaction 
techniques which they are made up of, can be appropriately designed. In this chapter, we 
review the previous research which will help guide our investigation into making 
volumetric displays an interactive platform. 
The chapter will be structured as follows. In Section 2.2 we present an overview of 
existing 3D display technologies, followed by a description of existing volumetric display 
technology in Section 2.3. Section 2.4 looks at methods for evaluating the viewing 
experience in these various 3D displays, which can be extended to the study of 
volumetric displays. In Section 2.5, we provide an overview of the input devices used for 
interacting with 3D environments. In Section 2.6, we look at some of the basic interaction 
techniques existing in the virtual reality and 3D interaction communities, which will 
provide insights into the development of interaction techniques for volumetric displays. 
In Section 2.7, we look at work which integrates these interaction techniques into 3D 
applications. Section 2.8 focuses on collaborative applications, which will aid in the 
development of interaction techniques for volumetric displays, under a multiple user 


 
15 
 
scenario. Because there is such a large collection of related research, we focus our 
literature review on the most relevant and initial works where the concepts appeared. 
2.2 
Three-Dimensional Display Technology 
In this section we provide a background on the types of display technology which have 
been used to present three-dimensional data. These display techniques all utilize various 
depth cues which have been identified in psychological research on human perception. 
We now discuss the display techniques, and the associated cues which these displays 
provide. 
2.2.1 Perspective Displays 
A basic method for displaying three-dimensional environments, which is commonly used 
in 3D graphics, is to use a standard workstation monitor, using a perspective projection. 
Perspective displays utilize perspective and relative size cues, in which objects further 
away, produce smaller retinal images than closer objects. Such displays are commonly 
exploited in 3D graphics [Foley et al. 1990]. Brooks [1988] notes that perspective cues 
are particularly effective when parallel lines are displayed within the scene. 
Another cue which is utilized in perspective displays is motion parallax, also referred to 
as the kinetic depth effect. With this cue, a sensation of depth is produced when an object 
moves in space relative to an observer. For this reason, interfaces should provide a 
mechanism for moving the viewpoint in a 3D scene [Brooks 1988, Lipscomb 1981]  
By utilizing these two powerful depth cues, perspective displays are effective tools for 
viewing and interacting with three-dimensional data, and are still the most commonly 
employed display type for tasks such as 3D graphics design and animation. 
2.2.2 Non-Immersive Stereoscopic Displays 
An important depth cue which cannot be provided by a standard workstation monitor is 
stereopsis. This depth cue is produced from the binocular disparity when viewing 3D 
objects in natural environments. It can be particularly strong when the perceived objects 
are close to the viewer [Yeh 1993]. To provide stereopsis, a system simply needs to 


 
16 
 
present different images for the left and right eyes, to produce the required binocular 
disparity. A fused 3D image appears at the point of convergence between the two images.  
There are a number of display technologies which can provide stereopsis on a flat screen 
[Arditi 1986, McAllister 1993]. Common examples of stereoscopic displays are polarized 
glasses which passively block certain light from each eye and liquid-crystal time-
multiplexed shuttering glasses which actively block light from each eye [Lipton 1985]. 
Autostereoscopic displays are another class of stereoscopic displays, which are glasses 
free systems that project multiple images for each eye in specific locations in space 
[Dodgson 2005]. 
 
Figure 2-1. Fish tank displays combine stereoscopic and head tracking technology to 
create a viewing volume roughly equivalent to the inside of the monitor. Image taken 
from Ware and Franck [1996]. 
2.2.3 Semi Immersive Fish Tank Displays 
The display technologies discussed so far are generally considered to be non-immersive, 
as there is a clear distinction between the physical and virtual environments. Fish tank 
displays increase the level of immersion by coupling the viewpoint of the virtual scene, 
with the physical location of the user’s head, so that the appropriate perspective is always 
presented [Diamond et al. 1982a, Fisher 1982, McKenna 1992b, Sollenberger and 
Milgram 1991, Sollenberger and Milgram 1993, Ware et al. 1993] (Figure 2-1). 
Generally the user’s head position is tracked, and the location of the user’s eyes is 
estimated by offsetting them by a constant distance from the user’s head [Arthur et al. 
1993]. The viewpoint of the virtual scene is then updated appropriately. The virtual scene 


 
17 
 
can be perceived monocularly, coupled to a single eye position, or binocularly, if 
combined with one of the stereoscopic technologies discussed above. Because the scene 
is still projected on a 2D display, fish tank displays are considered to be semi-immersive. 
Generally the viewing volume of these displays is roughly equivalent to the inside of the 
monitor, so viewing them is similar to looking into a fish tank. The head coupled 
viewpoint with fish tank displays provides motion parallax cues, without requiring users 
to explicitly manipulate the camera position. 
2.2.4 Head-Mounted Displays 
More immersive forms of displays, typically associated with the field of virtual reality, 
which provide stereopsis and motion parallax through head coupled viewpoints, have also 
been developed. A common form is a head mounted display, which use some sort of 
helmet or goggles to provide a stereo pair of displays directly in front of each eye 
[Buxton and Fitzmaurice 1998, Neale 1998, Sutherland 1968] (Figure 2-2). Such displays 
provide the widest possible field of view at high quality. Head mounted displays can 
provide the user with a realistic 3D experience, but a significant problem is that the user’s 
eyes are covered by the display. The result is a lost context of the user’s physical 
surrounding and possible collaborators [Arthur et al. 1993, Buxton and Fitzmaurice 
1998].  
 
Figure 2-2. A head mounted display creates an immersive virtual reality by covering the 
user’s eyes. Image taken from Buxton and Fitzmaurice [1998]. 


 
18 
 
A solution to this problem is to allow users to see the physical world, such as their hands, 
tools, and other people, while wearing the display. This can be accomplished by 
mounting video cameras onto the displays, and incorporating their images into the virtual 
world which the user sees [Azuma and Bishop 1994, State et al. 1996, Yoo and Olano 
1993]. The cameras act as an extra set of eyes for the user, projecting a view of the 
physical world onto the computer generated view of the virtual world. This is similar to 
providing the user with a heads up display, using an optical see-though display. This 
approach is generally known as augmented reality, as the systems augments the physical 
world with additional virtual imagery [Feiner et al. 1993b].  
 
Figure 2-3. Schematic of a Cave system. Tiled rear projected images appear on multiple 
faces of the room. Figure taken from Cruz-Neira et al. [1992]. 
2.2.5 Cave 
Another interesting form of an immersive 3D display is known as a Cave [Cruz-Neira et 
al. 1992]. A Cave is room where the walls, floor, and ceiling, act as the display (Figure 
2-3). To provide a seamless view of the virtual scene, each of the displays must be tiled 
together at the edges where they intersect. The projected surfaces of the Cave are 
typically in stereo, with the user wearing a pair of glasses. Furthermore, the head is 
tracked so that the appropriate perspective is always presented to the user. A benefit of 
Caves over head mounted displays is that users can still see and have a maintained 
context of their physical surroundings. A number of other systems similar to Caves have 
also been developed, which vary in size, and also the number of surfaces which are 
projected onto. One example is large scale projection displays, such as the ImmersaDesk, 


 
19 
 
which are stereoscopic but are only displayed on a single surface [Czernuszenko et al. 
1997]. Small format caves have also been built, such as the Cubby system, where three 
head tracked back projection screens form a cubic workspace in front of the user 
[Djajadiningrat et al. 1997].  
2.2.6 Chameleon 
A less common technology for presenting 3D environments is the Chameleon system 
[Fitzmaurice 1993]. With the Chameleon system, perspective images of three-
dimensional scenes appear on a small display held in the palm of the hand. As with fish 
tank and head mounted displays the perspective view is continuously updated. However 
the perspective viewpoint is determined by the position of the display, rather than being 
coupled with the head of the user.  
The Chameleon approach is almost like using a magnifying glass which looks into a 
virtual scene, rather than the physical world. While the display does not provide the full 
immersive feeling or viewing angle of a cave or head mounted display, users can easily 
browse the scene by moving the lightweight display.  
There have been other implementations of Chameleon displays. The boom chameleon 
[Tsang et al. 2002] consists of a flat-panel display mounted on a tracked mechanical 
boom. The armature of the boom is carefully balanced to allow the display to float 
weightlessly in space. The display acts as a physical window into 3D virtual 
environments, through which a one-to-one mapping between real and virtual space is 
preserved. 
Chameleon systems can also have the ability to support augmented reality. Fitzmaurice 
[1993] showed how location tracking could also be used to sense the context of its 
environment. For example, bringing the display close to a map could give additional 
information about the region that it was close to. Rekimoto [1996] augmented 
Chameleon-like devices further by adding video cameras, allowing computer-generated 
information to be superimposed over a view of the physical world. 


 
20 
 
2.2.7 Summary 
We have presented a variety of display technologies for three-dimensional data. The 
displays provide different levels of immersion to the users ranging from non immersive 
perspective displays to fully immersive head mounted displays. Each display has its own 
unique properties which afford different methods of interaction. In the next section, we 
will discuss various volumetric display technologies. By examining and comparing the 
properties of volumetric displays to the technologies discussed in this section, we will 
gain an understanding of what interaction techniques will transfer well to volumetric 
displays, and what interaction techniques will require modifications or enhancements.  
2.3 
Volumetric Displays 
Unlike the other display technologies previously discussed volumetric displays present 
imagery in true 3D space. The viewing space is divided up into 3D pixels, called voxels, 
which illuminate visible light from the regions which they appear. Because light is 
emitted in true 3D space, depth cues such as motion parallax and stereopsis will always 
be present without the need for supplementary hardware. From a technological stand 
point, there are some interesting differences between the various implementations of 
volumetric displays. While they all generate true 3D images, the underlying technology 
of the various displays vary greatly in both concept and design. From an interaction 
standpoint, however, these differences will not be so critical, as all of these displays pose 
the same qualities which we have discussed in Section 1.2. We now provide an overview 
of the basic classes of 3D volumetric displays. 
2.3.1 Oscillating Swept Volumetric Displays 
A common method for presenting volumetric imagery is to use a two-dimensional image 
which periodically sweeps out a three-dimensional volume of space. When the space is 
swept out cyclically at a frequency higher than what the eye can resolve, a spatial image 
is formed through the persistence of vision. We now discuss the class of displays in 
which volumes are swept out by oscillating screens. 
An early implementation uses a vibrating CRT where the images which output to the 
screen are synchronized within each oscillation cycle, so that each image appears at the 


 
21 
 
appropriate position of the tube [Blundell et al. 1993]. Because of the high mass of the 
tube, it would be difficult to obtain the desirable rapid acceleration and deceleration at 
each end of its oscillation.  
A more practical suggestion is to have the phosphorous screen within the CRT oscillate 
rather than the entire CRT itself [Rawson 1969]. The screen is mounted within a vacuum 
tube behind a transparent viewing globe, and oscillates with a piston like motion. An 
electron gun illuminates the screen from the rear (Figure 2-4). 
.
 
Figure 2-4. An oscillating phosphorous screen is illuminated by an electron gun. Figure 
taken from Langhans et al. [1998]. 
A variation of the oscillating screen, is to have an oscillating mirror from which a CRT 
image is viewed [Langhans et al. 1998]. The mirror moves such that the visual path 
length is swept periodically, and the CRT image apparently sweeps out the volume. The 
drawback of this scheme is that the viewing angle is limited to the reflective surface 
coverage.  
Because of the inertial forces required for oscillating screens, this class of displays 
generally has problems with vibration and noise. The accelerations involved also limit the 
oscillation frequency, causing considerable flicker of the displayed images. A more 
promising approach is a rotating swept display, which we now discuss. 
2.3.2 Rotating Swept Volumetric Displays 
One of the earliest implementations of rotating swept volumetric displays was developed 
by the ITT Laboratories in 1960, which consisted of a cathode ray tube whose light is 
optically transferred to a translucent rotating screen within a glass cylinder [ITT-
Laboratories 1960]. The motor driven panel turned at approximately 20 revolutions per 


 
22 
 
second. Another implementation was presented in 1963, where a phosphor-coated screen 
rotated in a vacuum, with a controlled electron beam striking its surface. The 3D images 
were presented by having the electron beam project on the screen as it passes through the 
desired location of space [Ketchpel 1963]. 
The rotating screens can also be actively emissive, instead of having imagery projected 
onto them. Berlin proposed using a 2D matrix of light emitting diodes (LEDs) with the 
light electronics rotating to sweep out a 3D volume [Budinger 1984] (Figure 2-5). In this 
implementation, the display resolution is a function of the number and density of LEDs, 
the speed of rotation, and the rate at which LEDS can be pulsed. 
 
Figure 2-5. Rotating volumetric display using an emissive panel of LEDs. Figure taken 
from Langhans et al. [1998]. 
 
Figure 2-6. High-end rotating volumetric displays. (a) Felix: www.felix3d.com. Image 
taken from Balakrishnan et al. [2001]. (b) Perspecta: www.actuality.com. 


 
23 
 
The above rotating displays are swept out by flat surfaces. However in another class of 
volumetric displays, the viewing volume is swept out by a curved surface. The shapes of 
such displays can be spherical spirals [Langhans et al. 1998] or helical [Bahr et al. 1996]. 
Recently, rotating swept displays have been developed to use light fields to display 
different imagery to each viewing angle [Cossairt et al. 2007, Jones et al. 2007]. The 
benefit of such displays is that they can produce viewpoint dependent rendering effects, 
such as shading, and hidden surface removal. However, such displays are not truly 
volumetric, as the perceived location of a voxel might not be the actual location where it 
is emitted.  
Rotating volumetric displays are one of the more promising technologies to date, with 
current implementations being available commercially (Figure 2-6). This is the 
technology we use in this thesis (Section 1.4). 
2.3.3 Static Volumetric Displays 
Static volumetric displays are defined as displays which generate light in true 3D space, 
without the need for mechanical motion [Ebert et al. 1999]. With this technique, emissive 
voxels are provided at a large number of locations in a static setup, without the use of 
oscillating or rotating mirrors or screens. This can be accomplished by exciting a plasma 
filled medium within a display volume to produce a glow at a single point. 
A proof-of-concept of this displays was implemented in 1971, where two faint spots of 
light were generated inside a transparent crystal of erbium-doped calcium fluoride, with 
the use of filtered xenon lamps as excitation sources [Lewis et al. 1971]. 
Based on this early work, Downing et al. presented a three-color static volumetric display 
with improved material using high powered laser diodes [Downing et al. 1996]. The laser 
beams intersect inside a transparent volume, which consists of a rare earth-doped heavy 
metal fluoride glass. Red, green, and blue voxels can be illuminated by sequential two-
step resonant absorption. Imagery can be produced in 3D by scanning the point of 
intersection of the lasers in various 3D locations of the volume. The demonstrated work 
was implemented in a prototype sugar-cube sized volume (Figure 2-7). 


 
24 
 
 
Figure 2-7. A prototype sugar-cube sized static volumetric display. Image taken from 
www.3dtl.com.  
In another implementation, a gaseous volume was enclosed within a sealed glass 
container. Two diode lasers were intersected in Rubidium vapor [Kim et al. 1996]. The 
setup requires Rubidium to be heated within a vacuum, making it difficult to design for 
larger scale display volumes.  
A more recent implementation used a pulsed laser to create glowing points of plasma in 
midair [Uchiyama et al. 2006]. This is one of the few volumetric displays which does not 
require a physical enclosure. However, the points of plasma are at an extreme 
temperature, so users are still unable to reach in and interact with the displayed imagery.  
Although the current level of quality for static volumetric displays is not up to par with 
the current generation of rotating swept volumetric displays, their desirable properties 
make for a promising alternative which researchers continue to develop. 
2.3.4 Summary 
This section has outlined the most common technological implementations for volumetric 
displays. From an interaction standpoint, these technological differences may not seem so 
interesting; however, there are some interesting observations to be made. Most 
importantly, all of the discussed technologies share the properties which we have 
discussed in Section 1.2.  
What is not common among the displays discussed in this section is the shape and size of 
the physical enclosure. For example, we have seen hemispherical domes, as well as 


 
25 
 
cuboids. Thus, if the enclosure is to be used as an interactive surface, then the interaction 
techniques which are designed should be able to be implemented regardless of the shape 
of the enclosure surface. We will consider this in our designs presented later in this 
thesis, and also discuss how our results can be generalized to other display forms in 
Chapter 9. 
2.4 
Evaluation of Three-Dimensional Viewing Modes 
In the previous two sections we have discussed the various display technologies for 
viewing 3D data. With all the available types of 3D display technologies, it is important 
for designers to know which will be the most appropriate device for their task at hand. 
Most relevant to our work, we will want to determine under what condition volumetric 
displays will prove to be beneficial. Researchers have tried to address this issue by 
conducting formal evaluations to provide comparisons of different viewing modes. We 
now provide a summary of such research, and an overview of the important results 
obtained to date. 
2.4.1 Subjective Impressions of Three-Dimensional Viewing Modes 
In an early study, Ware et al. compared the relative effectiveness of head coupled and 
stereoscopic views by allowing users to make comparisons between pairs of presentation 
methods [Ware et al. 1993]. Two different 3D scenes were presented to users. One 
consisted of a sphere with its shadow cast on a ground plane. The other consisted of a 
bent piece of tube based on Shepard and Metzler’s mental rotation for 3D objects 
[Shepard and Metzler 1971]. Once a scene was presented, subjects could toggle between 
two presentation modes until they could decide which contributed more to the perception 
of the 3D space.  
The experiment consisted of the following 5 conditions: perspective, stereo, head coupled 
monocular, head coupled binocular, head coupled with stereo. In the non-stereo 
conditions the same scene was presented to both eyes. In the binocular condition the 
viewpoint was between the eyes, while in the monocular condition, the viewpoint was 
correct for the right eye, and the subjects were asked to close their left eye. In the fixed 


 
26 
 
viewpoint conditions, the perspective view was established by the initial head position at 
the start of the trial.  
For each trial of the experiment, subjects were given one of the 10 pair wise comparisons 
of the 5 viewing conditions. Subjects toggled between the viewing conditions until they 
made their final selection, as to which was “best”. 
Their results showed no differences between the two scenes so their data was combined. 
The results showed that users rarely preferred stereo without head coupling over head 
coupling without stereo. Another interesting result was that users picked head coupling 
without stereo over head coupling with stereo 68% of the time. The authors attribute this 
result to the ghosting effect in the stereo conditions, caused by imperfect phosphor decay, 
which causes cross talk between the left and right images. 
Most importantly, their results supported the use of head coupled stereo viewing. All 
subjects said that they would use it for object visualization it were available.  
2.4.2 Empirical Evaluation of Stereo and Motion Cues  
The results of the subjective evaluations of three-dimensional viewing modes are 
unsurprising: providing stereo or motion cues will improve the user’s perception of a 
three-dimensional scene. Researchers have also tried to quantitatively determine exactly 
how much is gained by moving from 2D to 3D representations. Ware and Franck note 
that a completely general answer to this question cannot be expected, because the 
advantages will greatly depend on the specific task at hand [Ware and Franck 1996]. To 
gain a preliminary understanding of the issues, researchers have commonly chosen a path 
tracing task in a network of nodes, of which the results can be generalized to the large set 
of problems which can be represented in this way [Arthur et al. 1993, Sollenberger and 
Milgram 1991, Sollenberger and Milgram 1993, Ware et al. 1993, Ware and Franck 
1996]. 
It has been shown that stereoscopy can improve user performance when detecting paths 
in a tree structure [Arthur et al. 1993, Sollenberger and Milgram 1991, Sollenberger and 
Milgram 1993, Ware and Franck 1996]. Sollenberger and Milgram [1991, 1993] also 
found that scene rotation further reduced errors in such a path tracing task. In their 
implementation, scene rotation was controlled by the system. In a follow up study, Ware 


 
27 
 
et al. [1993] found similar results when the motion was controlled by the user, in the form 
of a head coupled perspective view. 
In one of the more recent studies, Ware and Franck [1996] evaluated nine different types 
of viewing modes for a path tracing task. Randomly generated graphs were presented, 
and users were required to determine if two highlighted nodes were connected by a path 
of length two. The viewing modes consisted of different combinations of perspective, 
stereo, and motion parallax cues, where they tested both hand, head, a system controlled 
rotation of the scene. 
It was found that the stereo viewing mode without motion was significantly worse than 
all three tested stereo modes with motion, including system controlled rotation, hand 
coupled rotation, and head coupled rotation. Of the three viewing modes which combined 
stereo and motion, there were no significant differences, showing that the motion parallax 
cues were important, but it did not matter how they were provided.  
In the virtual reality literature, researchers have attempted to quantify the benefits of 
immersion within virtual environments. Barfield et al. found that head tracking 
significantly improves users’ sense of presence [Barfield et al. 1997]. In a collaborative 
task, where two users had to maneuver a ring through a 3D object, Narayan et al. found 
that stereo was extremely important, while head tracking did not provide significant 
performance gains [Narayan et al. 2005].  
2.4.3 Qualitative Evaluation of Volumetric Displays 
Because volumetric displays are still in the developmental stages, little evaluation has 
been conducted to provide a quantitative comparison to other 3D viewing modes. 
However, qualitative benefits associated with their use have been reported. Balakrishnan 
et al. provide a good summary of these benefits, which we now discuss [Balakrishnan et 
al. 2001].  
The fundamental difference is that volumetric displays generate images in true 3D space, 
so imagery can be viewed within the displays, just as one would view real physical 
objects. The human viewer can use their natural physiological mechanisms for depth 
perception, such as true motion parallax and stereopsis through eye convergence and 
accommodation, without the need for supplementary hardware. Furthermore, the 


 
28 
 
convergence and accommodation cues are consistent, unlike in stereoscopic displays. As 
a result, the documented problem of asthenopia should not occur from viewing 
volumetric displays.  
Another advantage of volumetric displays which Balakrishnan et al. discuss is that they 
provide a 360° viewing angle. As a result, these displays can be viewed from almost any 
angle, and can be viewed by multiple users simultaneously. This makes volumetric 
displays particularly suitable for collaborative applications. 
2.4.4 Quantitative Evaluation of Volumetric Displays 
To date, only a few studies have been reported, and none provide conclusive evidence as 
to how volumetric displays compare to other existing 3D display technologies for depth 
perception tasks. 
Rosen et al. [2004] found that users could identify deformations in three-dimensional 
objects with more accuracy on a volumetric display than on a 2D display. However, 
given that the 2D display used did not provide any stereo or motion cues, this study does 
not provide much insight as to how the volumetric display compares to the other, more 
relevant, 3D displays that are available today. 
A study of air traffic control tasks [Van Orden and Broyles 2000] found that a volumetric 
display was not superior to other displays except in a collision avoidance task. 
Unfortunately, the study provides insufficient detail of the procedure used or insight into 
the cause of the results. For example, the users’ viewing height relative to the display – a 
factor that could have a major impact on the results – is not reported for any of the 
viewing modes. This could be one reason why the study somewhat surprisingly found 
that in a height judgment task a 2D side view resulted in the worst accuracy of all the 
displays studied, when one might expect such a view to give the best performance for 
such tasks. This study also indicates that stereo displays are not beneficial over 2D 
displays, which is surprising given the previous work that demonstrates the benefit of 
stereo displays.  
In another evaluation of volumetric displays, participants navigated a simple maze using 
a joystick [Tyler et al. 2005]. However, the comparison was to a 2D perspective display, 
and there was no clear advantage in overall performance times. Further, the maze and 


 
29 
 
task were 2D, providing little insight into the value of volumetric displays for 
understanding the 3D scenes that they were designed to display. 
2.4.5 Summary 
In this section, we have provided an overview of the evaluations which have been 
performed on the various 3D display technologies. We have seen that both motion 
parallax and stereoscopic cues can increase users’ experiences, both quantitatively and 
qualitatively. We have also seen that a system which provides only motion parallax and 
no stereopsis can perform better than a display with only stereopsis and no motion 
parallax, while a display which provides both will generally provide the best results. 
As for volumetric displays, we have presented some early work in their quantitative 
evaluation. However, our review of the literature revealed little conclusive data on the 
performance of volumetric displays in comparison to other 3D display techniques for 3D 
perception tasks. Further work in this area will be required to provide more data in this 
regard. 
2.5 
Three-Dimensional Input Devices 
We have discussed the main 3D display technologies which are being used, and the 
evaluations which have been performed on them. In the remaining sections of this 
chapter, we will discuss issues related to interacting with these displays. 
Three-dimensional displays do not just add a new dimension to visualization; they also 
present a new dimension for interaction. Although the mouse has strong benefits, which 
has made it such a successful device in the 2D realm (see [Balakrishnan et al. 1997] for a 
discussion of these properties), the input device only provides two degrees of freedom. 
There have been numerous attempts to map the 2D input of the mouse to 3D control, 
however researchers have also looked at input devices which provide three or more 
degree-of-freedom input for interacting with three-dimensional displays. In this section, 
we summarize some of these input devices. 


 
30 
 
2.5.1 Six Degree-of-Freedom Devices 
Ware and Jessome explore the use of a free-space six degree-of-freedom device for a 
three- dimensional positioning task [Ware and Jessome 1988]. They called the device a 
“bat”, as it is like a mouse which flies (Figure 2-8a). The tracking device provides six 
degrees of freedom by sensing its x, y, and z positions, as well as its roll, pitch, and yaw. 
There are a number of commercially available implementations of such six degree-of-
freedom tracking devices (e.g. www.ascension-tech.com, www.polhemus.com) and they 
have been commonly used for interacting with virtual environments, as they can be used 
to directly manipulate the position and orientation of virtual objects [Bowman and 
Hodges 1997, Hollerbach and Jacobsen 1993, Mine 1995a, Poupyrev et al. 1996]. Frolich 
and Plate [2000] augmented a bat with 3 rods representing the principal axes, which 
could be pushed and pulled to specify constrained motion along the corresponding axis. 
 
 
Figure 2-8. (a) The “bat” is an isotonic device consisting of a handle with a six degree-
of-freedom tracker. (b) The spaceball ™ is an example of a six degree-of-freedom 
isometric device. Images taken from Zhai [1995]. 
Zhai gives a detailed comparison of these isotonic devices, which can be moved freely in 
3D space, to six degree-of-freedom isometric input devices [Zhai 1995]. Isometric 
devices are mounted on a stationary surface, and sometimes termed “desktop devices” 
[Zhai 1998], and are like six degree-of-freedom joysticks. These devices are isometric as 
they all have some sort of spring loaded or elastic self-centering mechanism. Examples 
are the Spaceball™, SpaceMaster™ and SpaceMouse™ (Figure 2-8b). Zhai found that 
isotonic devices are much more appropriate for position control, while isometric devices 
are superior for rate control. 


 
31 
 
2.5.2 Roller mouse 
A drawback of using the previously discussed six degree-of-freedom input devices is that 
they can be fatiguing to users. Unlike a mouse, a user cannot simply let go of the device, 
and have it maintain its position. To address this problem, 3D pointing devices have been 
developed, which are based on the standard 2D mouse, but enable 3D interactions. The 
“roller mouse” is a standard mouse with two wheels on the front, on either side of a 
single button [Venolia 1993]. The wheels are fixed to a common axle so that they control 
a single degree-of-freedom (Figure 2-9a). The roller mouse can be used to control a 3D 
cursor, by mapping the usual mouse movements to X and Y axis movements of the 
cursor, while mapping movement of the scroll-wheel to movement of the cursor along the 
Z axis. 
 
Figure 2-9. (a) The roller mouse is a standard mouse with two wheels for an added 
degree-of-freedom. Image taken from [Venolia 1993]. (b) The Rockin’Mouse has a 
rounded bottom adding two degrees of freedom. Image taken from [Balakrishnan et al. 
1997]. 
2.5.3 Rockin’Mouse 
The Rockin’Mouse is another example of a standard mouse which has been enhanced for 
added degrees of freedom [Balakrishnan et al. 1997]. The Rockin’Mouse can move like a 
standard mouse, but its bottom is rounded, so that it can be tilted left and right, as well as 
forward and backwards, providing two additional degrees of freedom (Figure 2-9b). In a 
3D positioning task, it was shown that the Rockin’Mouse was 30% faster, when 
compared to a standard mouse.  
Because the Rockin’Mouse and roller mouse operate the depth dimension by different 
behaviours and muscle groups from those which operate the X and Y dimensions, it may 


 
32 
 
be difficult to produce simultaneous and coordinated motion, in comparison to six 
degree-of-freedom devices [Zhai 1998]. 
2.5.4 Bimanual Input 
Researchers have also looked at using two devices, one in each hand, to increase the 
number of degrees of freedom available for 3D tasks. Zeleznik et al. explore a range of 
techniques for performing 3D operations in desktop applications, using two hands to 
control two independent cursors [Zeleznik et al. 1997]. Hinckley et al. embedded a head 
viewing prop and a cutting plane tool with six degree-of-freedom trackers, for use within 
a neurosurgical application [Hinckley et al. 1998]. The cutting plane tool could act on the 
head viewing prop, allowing for bimanual input. The 3-Draw system also used two props 
for designing 3D curves. A tablet and pen, used bimanually, were both tracked in 3D 
space [Sachs et al. 1991]. Balakrishnan and Kurtenbach performed two experiments to 
evaluate bimanual input for interacting with 3D scenes [Balakrishnan and Kurtenbach 
1999]. They found that bimanual techniques were 20% faster for 3D selection, and 
strongly preferable in a free from 3D painting task. 
2.5.5 High Degree-of-Freedom Input 
By providing two devices, one for each hand, bimanual input techniques essentially 
multiply the number of degrees of freedom by two, allowing users to have more control 
of object parameters in 3D environments. Researchers have also looked at other methods 
for providing high degree-of-freedom input for 3D tasks which we now describe.  
Krueger’s VIDEOPLACE [Krueger 1991] was a deliberately informal and playful arena 
for the exploration of human interfaces with large displays. The user was in a darkened 
room with a real-time image of their silhouette displayed on a large video projection 
screen. Their entire body could be considered the input device, as the system responded 
to the user’s image and motion with interactive graphics, video effects, and sound. While 
the interactions were with 2D data imagery on the large display, such fully body, or hand 
and multi-finger tracking could also be applied to 3D interactions [Cutler et al. 1997, 
Pierce et al. 1997, Schkolne et al. 2001]. 


 
33 
 
Another interesting input device which has been used for 3D interfaces is called 
ShapeTape™. ShapeTape™ is a curve input device, which senses the bend and twist 
along its entire length. Researchers have explored the use of such a high degree-of-
freedom input device for the manipulation of curves and surfaces in 3D environments 
[Balakrishnan et al. 1999, Grossman et al. 2003]. 
2.5.6 Summary 
In this section we have provided an outline of the most common input devices used for 
interacting with 3D environments. Six degree-of-freedom devices can be used to provide 
direct manipulation of virtual objects, while enhancements to the mouse can also increase 
the number of degrees of freedom of an input device, while keeping some of the desirable 
properties of the mouse. 
For added degrees of freedom, researchers have also looked at bimanual techniques, 
where the user can directly use both hands, or use both hands to hold physical tools. We 
have also seen how specialized high degree-of-freedom input devices can be used for 
both 2D and 3D interaction. 
Because little research has been conducted on volumetric displays, no one has really 
explored what input devices should be used with these displays. It will be of interest to 
see which of these discussed input devices will be most appropriate for interacting with 
volumetric displays. We may find that the devices will need to be modified or enhanced. 
We may also find new methods of input, such as using the volumetric display’s enclosing 
surface as a touch sensitive input device.  
While the choice of input device is interesting, this will only be a step in the direction of 
developing interactive user interfaces for volumetric displays. In the following sections, 
we will see the 3D interaction techniques and applications which have been developed 
using the input devices discussed in this section.  
2.6 
Three-Dimensional Interaction Techniques 
Along with finding appropriate input devices for volumetric displays, we will be 
interested in finding effective interaction techniques for such displays. In exploring this 
topic, the vast literature on interaction within 3D user interfaces and virtual reality 


 
34 
 
environments is clearly relevant. A number of researchers have proposed and agreed 
upon four fundamental tasks for 3D interactions: navigation (or travel), selection, 
manipulation, and system control [Bowman and Hodges 1999, Mine 1995a, van Dam et 
al. 2000]. In this section we summarize the interactions techniques which have been 
developed in each of these categories. 
2.6.1 Navigation  
Navigation refers to the task of positioning and orienting the viewpoint within a 3D 
environment. Because the environment size displayed within a volumetric display is 
limited to the size of its enclosure, users will be able to effectively control their viewpoint 
orientation and position by simply changing the position of their head. As a result, the 
navigation techniques developed for vast large virtual environments, where changing the 
viewpoint position may require significant travel distances, will be less applicable, in 
comparison to the other three fundamental tasks, so we online give a brief outline of them 
here. 
2.6.1.1 Cinematic Camera Metaphor 
In non-immersive 3D environments, such as 3D graphics and animation programs, mouse 
movements coupled with modifier keys are generally used to manipulate the position of 
the virtual camera, which in turn controls the user’s viewpoint of the scene. This is 
generally termed as a cinematic camera metaphor, since the user can tumble, track and 
dolly a viewpoint [Burtnyk et al. 2002]. The Unicam allows users to manipulate the 
position of the 3D camera using a mouse and only a single button, coupled with different 
gestures for invoking camera functionality [Zeleznik and Forsberg 1999]. The StyleCam 
allows authors to significantly tailor the best possible camera positions and paths to be 
used by a viewer [Burtnyk et al. 2002]. 
Various metaphors for viewpoint motion and control in 3D environments, which use 
higher degree-of-freedom input, have also been proposed. Ware and Osborne explore 3 
such metaphors which were implemented using a six degree-of-freedom input device 
which we now discuss [Ware and Osborne 1990].  


 
35 
 
2.6.1.2 Eyeball-in-Hand Metaphor 
With the eyeball-in-hand technique, the position of the input device is directly mapped to 
the position of the virtual camera, or eyeball, within the 3D scene. The viewpoint of this 
eyeball is then projected on the viewing display. They explored both an absolute mapping 
between the input device and eyeball position, and a relative mapping, in which the 
viewpoint only changed when a button was depressed. While the relative mapping 
allowed for ratcheting, it destroyed the user’s mental model of a fixed invisible scene, 
and so users found it confusing. The chameleon discussed in Section 2.2.6 is an example 
of a display device which provides eyeball in hand navigation [Fitzmaurice 1993]. 
2.6.1.3 Scene-in-Hand Metaphor 
With the scene-in-hand metaphor, the three-dimensional world is moved in 
correspondence with the six degree-of-freedom input device. If the device is rotated 
clockwise, then the scene will also rotate clockwise. Large movements can be 
accomplished by ratcheting, using a button as a clutch. It was found that the scene-in-
hand metaphor was useful for changing the viewpoint in a hierarchal scene. Stoakley et 
al. designed an extension of the scene-in-hand metaphor, which makes use of a “World-
in-Miniature” representation of the scene [Stoakley et al. 1995]. With this technique, 
navigation can be accomplished by manipulating a hand-held miniature copy of the 
virtual environment. 
2.6.1.4 Flying Vehicle Metaphor 
The other technique proposed is the flying vehicle metaphor. With this technique the 
scene is perceived from the position and orientation of the vehicle. The input device is 
used to control the spatial and angular velocity of the vehicle, allowing it to be moved 
throughout the scene. This metaphor is commonly used in 3D games, in which the 
“player position” can be thought of as the vehicle. The user controls the position and 
orientation of the viewpoint to move throughout the environment. This technique has 
been enhanced in various ways, such as allowing for rapid and controlled movement 
[Mackinlay et al. 1990]. 


 
36 
 
2.6.2 Selection 
Selection is a fundamental aspect of any interactive 3D system, as a user must be able to 
specify an object in the virtual world, so they can then manipulate or interact with it. 
Techniques for selection have been thoroughly developed within the VR literature. These 
techniques will be of high relevance to the design of interactive applications for 
volumetric displays. We now give a review of selection techniques used in 3D 
environments.  
2.6.2.1 Image Plane Selection 
When 3D environments are displayed on desktop screens, the monitor defines a 2D 
image plane, which displays the 3D scene. The application projects the objects in the 3D 
environment onto the image plane for display to the user. The user can select objects in 
the 3D scene using the image plane by positioning the mouse cursor over the object’s 
projection on the image plane. In essence the cursor defines a ray perpendicular to the 
surface of the image plane, and clicking selects the first object which the ray intersects 
[Pierce et al. 1997]. This technique does not directly extend to 3D displays, as there is not 
always a well defined image plane. Ware and Lowther extend the technique for a 
stereoscopic display by defining the image plane as the viewpoint from only a single eye 
[Ware and Lowther 1997]. This “one-eyed cursor” was found to be an effective selection 
technique for 3D environments. 
2.6.2.2 Ray Cursor 
For selection within immersive 3D environments, Liang and Green [1994] implemented a 
ray firing selection mechanism that they called “laser gun” selection. A ray is emitted 
from the user’s hand, so the user has control over the start point and orientation of the 
ray, much like a physical laser pointer (Figure 2-10a). The first object it intersected with 
would be selected. This technique allowed users to select both near and distant objects; 
however, they found it was difficult to select small and distant objects due to the angular 
accuracy required for such targets. To alleviate this problem, they created a mechanism 
called “spotlight selection”. Instead of emitting a ray, the user emits a cone with its apex 


 
37 
 
at the user’s hand (Figure 2-10b). This allows a certain level of error to be 
accommodated.   
 
Figure 2-10. (a) Ray cursor selection. Image taken from Mine [1995a]. (b) Spotlight 
selection. Image taken from Liang and Green [1994]. 
A problem with the ray casting selection is that the ray can intersect multiple objects. 
This problem is magnified when a cone is used instead of a ray. Liang and Green 
developed a metric to decide which object would be selected if multiple targets were 
within the spotlight, based on the distance from the targets to the apex and central axis of 
the cone [Liang and Green 1994]. Hinckley suggests that the ray casting technique could 
be augmented with a mechanism for cycling through the set of all ray-object intersection 
points [Hinckley et al. 1994].  
2.6.2.3 Occlusion Selection 
Occlusion selection is an extension of the image plane selection used on a desktop to 
immersive 3D environments [Mine et al. 1997]. With this technique, users select objects 
that visually lie behind a hand-attached cursor. Essentially this is a ray casting technique, 
where the ray is defined by the vector which joins the user’s eye and hand. This 
technique has been explored in a couple of different implementations. 
Forsberg created aperture based selection where a cone is cast from the users eye and 
goes through the users finger, and the distance between the finger and the eye controls the 
angle of diversion of the cone [Forsberg et al. 1996]. Because orientation information is 
not used to define the direction of the ray, they used it for disambiguation when the ray 
intersected multiple objects. When the ray intersected more than one object, the object 
whose orientation was most closely matched by the input device was selected. 


 
38 
 
 
Figure 2-11. (a) The Head Crusher technique. Objects which lie between the user’s 
finger and thumb can be selected. (b) The Sticky Finger technique. Objects occluded by 
the tip of the index finger can be selected. Images taken from Pierce et al. [1997]. 
Pierce et al. explored several different image plane interaction techniques which uses 
occlusion selection [Pierce et al. 1997]. With the Head Crusher technique, objects which 
lie between the user’s index finger and thumb are selected (Figure 2-11a). The Sticky 
Finger technique selects objects by occluding them with the tip of the index finger 
(Figure 2-11b). The Lifting Palm technique allows users to select objects by flattening 
their hand and positioning their palm so that it appears to be underneath the object. The 
last technique was Framing Hands, in which both hands are used to define a bounding 
box around the object of interest, using the thumbs and index finger. 
2.6.2.4 3D Cursor 
A more direct method of interaction, using a 3D cursor which specifies X, Y and Z 
coordinates has also been suggested [Hinckley et al. 1994, Mine 1995a, Poupyrev et al. 
1996]. Mine distinguishes between local and action-at-a-distance interactions in a virtual 
world [Mine 1995a]. He states that in local interactions, a direct mapping from the users 
hand to a 3D cursor should be used to select an object, while selection of objects at a 
distance, laser beam or spotlight selection could be used. He also suggests that a “virtual 
cursor or drone” could be moved by the user through the environment until it reaches a 
distance target for selection.  


 
39 
 
 
Figure 2-12. The silk cursor is a volume cursor with a semi-transparent lining. Image 
taken from [Zhai et al. 1994]. 
2.6.2.5 Silk Cursor 
The Silk Cursor [Zhai et al. 1994] is a 3D volume cursor, the extension of 2D area 
cursors [Kabbash and Buxton 1995]. The silk cursor provides two advantages over a 
standard point cursor for selection tasks. Firstly, as with 2D area cursors, the effective 
activation area of a potential target is increased. Secondly, the rectangular shaped silk 
cursor is lined with a semi-transparent surface, creating a partial occlusion effect (Figure 
2-12). This allows users to tell when a target is in front, inside, and behind the silk cursor. 
In a controlled experiment, the silk cursor was found to be beneficial in both monoscopic 
and stereoscopic displays. 
2.6.2.6 Go – Go Technique 
Poupyrev [1996] introduced the go-go selection technique to enhance 3D cursor selection 
for objects at a distance. The technique uses a metaphor of growing a user’s arm 
interactively, with a non-linear mapping for selecting distant objects. When the user 
operates on nearby objects, the movement of the virtual hand matches movement of the 
real hand. To reach remote objects the user simply extends the hand further than 2/3 the 
length of their arm. The mapping becomes non-linear and the virtual arm grows. Unlike a 
standard 3D cursor, in which the range of selection is limited to arm’s length, the go-go 
technique allows for selection of both nearby objects and those at a distance.  


 
40 
 
2.6.2.7 Evaluation of Selection Techniques 
In a formal experiment, Ware and Lowther evaluated the one-eyed cursor, which is 
essentially a ray cursor, where the vector of the ray is always perpendicular to the surface 
of the screen [Ware and Lowther 1997]. They found it to be superior to a standard 3D 
cursor, as with the one eyed cursor, only two of the three dimensions of a goal target need 
to be defined. Bowman collected quantitative data to compare ray casting, occlusion 
selection and the go - go technique [Bowman et al. 1999]. The go-go technique was 
found to be significantly slower, as it required the positioning of the hand in 3D space. 
Although there was no significant difference in movement time between ray casting and 
occlusion selection, occlusion selection caused higher levels of arm strain. Ray casting 
was more comfortable as users could “shoot from the hip”. To date there has not been a 
comparison of ray cursor with 3D volume cursors, such as the silk cursor, but area 
cursors have been shown to be advantageous in 2D environments [Worden et al. 1997]. 
While these results seem to indicate that ray casting techniques should be used for 
selection within volumetric displays, there are a couple of points which require further 
exploring. Firstly, the go-go technique was found to benefit from shortened target 
distances [Bowman et al. 1999]. Within a volumetric display, the distances will be 
limited by the physical enclosure, so 3D point techniques may not fare as poorly. 
Secondly, ray cursor selection breaks down in dense target environments, and to date 
there have not been any formal evaluations of techniques for disambiguating between 
multiple intersected targets. It may be the case that such a disambiguation mechanism 
will introduce an overhead cost which mitigates the advantages of ray cursors. 
2.6.3 Manipulation 
Once objects are selected, it is important that users can manipulate them in an interactive 
3D application. We now discuss the techniques which have been developed to manipulate 
objects in 3D environments. 
2.6.3.1 Direct Six Degree-of-Freedom Manipulation 
One of the most common forms of manipulation in virtual environments is to map the 
movement of a six degree-of-freedom input device to the movement of a selected object 


 
41 
 
[Bowman and Hodges 1997, Hollerbach and Jacobsen 1993, Mine 1995a, Poupyrev et al. 
1996]. This allows the object of interest to be rotated and translated as desired.  
Techniques have also been proposed to allow for direct manipulation with objects which 
are at a distance. In the ISAAC system, users could first select an object with a ray cursor 
and then manipulate the object with a direct mapping from the hand [Mine 1995b]. A 
similar technique called HOMER (Hand-Centered Object Manipulation Extending Ray-
Casting) was suggested by Bowman and Hodges, where the object is selected with a ray 
cursor and then a virtual hand jumps to the object position, and the object becomes 
attached to the hand [Bowman and Hodges 1997]. The World in Miniature interface 
allows users to quickly select and manipulate an object positioned anywhere in the 
environment by grabbing the miniature object which is in the palm of their hand 
[Stoakley et al. 1995]. They can orient the miniature environment by rotating the hand 
that holds it, allowing them to select objects that may be obscured from their current 
point of view. Once an object is selected, it can be positioned and oriented in the 
miniature world with a one-to-one mapping from the hand, or also at a greater scale for 
more fine grain control.  
2.6.3.2 Voodoo Dolls 
Voodoo dolls extend these direct manipulation techniques by allowing bimanual 
interactions [Pierce et al. 1999b]. With this technique, each hand can hold a voodoo doll, 
a miniature copy of an object in the virtual environment (Figure 2-13). The dolls are 
created by using occlusion selection with either hand, and held with a pinch. Dolls can be 
passed from one hand to the other, and dropped by releasing the pinch. The object held in 
the dominant hand can be positioned and oriented relative to the object being held in the 
non-dominant hand. This follows Guiard’s bimanual theory where the dominant hand 
works in the reference frame set by the non-dominant hand [Guiard 1987]. To move a 
lamp onto a table, for example, the user creates a voodoo doll of the lamp in the dominant 
hand and of the table in the non dominant hand. The user then places the miniature copy 
of the lamp on top of the table. In the actual virtual scene, the lamp will move on top of 
the table, which remains stationary. In a follow-up study, it was found that the Voodoo 


 
42 
 
Dolls technique allowed users to position and orient objects more precisely than the 
HOMER technique [Pierce and Pausch 2002]. 
 
Figure 2-13. Voodoo dolls. The dominant hand manipulates a pin relative to the position 
of the toy soldier held by the non-dominant hand using hand-held miniature copies. 
Image taken from [Pierce et al. 1999b]. 
2.6.3.3 Three-Dimensional Widgets 
Conner et al. explored manipulations of objects which diverged from the stranded direct 
manipulation techniques described above, using three-dimensional widgets [Conner et al. 
1992]. Using the widgets allow for manipulations which are difficult or impossible to 
accomplish using a direct mapping from the physical hand, and also allow for constrained 
manipulations, such as rotating an object about a single axis (Figure 2-14). They describe 
several widgets which allow for different types of manipulations. For example a virtual 
sphere can be used to rotate an object. The mouse clicks and drags on the sphere, and the 
2D mouse coordinates are mapped to points on the surface of the sphere, causing the 
object to rotate. Object handles are 3D widgets that constrain the manipulations. For 
example, handles can be available to scale, rotate, or translate an object along any of the 
major axes. Many current applications (e.g. MAYA™, 3D StudioMax™) for 3D 
modeling and animation make extensive use of such 3D widgets since they can be easily 
operated with status-quo mouse & keyboards input. 


 
43 
 
 
Figure 2-14. A three-dimensional widget. Object handles can be manipulated to perform 
a constrained rotation about a single axis. Image taken from Conner et al. [1992].  
2.6.3.4 Gestural Manipulation 
In Charade freehand gestures were used to manipulate 2-dimensional computerized 
objects in an augmented reality system [Baudel and Beaudouin-Lafon 1993]. Although 
the gestural interaction was mapped to the manipulation of two-dimensional objects, this 
could be a valuable method for manipulating three-dimensional objects. Since this 
foundational work, gestural interfaces have been developed for pen based devices 
[Zeleznik and Miller 2005], large displays [Vogel and Balakrishnan 2004], and tabletop 
displays [Wu and Balakrishnan 2003], and could be a valuable method for interaction 
with volumetric displays.  
2.6.4 System Control 
System control is the set of commands that the user gives to accomplish work within the 
application. For example, the user may wish to delete an object, or save a model which 
they are manipulating. In a standard desktop application, system control is achieved 
through toolbars and menus. Because these widgets are generally 2D, there are interesting 
challenges involved with integrating them into a 3D environment. 
In Mine [1995b], a 2D menu was embedded in the virtual environment. The menu which 
was developed floats in 3D space and includes various widgets such as radio buttons, 
sliders, and dials. The user interacts with the menu using a ray cursor, so that the user 
does not have to make large reaching movements. In the JDCAD system [Liang and 
Green 1994] a ring menu was used for item selection, where the items were arranged 


