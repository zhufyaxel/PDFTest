## 2. Background Literature

### 2.1 Introduction

In Section 1.2, we discussed the new affordances presented by volumetric displays. These affordances raise new human factors issues and interaction challenges. Once these new topics are better understood, applications, and the user interfaces and interaction techniques which they are made up of, can be appropriately designed. In this chapter, we review the previous research which will help guide our investigation into making volumetric displays an interactive platform.

The chapter will be structured as follows. In Section 2.2 we present an overview of existing 3D display technologies, followed by a description of existing volumetric display technology in Section 2.3. Section 2.4 looks at methods for evaluating the viewing experience in these various 3D displays, which can be extended to the study of volumetric displays. In Section 2.5, we provide an overview of the input devices used for interacting with 3D environments. In Section 2.6, we look at some of the basic interaction techniques existing in the virtual reality and 3D interaction communities, which will provide insights into the development of interaction techniques for volumetric displays. In Section 2.7, we look at work which integrates these interaction techniques into 3D applications. Section 2.8 focuses on collaborative applications, which will aid in the development of interaction techniques for volumetric displays, under a multiple user

## 2.2 Three-Dimensional Display Technology

In this section we provide a background on the types of display technology which have been used to present three-dimensional data. These display techniques all utilize various depth cues which have been identified in psychological research on human perception. We now discuss the display techniques, and the associated cues which these displays provide.

### 2.2.1 Perspective Displays

A basic method for displaying three-dimensional environments, which is commonly used in 3D graphics, is to use a standard workstation monitor, using a perspective projection. Perspective displays utilize perspective and relative size cues, in which objects further away, produce smaller retinal images than closer objects. Perspective cues are particularly effective when parallel lines are displayed within the scene.

Another cue which is utilized in perspective displays is motion parallax, also referred to as the kinetic depth effect. With this cue, a sensation of depth is produced when an object moves in space relative to an observer. Therefore, interfaces should provide a mechanism for moving the viewpoint in a 3D scene.

By utilizing these two powerful depth cues, perspective displays are effective tools for viewing and interacting with three-dimensional data, and are still the most commonly employed display type for tasks such as 3D graphics design and animation.

### 2.2.2 Non-Immersive Stereoscopic Displays

An important depth cue which cannot be provided by a standard workstation monitor is stereopsis. This depth cue is produced from the binocular disparity when viewing 3D objects in natural environments. It can be particularly strong when the perceived objects are close to the viewer. To provide stereopsis, a system simply needs to

There are a number of display technologies which can provide stereopsis on a flat screen. Common examples of stereoscopic displays are polarized glasses which passively block certain light from each eye and liquid-crystal time-multiplexed shuttering glasses which actively block light from each eye. Autostereoscopic displays are another class of stereoscopic displays, which are glasses free systems that project multiple images for each eye in specific locations in space.

### 2.2.3 Semi Immersive Fish Tank Displays

The display technologies discussed so far are generally considered to be non-immersive, as there is a clear distinction between the physical and virtual environments. Fish tank displays increase the level of immersion by coupling the viewpoint of the virtual scene, with the physical location of the user’s head, so that the appropriate perspective is always presented. Generally the user’s head position is tracked, and the location of the user’s eyes is estimated by offsetting them by a constant distance from the user’s head. The viewpoint of the virtual scene is then updated appropriately.

can be perceived monocularly, coupled to a single eye position, or binocularly, if combined with one of the stereoscopic technologies discussed above. Because the scene is still projected on a 2D display, fish tank displays are considered to be semi-immersive. Generally the viewing volume of these displays is roughly equivalent to the inside of the monitor, so viewing them is similar to looking into a fish tank. The head coupled viewpoint with fish tank displays provides motion parallax cues, without requiring users to explicitly manipulate the camera position.

## 2.2.4 Head-Mounted Displays

More immersive forms of displays, typically associated with the field of virtual reality, which provide stereopsis and motion parallax through head coupled viewpoints, have also been developed. A common form is a head mounted display, which use some sort of helmet or goggles to provide a stereo pair of displays directly in front of each eye. Such displays provide the widest possible field of view at high quality. Head mounted displays can provide the user with a realistic 3D experience, but a significant problem is that the user’s eyes are covered by the display. The result is a lost context of the user’s physical surrounding and possible collaborators.

A solution to this problem is to allow users to see the physical world, such as their hands, tools, and other people, while wearing the display. This can be accomplished by mounting video cameras onto the displays, and incorporating their images into the virtual world which the user sees. The cameras act as an extra set of eyes for the user, projecting a view of the physical world onto the computer generated view of the virtual world. This is similar to providing the user with a heads up display, using an optical see-though display. This approach is generally known as augmented reality, as the systems augments the physical world with additional virtual imagery.

## 2.2.5 Cave

Another interesting form of an immersive 3D display is known as a Cave. A Cave is room where the walls, floor, and ceiling, act as the display. To provide a seamless view of the virtual scene, each of the displays must be tiled together at the edges where they intersect. The projected surfaces of the Cave are typically in stereo, with the user wearing a pair of glasses. Furthermore, the head is tracked so that the appropriate perspective is always presented to the user. A benefit of Caves over head mounted displays is that users can still see and have a maintained context of their physical surroundings. A number of other systems similar to Caves have also been developed, which vary in size, and also the number of surfaces which are projected onto. One example is large scale projection displays, such as the ImmersaDesk.

## 2.2.6 Chameleon

A less common technology for presenting 3D environments is the Chameleon system. With the Chameleon system, perspective images of three-dimensional scenes appear on a small display held in the palm of the hand. As with fish tank and head mounted displays the perspective view is continuously updated. However, the perspective viewpoint is determined by the position of the display, rather than being coupled with the head of the user.

The Chameleon approach is almost like using a magnifying glass which looks into a virtual scene, rather than the physical world. While the display does not provide the full immersive feeling or viewing angle of a cave or head mounted display, users can easily browse the scene by moving the lightweight display.

There have been other implementations of Chameleon displays. The boom chameleon consists of a flat-panel display mounted on a tracked mechanical boom. The armature of the boom is carefully balanced to allow the display to float weightlessly in space. The display acts as a physical window into 3D virtual environments, through which a one-to-one mapping between real and virtual space is preserved.

Chameleon systems can also have the ability to support augmented reality. Location tracking could be used to sense the context of its environment. For example, bringing the display close to a map could give additional information about the region that it was close to. Further augmentations included adding video cameras, allowing computer-generated information to be superimposed over a view of the physical world.

## 2.2.7 Summary

We have presented a variety of display technologies for three-dimensional data. The displays provide different levels of immersion to the users ranging from non immersive perspective displays to fully immersive head mounted displays. Each display has its own unique properties which afford different methods of interaction. In the next section, we will discuss various volumetric display technologies. By examining and comparing the properties of volumetric displays to the technologies discussed in this section, we will gain an understanding of what interaction techniques will transfer well to volumetric displays, and what interaction techniques will require modifications or enhancements.

