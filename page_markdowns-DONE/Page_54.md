## 2.6.2.7 Evaluation of Selection Techniques

In a formal experiment, Ware and Lowther evaluated the one-eyed cursor, which is essentially a ray cursor, where the vector of the ray is always perpendicular to the surface of the screen [Ware and Lowther 1997]. They found it to be superior to a standard 3D cursor, as with the one eyed cursor, only two of the three dimensions of a goal target need to be defined. Bowman collected quantitative data to compare ray casting, occlusion selection and the go - go technique [Bowman et al. 1999]. The go-go technique was found to be significantly slower, as it required the positioning of the hand in 3D space. Although there was no significant difference in movement time between ray casting and occlusion selection, occlusion selection caused higher levels of arm strain. Ray casting was more comfortable as users could “shoot from the hip”. To date there has not been a comparison of ray cursor with 3D volume cursors, such as the silk cursor, but area cursors have been shown to be advantageous in 2D environments [Worden et al. 1997]. 

While these results seem to indicate that ray casting techniques should be used for selection within volumetric displays, there are a couple of points which require further exploring. Firstly, the go-go technique was found to benefit from shortened target distances [Bowman et al. 1999]. Within a volumetric display, the distances will be limited by the physical enclosure, so 3D point techniques may not fare as poorly. Secondly, ray cursor selection breaks down in dense target environments, and to date there have not been any formal evaluations of techniques for disambiguating between multiple intersected targets. It may be the case that such a disambiguation mechanism will introduce an overhead cost which mitigates the advantages of ray cursors.

## 2.6.3 Manipulation

Once objects are selected, it is important that users can manipulate them in an interactive 3D application. We now discuss the techniques which have been developed to manipulate objects in 3D environments.

### 2.6.3.1 Direct Six Degree-of-Freedom Manipulation

One of the most common forms of manipulation in virtual environments is to map the movement of a six degree-of-freedom input device to the movement of a selected object