## 2.3 Volumetric Displays

Unlike the other display technologies previously discussed volumetric displays present imagery in true 3D space. The viewing space is divided up into 3D pixels, called voxels, which illuminate visible light from the regions which they appear. Because light is emitted in true 3D space, depth cues such as motion parallax and stereopsis will always be present without the need for supplementary hardware. From a technological standpoint, there are some interesting differences between the various implementations of volumetric displays. While they all generate true 3D images, the underlying technology of the various displays vary greatly in both concept and design. From an interaction standpoint, however, these differences will not be so critical, as all of these displays pose the same qualities which we have discussed in Section 1.2. We now provide an overview of the basic classes of 3D volumetric displays.

### 2.3.1 Oscillating Swept Volumetric Displays

A common method for presenting volumetric imagery is to use a two-dimensional image which periodically sweeps out a three-dimensional volume of space. When the space is swept out cyclically at a frequency higher than what the eye can resolve, a spatial image is formed through the persistence of vision. We now discuss the class of displays in which volumes are swept out by oscillating screens.

An early implementation uses a vibrating CRT where the images which output to the screen are synchronized within each oscillation cycle, so that each image appears at the

appropriate position of the tube. Because of the high mass of the tube, it would be difficult to obtain the desirable rapid acceleration and deceleration at each end of its oscillation.

A more practical suggestion is to have the phosphorous screen within the CRT oscillate rather than the entire CRT itself. The screen is mounted within a vacuum tube behind a transparent viewing globe, and oscillates with a piston like motion. An electron gun illuminates the screen from the rear.

A variation of the oscillating screen, is to have an oscillating mirror from which a CRT image is viewed. The mirror moves such that the visual path length is swept periodically, and the CRT image apparently sweeps out the volume. The drawback of this scheme is that the viewing angle is limited to the reflective surface coverage.

Because of the inertial forces required for oscillating screens, this class of displays generally has problems with vibration and noise. The accelerations involved also limit the oscillation frequency, causing considerable flicker of the displayed images. A more promising approach is a rotating swept display, which we now discuss.

## Rotating Swept Volumetric Displays

One of the earliest implementations of rotating swept volumetric displays was developed by the ITT Laboratories in 1960, which consisted of a cathode ray tube whose light is optically transferred to a translucent rotating screen within a glass cylinder. The motor driven panel turned at approximately 20 revolutions per

Another implementation was presented in 1963, where a phosphor-coated screen rotated in a vacuum, with a controlled electron beam striking its surface. The 3D images were presented by having the electron beam project on the screen as it passes through the desired location of space [Ketchepel 1963].

The rotating screens can also be actively emissive, instead of having imagery projected onto them. Berlin proposed using a 2D matrix of light emitting diodes (LEDs) with the light electronics rotating to sweep out a 3D volume [Budinger 1984]. In this implementation, the display resolution is a function of the number and density of LEDs, the speed of rotation, and the rate at which LEDs can be pulsed.

The above rotating displays are swept out by flat surfaces. However in another class of volumetric displays, the viewing volume is swept out by a curved surface. The shapes of such displays can be spherical spirals or helical.

Recently, rotating swept displays have been developed to use light fields to display different imagery to each viewing angle. The benefit of such displays is that they can produce viewpoint dependent rendering effects, such as shading, and hidden surface removal. However, such displays are not truly volumetric, as the perceived location of a voxel might not be the actual location where it is emitted.

Rotating volumetric displays are one of the more promising technologies to date, with current implementations being available commercially. This is the technology we use in this thesis.

### 2.3.3 Static Volumetric Displays

Static volumetric displays are defined as displays which generate light in true 3D space, without the need for mechanical motion. With this technique, emissive voxels are provided at a large number of locations in a static setup, without the use of oscillating or rotating mirrors or screens. This can be accomplished by exciting a plasma filled medium within a display volume to produce a glow at a single point.

A proof-of-concept of this displays was implemented in 1971, where two faint spots of light were generated inside a transparent crystal of erbium-doped calcium fluoride, with the use of filtered xenon lamps as excitation sources.

Based on this early work, Downing et al. presented a three-color static volumetric display with improved material using high powered laser diodes. The laser beams intersect inside a transparent volume, which consists of a rare earth-doped heavy metal fluoride glass. Red, green, and blue voxels can be illuminated by sequential two-step resonant absorption. Imagery can be produced in 3D by scanning the point of intersection of the lasers in various 3D locations of the volume. The demonstrated work was implemented in a prototype sugar-cube sized volume.

##

In another implementation, a gaseous volume was enclosed within a sealed glass container. Two diode lasers were intersected in Rubidium vapor. The setup requires Rubidium to be heated within a vacuum, making it difficult to design for larger scale display volumes.

A more recent implementation used a pulsed laser to create glowing points of plasma in midair. This is one of the few volumetric displays which does not require a physical enclosure. However, the points of plasma are at an extreme temperature, so users are still unable to reach in and interact with the displayed imagery.

Although the current level of quality for static volumetric displays is not up to par with the current generation of rotating swept volumetric displays, their desirable properties make for a promising alternative which researchers continue to develop.

### 2.3.4 Summary

This section has outlined the most common technological implementations for volumetric displays. From an interaction standpoint, these technological differences may not seem so interesting; however, there are some interesting observations to be made. Most importantly, all of the discussed technologies share the properties which we have discussed in Section 1.2.

What is not common among the displays discussed in this section is the shape and size of the physical enclosure. For example, we have seen hemispherical domes, as well as

## 2.4 Evaluation of Three-Dimensional Viewing Modes

In the previous two sections we have discussed the various display technologies for viewing 3D data. With all the available types of 3D display technologies, it is important for designers to know which will be the most appropriate device for their task at hand. Most relevant to our work, we will want to determine under what condition volumetric displays will prove to be beneficial. Researchers have tried to address this issue by conducting formal evaluations to provide comparisons of different viewing modes. We now provide a summary of such research, and an overview of the important results obtained to date.

### 2.4.1 Subjective Impressions of Three-Dimensional Viewing Modes

In an early study, Two different 3D scenes were presented to users. One consisted of a sphere with its shadow cast on a ground plane. The other consisted of a bent piece of tube representing mental rotation for 3D objects. Once a scene was presented, subjects could toggle between two presentation modes until they could decide which contributed more to the perception of the 3D space.

The experiment consisted of the following 5 conditions: perspective, stereo, head coupled monocular, head coupled binocular, head coupled with stereo. In the non-stereo conditions, the same scene was presented to both eyes. In the binocular condition, the viewpoint was between the eyes, while in the monocular condition, the viewpoint was correct for the right eye, and the subjects were asked to close their left eye.

## Viewpoint Conditions, The Perspective View

For each trial of the experiment, subjects were given one of the 10 pairwise comparisons of the 5 viewing conditions. They toggled between the viewing conditions until they made their final selection on which was “best”. 

The results showed that users rarely preferred stereo without head coupling over head coupling without stereo. More frequently, users chose head coupling without stereo over head coupling with stereo 68% of the time, attributing this preference to the ghosting effect in the stereo conditions due to imperfect phosphor decay causing crosstalk between the left and right images.

The results supported the use of head coupled stereo viewing, with all subjects expressing their willingness to use it for object visualization if it were available.

## 2.4.2 Empirical Evaluation of Stereo and Motion Cues

Subjective evaluations of three-dimensional viewing modes indicate that providing stereo or motion cues improves the user’s perception of a three-dimensional scene. Quantitative measures have been attempted to determine the exact benefit of moving from 2D to 3D representations, though results depend on the specific tasks involved.

It has been demonstrated that stereoscopy enhances performance in detecting paths in a tree structure. Further reductions in errors were found when scene rotation was incorporated, which was system-controlled in the studies.

et al. [1993] found similar results when the motion was controlled by the user, in the form of a head coupled perspective view.

In one of the more recent studies, Ware and Franck [1996] evaluated nine different types of viewing modes for a path tracing task. Randomly generated graphs were presented, and users were required to determine if two highlighted nodes were connected by a path of length two. The viewing modes consisted of different combinations of perspective, stereo, and motion parallax cues, where they tested both hand, head, a system controlled rotation of the scene.

It was found that the stereo viewing mode without motion was significantly worse than all three tested stereo modes with motion, including system controlled rotation, hand coupled rotation, and head coupled rotation. Of the three viewing modes which combined stereo and motion, there were no significant differences, showing that the motion parallax cues were important, but it did not matter how they were provided.

In the virtual reality literature, researchers have attempted to quantify the benefits of immersion within virtual environments. Barfield et al. found that head tracking significantly improves users’ sense of presence. In a collaborative task, where two users had to maneuver a ring through a 3D object, Narayan et al. found that stereo was extremely important, while head tracking did not provide significant performance gains.

### 2.4.3 Qualitative Evaluation of Volumetric Displays

Because volumetric displays are still in the developmental stages, little evaluation has been conducted to provide a quantitative comparison to other 3D viewing modes. However, qualitative benefits associated with their use have been reported. Balakrishnan et al. provide a good summary of these benefits.

The fundamental difference is that volumetric displays generate images in true 3D space, so imagery can be viewed within the displays, just as one would view real physical objects. The human viewer can use their natural physiological mechanisms for depth perception, such as true motion parallax and stereopsis through eye convergence and accommodation, without the need for supplementary hardware. Furthermore, the

## Quantitative Evaluation of Volumetric Displays

To date, only a few studies have been reported, and none provide conclusive evidence as to how volumetric displays compare to other existing 3D display technologies for depth perception tasks.

Rosen et al. found that users could identify deformations in three-dimensional objects with more accuracy on a volumetric display than on a 2D display. However, given that the 2D display used did not provide any stereo or motion cues, this study does not provide much insight as to how the volumetric display compares to the other, more relevant, 3D displays that are available today.

A study of air traffic control tasks found that a volumetric display was not superior to other displays except in a collision avoidance task. Unfortunately, the study provides insufficient detail of the procedure used or insight into the cause of the results. For example, the users’ viewing height relative to the display – a factor that could have a major impact on the results – is not reported for any of the viewing modes. This could be one reason why the study somewhat surprisingly found that in a height judgment task a 2D side view resulted in the worst accuracy of all the displays studied, when one might expect such a view to give the best performance for such tasks. This study also indicates that stereo displays are not beneficial over 2D displays, which is surprising given the previous work that demonstrates the benefit of stereo displays.

In another evaluation of volumetric displays, participants navigated a simple maze using a joystick. However, the comparison was to a 2D perspective display, and there was no clear advantage in overall performance times. Further, the maze and

## 2.4.5 Summary

In this section, we have provided an overview of the evaluations which have been performed on the various 3D display technologies. We have seen that both motion parallax and stereoscopic cues can increase users’ experiences, both quantitatively and qualitatively. We have also seen that a system which provides only motion parallax and no stereopsis can perform better than a display with only stereopsis and no motion parallax, while a display which provides both will generally provide the best results.

As for volumetric displays, we have presented some early work in their quantitative evaluation. However, our review of the literature revealed little conclusive data on the performance of volumetric displays in comparison to other 3D display techniques for 3D perception tasks. Further work in this area will be required to provide more data in this regard.

## 2.5 Three-Dimensional Input Devices

We have discussed the main 3D display technologies which are being used, and the evaluations which have been performed on them. In the remaining sections of this chapter, we will discuss issues related to interacting with these displays.

Three-dimensional displays do not just add a new dimension to visualization; they also present a new dimension for interaction. Although the mouse has strong benefits, which has made it such a successful device in the 2D realm, the input device only provides two degrees of freedom. There have been numerous attempts to map the 2D input of the mouse to 3D control, however researchers have also looked at input devices which provide three or more degree-of-freedom input for interacting with three-dimensional displays. In this section, we summarize some of these input devices.

## 2.5.1 Six Degree-of-Freedom Devices

Ware and Jessome explore the use of a free-space six degree-of-freedom device for a three-dimensional positioning task. They called the device a “bat”, as it is like a mouse which flies. The tracking device provides six degrees of freedom by sensing its x, y, and z positions, as well as its roll, pitch, and yaw. There are a number of commercially available implementations of such six degree-of-freedom tracking devices and they have been commonly used for interacting with virtual environments, as they can be used to directly manipulate the position and orientation of virtual objects. Frolich and Plate augmented a bat with 3 rods representing the principal axes, which could be pushed and pulled to specify constrained motion along the corresponding axis.

Zhai gives a detailed comparison of these isotonic devices, which can be moved freely in 3D space, to six degree-of-freedom isometric input devices. Isometric devices are mounted on a stationary surface, and sometimes termed “desktop devices”, and are like six degree-of-freedom joysticks. These devices are isometric as they all have some sort of spring loaded or elastic self-centering mechanism. Examples are the Spaceball™, SpaceMaster™ and SpaceMouse™. Zhai found that isotonic devices are much more appropriate for position control, while isometric devices are superior for rate control.

## 2.5.2 Roller mouse

A drawback of using the previously discussed six degree-of-freedom input devices is that they can be fatiguing to users. Unlike a mouse, a user cannot simply let go of the device, and have it maintain its position. To address this problem, 3D pointing devices have been developed, which are based on the standard 2D mouse, but enable 3D interactions. The “roller mouse” is a standard mouse with two wheels on the front, on either side of a single button. The wheels are fixed to a common axle so that they control a single degree-of-freedom. The roller mouse can be used to control a 3D cursor, by mapping the usual mouse movements to X and Y axis movements of the cursor, while mapping movement of the scroll-wheel to movement of the cursor along the Z axis.

## 2.5.3 Rockin’Mouse

The Rockin’Mouse is another example of a standard mouse which has been enhanced for added degrees of freedom. The Rockin’Mouse can move like a standard mouse, but its bottom is rounded, so that it can be tilted left and right, as well as forward and backwards, providing two additional degrees of freedom. In a 3D positioning task, it was shown that the Rockin’Mouse was 30% faster, when compared to a standard mouse.

Because the Rockin’Mouse and roller mouse operate the depth dimension by different behaviours and muscle groups from those which operate the X and Y dimensions, it may

## 2.5.4 Bimanual Input

Researchers have also looked at using two devices, one in each hand, to increase the number of degrees of freedom available for 3D tasks. Zeleznik et al. explore a range of techniques for performing 3D operations in desktop applications, using two hands to control two independent cursors. Hinckley et al. embedded a head viewing prop and a cutting plane tool with six degree-of-freedom trackers, for use within a neurosurgical application. The cutting plane tool could act on the head viewing prop, allowing for bimanual input. The 3-Draw system also used two props for designing 3D curves. A tablet and pen, used bimanually, were both tracked in 3D space. Balakrishnan and Kurtenbach performed two experiments to evaluate bimanual input for interacting with 3D scenes. They found that bimanual techniques were 20% faster for 3D selection, and strongly preferable in a free from 3D painting task.

## 2.5.5 High Degree-of-Freedom Input

By providing two devices, one for each hand, bimanual input techniques essentially multiply the number of degrees of freedom by two, allowing users to have more control of object parameters in 3D environments. Researchers have also looked at other methods for providing high degree-of-freedom input for 3D tasks which we now describe.

Krueger’s VIDEOPLACE was a deliberately informal and playful arena for the exploration of human interfaces with large displays. The user was in a darkened room with a real-time image of their silhouette displayed on a large video projection screen. Their entire body could be considered the input device, as the system responded to the user’s image and motion with interactive graphics, video effects, and sound. While the interactions were with 2D data imagery on the large display, such fully body, or hand and multi-finger tracking could also be applied to 3D interactions.

Another interesting input device which has been used for 3D interfaces is called ShapeTape™. ShapeTape™ is a curve input device, which senses the bend and twist along its entire length. Researchers have explored the use of such a high degree-of-freedom input device for the manipulation of curves and surfaces in 3D environments.

## 2.5.6 Summary

In this section we have provided an outline of the most common input devices used for interacting with 3D environments. Six degree-of-freedom devices can be used to provide direct manipulation of virtual objects, while enhancements to the mouse can also increase the number of degrees of freedom of an input device, while keeping some of the desirable properties of the mouse.

For added degrees of freedom, researchers have also looked at bimanual techniques, where the user can directly use both hands, or use both hands to hold physical tools. We have also seen how specialized high degree-of-freedom input devices can be used for both 2D and 3D interaction.

Because little research has been conducted on volumetric displays, no one has really explored what input devices should be used with these displays. It will be of interest to see which of these discussed input devices will be most appropriate for interacting with volumetric displays. We may find that the devices will need to be modified or enhanced. We may also find new methods of input, such as using the volumetric display’s enclosing surface as a touch sensitive input device.

While the choice of input device is interesting, this will only be a step in the direction of developing interactive user interfaces for volumetric displays. In the following sections, we will see the 3D interaction techniques and applications which have been developed using the input devices discussed in this section.

## 2.6 Three-Dimensional Interaction Techniques

Along with finding appropriate input devices for volumetric displays, we will be interested in finding effective interaction techniques for such displays. In exploring this topic, the vast literature on interaction within 3D user interfaces and virtual reality.

environments is clearly relevant. A number of researchers have proposed and agreed upon four fundamental tasks for 3D interactions: navigation (or travel), selection, manipulation, and system control. In this section we summarize the interactions techniques which have been developed in each of these categories.

## 2.6.1 Navigation

Navigation refers to the task of positioning and orienting the viewpoint within a 3D environment. Because the environment size displayed within a volumetric display is limited to the size of its enclosure, users will be able to effectively control their viewpoint orientation and position by simply changing the position of their head. As a result, the navigation techniques developed for vast large virtual environments, where changing the viewpoint position may require significant travel distances, will be less applicable, in comparison to the other three fundamental tasks, so we online give a brief outline of them here.

### 2.6.1.1 Cinematic Camera Metaphor

In non-immersive 3D environments, such as 3D graphics and animation programs, mouse movements coupled with modifier keys are generally used to manipulate the position of the virtual camera, which in turn controls the user’s viewpoint of the scene. This is generally termed as a cinematic camera metaphor, since the user can tumble, track and dolly a viewpoint. The Unicam allows users to manipulate the position of the 3D camera using a mouse and only a single button, coupled with different gestures for invoking camera functionality. The StyleCam allows authors to significantly tailor the best possible camera positions and paths to be used by a viewer.

Various metaphors for viewpoint motion and control in 3D environments, which use higher degree-of-freedom input, have also been proposed. Ware and Osborne explore 3 such metaphors which were implemented using a six degree-of-freedom input device which we now discuss.

### 2.6.1.2 Eyeball-in-Hand Metaphor

With the eyeball-in-hand technique, the position of the input device is directly mapped to the position of the virtual camera, or eyeball, within the 3D scene. The viewpoint of this eyeball is then projected on the viewing display. They explored both an absolute mapping between the input device and eyeball position, and a relative mapping, in which the viewpoint only changed when a button was depressed. While the relative mapping allowed for ratcheting, it destroyed the user’s mental model of a fixed invisible scene, and so users found it confusing.

### 2.6.1.3 Scene-in-Hand Metaphor

With the scene-in-hand metaphor, the three-dimensional world is moved in correspondence with the six degree-of-freedom input device. If the device is rotated clockwise, then the scene will also rotate clockwise. Large movements can be accomplished by ratcheting, using a button as a clutch. It was found that the scene-in-hand metaphor was useful for changing the viewpoint in a hierarchical scene. With this technique, navigation can be accomplished by manipulating a hand-held miniature copy of the virtual environment.

### 2.6.1.4 Flying Vehicle Metaphor

The other technique proposed is the flying vehicle metaphor. With this technique the scene is perceived from the position and orientation of the vehicle. The input device is used to control the spatial and angular velocity of the vehicle, allowing it to be moved throughout the scene. This metaphor is commonly used in 3D games, in which the "player position" can be thought of as the vehicle. The user controls the position and orientation of the viewpoint to move throughout the environment. This technique has been enhanced in various ways, such as allowing for rapid and controlled movement.

## 2.6.2 Selection

Selection is a fundamental aspect of any interactive 3D system, as a user must be able to specify an object in the virtual world, so they can then manipulate or interact with it. Techniques for selection have been thoroughly developed within the VR literature. These techniques will be of high relevance to the design of interactive applications for volumetric displays. We now give a review of selection techniques used in 3D environments.

### 2.6.2.1 Image Plane Selection

When 3D environments are displayed on desktop screens, the monitor defines a 2D image plane, which displays the 3D scene. The application projects the objects in the 3D environment onto the image plane for display to the user. The user can select objects in the 3D scene using the image plane by positioning the mouse cursor over the object’s projection on the image plane. In essence the cursor defines a ray perpendicular to the surface of the image plane, and clicking selects the first object which the ray intersects. This technique does not directly extend to 3D displays, as there is not always a well-defined image plane. Ware and Lowther extend the technique for a stereoscopic display by defining the image plane as the viewpoint from only a single eye. This “one-eyed cursor” was found to be an effective selection technique for 3D environments.

### 2.6.2.2 Ray Cursor

For selection within immersive 3D environments, a ray firing selection mechanism called “laser gun” selection was implemented. A ray is emitted from the user’s hand, so the user has control over the start point and orientation of the ray, much like a physical laser pointer. The first object it intersected with would be selected. This technique allowed users to select both near and distant objects; however, it was found to be difficult to select small and distant objects due to the angular accuracy required for such targets. To alleviate this problem, a mechanism called “spotlight selection” was created. Instead of emitting a ray, the user emits a cone with its apex.

A problem with the ray casting selection is that the ray can intersect multiple objects. This problem is magnified when a cone is used instead of a ray. Liang and Green developed a metric to decide which object would be selected if multiple targets were within the spotlight, based on the distance from the targets to the apex and central axis of the cone.

### 2.6.2.3 Occlusion Selection

Occlusion selection is an extension of the image plane selection used on a desktop to immersive 3D environments. With this technique, users select objects that visually lie behind a hand-attached cursor. Essentially this is a ray casting technique, where the ray is defined by the vector which joins the user's eye and hand. This technique has been explored in a couple of different implementations.

Forsberg created aperture based selection where a cone is cast from the users eye and goes through the users finger, and the distance between the finger and the eye controls the angle of diversion of the cone. Because orientation information is not used to define the direction of the ray, they used it for disambiguation when the ray intersected multiple objects. When the ray intersected more than one object, the object whose orientation was most closely matched by the input device was selected.

## Interaction Techniques in Image Plane

Pierce et al. explored several different image plane interaction techniques which use occlusion selection. These include:

1. **Head Crusher Technique**: Objects which lie between the user’s index finger and thumb are selected.
2. **Sticky Finger Technique**: Objects are selected by occluding them with the tip of the index finger.
3. **Lifting Palm Technique**: Objects are selected by flattening the hand and positioning the palm underneath the object.
4. **Framing Hands Technique**: Both hands are used to define a bounding box around the object of interest, using the thumbs and index fingers.

### 3D Cursor for Interaction

A more direct method of interaction, using a 3D cursor that specifies X, Y, and Z coordinates has also been suggested. According to Mine, local interactions in a virtual world should use a direct mapping from the user's hand to the 3D cursor for selecting objects. For selecting objects at a distance, methods like laser beam or spotlight selection could be utilized. Additionally, a "virtual cursor or drone" could be maneuvered by the user throughout the environment until it reaches a target for selection.

## Silk Cursor

The Silk Cursor is a 3D volume cursor, evolving from 2D area cursors. It offers two benefits for selection tasks: enhanced target activation area, similar to 2D area cursors, and a semi-transparent, rectangular shape that helps users distinguish the relative position of targets—whether they are in front, inside, or behind it. Experiments showed its effectiveness in both monoscopic and stereoscopic displays.

## Go – Go Technique

Introduced by Poupyrev in 1996, the go-go selection technique is designed for selecting objects at a distance using a 3D cursor. It features a metaphor of extending the user’s arm. For close objects, the virtual hand corresponds with the real hand’s movement. To access distant objects, extending the hand beyond two-thirds the arm's length causes the virtual arm to grow non-linearly, facilitating the selection of distant objects beyond the normal reach.

## 2.6.2.7 Evaluation of Selection Techniques

In a formal experiment, Ware and Lowther evaluated the one-eyed cursor, which is essentially a ray cursor, where the vector of the ray is always perpendicular to the surface of the screen. They found it to be superior to a standard 3D cursor, as with the one eyed cursor, only two of the three dimensions of a goal target need to be defined. Bowman collected quantitative data to compare ray casting, occlusion selection and the go - go technique. The go-go technique was found to be significantly slower, as it required the positioning of the hand in 3D space. Although there was no significant difference in movement time between ray casting and occlusion selection, occlusion selection caused higher levels of arm strain. Ray casting was more comfortable as users could “shoot from the hip”. To date there has not been a comparison of ray cursor with 3D volume cursors, such as the silk cursor, but area cursors have been shown to be advantageous in 2D environments.

While these results seem to indicate that ray casting techniques should be used for selection within volumetric displays, there are a couple of points which require further exploring. Firstly, the go-go technique was found to benefit from shortened target distances. Within a volumetric display, the distances will be limited by the physical enclosure, so 3D point techniques may not fare as poorly. Secondly, ray cursor selection breaks down in dense target environments, and to date there have not been any formal evaluations of techniques for disambiguating between multiple intersected targets. It may be the case that such a disambiguation mechanism will introduce an overhead cost which mitigates the advantages of ray cursors.

## 2.6.3 Manipulation

Once objects are selected, it is important that users can manipulate them in an interactive 3D application. We now discuss the techniques which have been developed to manipulate objects in 3D environments.

### 2.6.3.1 Direct Six Degree-of-Freedom Manipulation

One of the most common forms of manipulation in virtual environments is to map the movement of a six degree-of-freedom input device to the movement of a selected object.

## Techniques

This allows the object of interest to be rotated and translated as desired.

Techniques have also been proposed to allow for direct manipulation with objects which are at a distance. In the ISAAC system, users could first select an object with a ray cursor and then manipulate the object with a direct mapping from the hand. A similar technique called HOMER (Hand-Centered Object Manipulation Extending Ray-Casting) was suggested by Bowman and Hodges, where the object is selected with a ray cursor and then a virtual hand jumps to the object position, and the object becomes attached to the hand. The World in Miniature interface allows users to quickly select and manipulate an object positioned anywhere in the environment by grabbing the miniature object which is in the palm of their hand. They can orient the miniature environment by rotating the hand that holds it, allowing them to select objects that may be obscured from their current point of view. Once an object is selected, it can be positioned and oriented in the miniature world with a one-to-one mapping from the hand, or also at a greater scale for more fine grain control.

### Voodoo Dolls

Voodoo dolls extend these direct manipulation techniques by allowing bimanual interactions. With this technique, each hand can hold a voodoo doll, a miniature copy of an object in the virtual environment. The dolls are created by using occlusion selection with either hand, and held with a pinch. Dolls can be passed from one hand to the other, and dropped by releasing the pinch. The object held in the dominant hand can be positioned and oriented relative to the object being held in the non-dominant hand. This follows Guiard’s bimanual theory where the dominant hand works in the reference frame set by the non-dominant hand. To move a lamp onto a table, for example, the user creates a voodoo doll of the lamp in the dominant hand and of the table in the non dominant hand. The user then places the miniature copy of the lamp on top of the table. In the actual virtual scene, the lamp will move on top of the table, which remains stationary.

Dolls technique allowed users to position and orient objects more precisely than the HOMER technique [Pierce and Pausch 2002].

## 2.6.3.3 Three-Dimensional Widgets

Conner et al. explored manipulations of objects which diverged from the stranded direct manipulation techniques described above, using three-dimensional widgets [Conner et al. 1992]. Using the widgets allow for manipulations which are difficult or impossible to accomplish using a direct mapping from the physical hand, and also allow for constrained manipulations, such as rotating an object about a single axis. They describe several widgets which allow for different types of manipulations. For example, a virtual sphere can be used to rotate an object. The mouse clicks and drags on the sphere, and the 2D mouse coordinates are mapped to points on the surface of the sphere, causing the object to rotate. Object handles are 3D widgets that constrain the manipulations. For example, handles can be available to scale, rotate, or translate an object along any of the major axes. Many current applications (e.g. MAYA™, 3D StudioMax™) for 3D modeling and animation make extensive use of such 3D widgets since they can be easily operated with status-quo mouse & keyboards input.

### 2.6.3.4 Gestural Manipulation

In Charade freehand gestures were used to manipulate 2-dimensional computerized objects in an augmented reality system. Although the gestural interaction was mapped to the manipulation of two-dimensional objects, this could be a valuable method for manipulating three-dimensional objects. Since this foundational work, gestural interfaces have been developed for pen based devices, large displays, and tabletop displays, and could be a valuable method for interaction with volumetric displays.

### 2.6.4 System Control

System control is the set of commands that the user gives to accomplish work within the application. For example, the user may wish to delete an object, or save a model which they are manipulating. In a standard desktop application, system control is achieved through toolbars and menus. Because these widgets are generally 2D, there are interesting challenges involved with integrating them into a 3D environment.

In Mine, a 2D menu was embedded in the virtual environment. The menu which was developed floats in 3D space and includes various widgets such as radio buttons, sliders, and dials. The user interacts with the menu using a ray cursor, so that the user does not have to make large reaching movements. In the JDCAD system a ring menu was used for item selection, where the items were arranged.

## Figure 2-15 
(a) Ring menus seen in JDCAD system. Menu can be rotated until the item of interest is at the front. (b) The TULIP menu binds different menu options to each individual finger.

Bowman and Wingrave describe and compare three different menu techniques for virtual environments. A floating menu was developed, in which the location of the menu is bound to the location of the user’s head. The menu acts like a standard drop-down menu, which can be navigated through using occlusion selection. The pen and tablet menu system places menus and widgets on the surface of a virtual tablet that corresponds to a physical surface that the user holds. A physical pen is held and controls a virtual stylus, which is used to interact with the tablet. TULIP menus require multiple-finger tracking and bind different menu options to each finger. Users could select the options by pinching the thumb with the appropriate finger (Figure 2-15b). Of these three techniques, the pen and tablet menu was fastest, although users had a preference for the TULIP menu. Users also reported higher discomfort levels with the pen and tablet technique.

## Figure 2-16 
Volumetric display prototypes. (a) Selection using a laser pointer input device. (b) Cuboid-shaped display allows the user to extract side profile views.

## 2.6.5 Interaction Techniques for Volumetric Displays

Given that volumetric displays have not been easily available until recently, there has been relatively little research on how to use such displays effectively in an interactive manner. A speculative paper discusses possible interaction scenarios for volumetric displays, using wizard-of-oz mock-up prototypes to demonstrate various techniques for selection, displaying text and menus, and manipulating objects [Balakrishnan et al. 2001]. However, they did not have or make use of a real volumetric display and as such did not demonstrate any working implementations of their ideas. Some of the main conclusions of their research were as follows:

- **Physical rotation**: users were compelled to physically rotate the displays to get different views of the 3D content.
- **Touching the enclosure**: Users wanted to interact with internal objects by touching the surface of the displays as if it were a touch sensitive input device.
- **Volume Management**: Given the realism of the displays, users wanted to manage the space inside with hand gestures which would be used to manage physical volumes.
- **Viewpoint independent user interface widgets**: Since users are able to move around the displays, interface widgets should be available from any viewpoint.
- **Reuse**: Some input devices and interaction techniques from the VR literature transfer well to volumetric displays and should be reused. Other techniques require some enhancements and innovation so that they are appropriate for use on volumetric displays.

## 2.6.6 Summary

In this section we have presented a number of fundamental interaction techniques which have been developed for 3D environments. These interaction techniques are categorized as navigation, selection, manipulation, and system control. The navigation techniques will be of less relevance to volumetric displays, since there is a limited viewing volume, and users can easily change their viewpoint by physically moving. However, the

## Development of Selection, Manipulation, and System Control Techniques

As discussed in Section 2.6.5, a number of the techniques developed in the VR literature can be reused in volumetric displays. However, a fundamental difference from VR environments is that in volumetric displays, there is a physical barrier separating the user and the virtual data. As a result, many of the interaction techniques, such as direct grabbing and manipulation, will need to be modified, and new interactions techniques may be developed.

The motivation for the development of the techniques discussed in this section was to create an equivalent of the standard desktop GUI in a virtual environment. Our motivation will be similar, as we would like to develop the fundamental interaction techniques which could make up a fluid interface within a volumetric display.

## 2.7 Interactive Three-Dimensional Applications

The interaction techniques discussed in the previous section will provide valuable insights for the development of interaction techniques for volumetric displays. Once new techniques are developed for the volumetric display, the next challenge will be to integrate these techniques into single fluid applications, which can be used for specialized purposes. We now provide a survey of some interactive 3D applications which have been developed for various 3D display systems, which will provide inspiration for the development of interactive applications for volumetric displays.

### 2.7.1 Designing Surfaces in 3D

One of the earliest interactive 3D applications was an experimental system for designing surfaces in 3D, built by Clark in the 1970’s [Clark 1976]. It used a head-mounted display to provide a stereoscopic view, and the user interacted with the system using a three degree-of-freedom wand, which had its position tracked by three microfilament lines.

## 2.7.2 3-Draw

Another system which is used to create 3D models is 3-Draw [Sachs et al. 1991]. The 3-Draw computer aided design tool is a tangible user interface for creating systems of 3D curves and editing them using deformations such as stretching, cutting, bending, and erasing. It is a two handed user interface. The non-dominant hand holds a thin rectangular plate with a six degree-of-freedom tracking device attached to it, and it is used to specify the viewing perspective. The dominant hand is used to point or draw 3D curves with a six degree-of-freedom stylus. A user can directly draw three-dimensional curves of a model as if the model were sitting on the plate that they are holding and positioning with their non-dominant hand. The user can also draw two dimensional curves to specify the shape of their curve and then specify its endpoints on an existing model. This allows an artist to use their sketching skills to accurately draw the shape of a curve, without worrying about its scale, placement, and orientation.

## 2.7.3 3DM

Butterworth developed a 3D modeling system called 3DM, which used a head mounted display to place the user inside the modeling space [Butterworth et al. 1992]. A six degree-of-freedom two-button mouse was used to interact with the system.

3D models, 3DM provides interface elements such as a toolbox, which is a floating menu from which the main commands of the system can be accessed using a cursor. From the toolbox there are tools, which change the current mode of operation, commands, which perform single actions without changing the system’s mode, and toggles, which change some global aspect of the system. The system provides various tools for surface creating, such as a triangle tool and an extrusion tool. The system also provides the standard editing operations, such as scaling, moving, cutting, and pasting. The user could navigate through the system by either walking or flying. The user could also change their scale relative to the environment to allow for faster navigation through larger distances.

## 2.7.4 JDCAD

Liang and Green developed a highly interactive 3D modeling system called JDCAD. The system runs using a head tracked fish tank environment, and the user interacts with the system using a six degree-of-freedom bat. JDCAD provided a suite of general interaction techniques, and operations specific for 3D modeling. Users interface elements included a spherical pop-up menu called Daisy, and the spotlight selection cursor was used for object selection. Available modeling operations included 3D rubber banding object creation, reshaping, alignment, and clipping. It was found that when using the JDCAD system, it could take as little as 1/10 of the time required by a traditional system, to model a mechanical component of moderate complexity.

### 2.7.5 Interactive 3D Workbenches

Poston and Serra developed the Virtual Workbench, which displays 3D images on a mirror in front of the user. The Virtual Workbench allows for bimanual interaction. Each hand can hold different props, which control various tools based on the current mode. The system was developed with medical applications in mind, including tools such as viewing the cross section of a volume. The responsive workbench is another example of a two-handed interactive virtual reality system, in which the user wore a pair of pinch gloves. A stereoscopic image is displayed on a rear-projected tabletop display. A number of two-handed interactions were developed, such as two-handed zooming and rotation about an axis.

With the zooming technique, the non-dominant hand controls a focus point, while the dominant hand controls the zoom factor. For rotation about an axis, the non-dominant hand defines an axis, while the dominant hand controls the rotation. A “steering wheel” rotation technique was also used, where both hands could grab the model and spin it.

### 2.7.6 Neurosurgical Planning

Hinckley et al. designed a user interface for three-dimensional neurosurgical visualization. The interface was based on the manipulation of physical tools in free space. The interface was bimanual, with each hand being able to hold a tool. The interface allowed users to transfer their skills of manipulating tools with two hands.

## 2.7.7 Browsing Volumetric Data with Deformations

McGuffin et al. build upon Hinckley's work by supporting more complex browsing operations of volumetric data [McGuffin et al. 2003]. Instead of just "looking inside" volumetric data, such as seeing a specific cutting plane, users could perform various deformation operations to browse the data. Numerous deformation strategies were explored, such as peeling, slicing, and spreading parts of the volume. These operations could be performed on specific layers, allowing users to see particular areas of interest while maintaining the context of the surrounding areas. The interaction techniques were controlled directly with pop-up menus and 3D widgets customized for each deformation technique.

volumetric display is particularly interesting, as the display does not have to be oriented to one particular user but rather can be accessed from all sides. This allows for natural and intuitive collaboration, as users can simply move around the display to get different perspectives or to interact with others.

When designing collaborative user interfaces for volumetric displays, several factors must be considered. The system needs to support multiple users in an unobtrusive manner, ensuring that their interactions do not interfere with each other. Also, it should facilitate communication between users, providing tools that enhance their ability to share and discuss the information displayed.

There are three primary areas to focus on when designing these interfaces:

1. **User Positioning and Interaction:** Ensuring that users have equal and effective access to the display, regardless of their position around it.

2. **Data Presentation and Manipulation:** Providing intuitive methods for users to interact with the data, including navigation, selection, and modification.

3. **Collaboration Support:** Developing features that support communication and coordination between users, such as annotation tools, shared cursors, or highlighting mechanisms.

In the following sections, we will delve into these areas, examining existing research and identifying best practices for the development of collaborative user interfaces for volumetric displays.

## Single Display Groupware

_single_ shared display was later categorized as single display groupware [Stewart et al. 1999]. This work also falls within the definition of some other categories of research. It fits Shafer and Bowman’s definition of spatial collaboration - collaboration activities focused on physical areas [Shafer and Bowman 2005]. Following the taxonomy given by Ellis, Gibbs, and Rein, it would be classified as same time, same place collaboration [Ellis et al. 1991]. Baecker refers to applications supporting this form of collaboration as synchronous co-located groupware [Baecker 1994]. While collaborative user interfaces have not been explored on volumetric displays, there has been research relevant to the area, which we now review.

### Single Display Groupware

Single display groupware (SDG) is generally defined as systems that support a group of collocated users working with a single display. Stewart et al. are credited with coining the term single display groupware [Stewart et al. 1999], but the first SDG system may have been MMM [Bier and Freeman 1991]. This system was the first to explore a system where multiple users shared a user interface not over a network, but across a single display. The MMM system looked at specific issues such as registering input devices with users, managing screen real-estate for the users, directing feedback to appropriate users without disrupting others, and allowing multiple users to work separately, without distracting each other. 

Following this work, Stewart et al. present a model for SDG, and discussed three issues central to SDG applications: Shared user interfaces, shared feedback, and coupled navigation [Stewart et al. 1999]. Shared user interfaces mean that elements of the user interface must be accessible to each user, and user interface elements must be able to handle multiple simultaneous streams of input. Shared feedback refers to the fact that feedback provided to one user will generally be seen by all users, which can sometimes be problematic. Coupled navigation is an issue that arises when one user navigates to a different part of the viewed data or document. Generally, all users’ views are coupled and so other users will navigate as well. These central issues must be considered when designing a single display groupware application, including on the volumetric display.

## 2.8.2 Collaborative Tabletop Displays

Collaborative tabletop applications are good examples of SDG and spatial collaboration, as the focus of interaction is on a single shared physical device. The following is a small sample of research in this area.

### 2.8.2.1 RoomPlanner

Wu and Balakrishnan developed RoomPlanner, a prototype application for furniture layout [Wu and Balakrishnan 2003]. The application runs on a DiamondTouch display [Dietz and Leigh 2001] which can sense multiple input points from multiple users. They present a suite of interaction technique based on multi-finger and whole-hand gesture interaction. They also incorporate techniques specifically relevant for spatial collaboration, such as creating and maintaining personal interaction spaces, sharing information with collaborators, and interacting with private data.

### 2.8.2.2 DiamondSpin

Shen et al. present a toolkit called DiamondSpin for experimentation with spatial collaboration on tabletop displays [Shen et al. 2004]. DiamondSpin allows for arbitrary orientation and positioning of documents on the display surface. The toolkit also supports various polygonal tabletop layouts, such as rectangular, octagonal, and circular. An important factor of the DiamondSpin is that it allows for multiple work areas, where multiple objects can be active concurrently, allowing for synchronous collaboration.

## 2.8.2.3 Storage Bins

Scott et al. developed a new interaction technique for tabletop displays called storage bins [Scott et al. 2005]. Storage bins are containers for data which allow users to share resources and transition between activities. Storage bins can be moved to bring a collection of items in and out of the users’ current focus, and they can be expanded or collapsed to allow people to dynamically customize their working area. Storage bins provide the same capabilities as containers, allowing users to add or remove items as a group or individually. The bins can also be resized to vary the capacity of the bin.

## 2.8.3 Spatial Collaboration in Virtual Environments

The relevant work on collaborative interaction discussed so far deals with interaction with 2D data – either in electronic meeting rooms or on digital table top displays. There has also been some relevant research on spatial collaboration in 3D virtual environments [Schafer and Bowman 2005]. Schafer and Bowman provide a virtual environment where users individually navigate through the 3D scene, while virtual avatars provide an indication of each user’s location and orientation [Schafer and Bowman 2004]. They analyzed the effect of the frame of reference on the overall collaboration experience, and the users’ awareness of each other’s location and activities. They looked at an egocentric frame of reference, where each user has their own first person view, an exocentric view, where each user has an equivalent and shared third person view of the environment, and a combination of both, in which one user had an egocentric, and the other had an

## Text Layout and Orientation

One significant challenge with spatial collaboration is how text can be effectively displayed to multiple users. If users all have their own viewpoint of the shared physical area, then they will be viewing text from different angles. This could make text difficult, or sometimes impossible to read. For example, if two viewers of the volumetric display are standing 90º apart from each other, then 2D text facing one user will be completely parallel and thus invisible to the other user. The role of orientation has been studied in collaborative settings and it has been agreed upon that elegant algorithms for the orientation of screen elements are required to avoid depriving the users of rich interaction.

On tabletop displays, there have been applications developed in which textual labels are oriented toward each participant. Kruger et al. present a thorough review of systems which attempt to dynamically and automatically re-orient objects. Wigdor and Balakrishnan present a study of the effects of text orientation on table top displays, which can guide interface designers as to when it is important for text to be re-oriented. They found that the effect of orientation on reading labels, numeric and textual data, and performing serial searches, was less dramatic than what might have been previously assumed. This shows that in some situations the designer need not worry about providing perfect orientations of all text to every user of a system.

## In the VR realm, generally each user has their own view of the world

In the VR realm, generally each user has their own view of the world, and so there are not the same challenges for proving text orientations suitable for all users. The system can simply provide appropriate orientations for each user’s view. Chen et al. provide a taxonomy of text layouts in virtual environments. They note that text can either have a within-the-world display, in which it appears inside the 3D environment, and can even be projected on to the faces of various 3D objects, or it can have a heads-up display, in which the text appears on an invisible 2D image plane directly in front of the user’s viewpoint. They found the heads-up display to perform better and to be preferable in a searching task. Bell et al. look at techniques for view management, in which decision algorithms for the layout of graphical objects such as text take into account visibility constraints that allow applications to manage what users see. They provide an algorithm which continuously updates the position, size, and transparency of textual labels based on the users viewpoint, preventing objects from occluding each other. The technique they present is valuable for 3D environments which have a single viewer, but would need to be extended for when there are multiple viewers of the scene.

### 2.8.5 Summary

In this section we have provided an outline of the research which relates to the development of collaborative applications for volumetric displays. Such collaboration would be synchronous and co-located, and falls within the definitions of single display groupware, and spatial collaboration.

We presented a brief overview of the early single groupware research, and also looked at spatial collaborations occurring on table-top displays. Since users of such applications are focused on a shared physical area, albeit a 2D space, these interfaces will be of great relevance to the development of collaborative interfaces for volumetric displays. Some of the important interaction techniques for spatial collaboration discussed were the creation and manipulation of shared and personalized spaces, interaction with private data, supporting multiple active areas, and techniques for storing data and sharing data between users. Such techniques should be incorporated in collaborative applications for volumetric displays.

We also looked at relevant collaborations in VR environments. The research demonstrated that egocentric views can increase the understanding of what other users are doing. It was also seen that awareness features, such as illustrating the locations and areas of interaction of other users, are important to enhance the sense of presence within such applications. It would be interesting to look at ways to do this on volumetric displays. Users would clearly know the location of the collaborators, but techniques for indicating what their collaborators were looking at or doing should be investigated.

Lastly, we discussed the important challenge of orienting text and widgets appropriately for multiple users. We have discussed applications for tabletop displays which automatically orient data for multiple users. This is an especially important area for volumetric displays, as improperly oriented text could be difficult or even impossible to read if parallel to a user’s line of vision. Furthermore, users may not be stationary, taking advantage of the display’s 360º viewing angle, and so menus and widgets should be accessible from all areas.

## Summary of Background Literature

We have presented various theories, studies, and techniques from previous literature which relate to the exploration of user interfaces for volumetric displays. However, much of the research is taken from the virtual reality community, and there is very little previous research which has been focused on volumetric displays. An investigation into the interaction issues which are associated with volumetric displays will need to be conducted. We carry out such an investigation in the remainder of this thesis.

This investigation requires both a study of low-level human factor issues, as well as higher-level explorations of interaction techniques and user interfaces. The most relevant low-level human factors issues are evaluating the viewing experience provided by the volumetric display in comparison to other 3D display modes and investigating the user’s ability to interact with a true 3D display space. These issues are investigated in Chapters 3-5. At a higher level, new interaction techniques and user interfaces will need to be explored, which are designed specifically for volumetric displays, for both single and multiple users. We describe our work in this area in Chapters 6-8.

