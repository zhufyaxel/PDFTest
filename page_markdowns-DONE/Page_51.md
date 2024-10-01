## at the user’s hand (Figure 2-10b). This allows a certain level of error to be accommodated.

![Figure 2-10. (a) Ray cursor selection. Image taken from Mine [1995a]. (b) Spotlight selection. Image taken from Liang and Green [1994].](image_path)

A problem with the ray casting selection is that the ray can intersect multiple objects. This problem is magnified when a cone is used instead of a ray. Liang and Green developed a metric to decide which object would be selected if multiple targets were within the spotlight, based on the distance from the targets to the apex and central axis of the cone [Liang and Green 1994]. Hinckley suggests that the ray casting technique could be augmented with a mechanism for cycling through the set of all ray-object intersection points [Hinckley et al. 1994].

### 2.6.2.3 Occlusion Selection

Occlusion selection is an extension of the image plane selection used on a desktop to immersive 3D environments [Mine et al. 1997]. With this technique, users select objects that visually lie behind a hand-attached cursor. Essentially this is a ray casting technique, where the ray is defined by the vector which joins the user's eye and hand. This technique has been explored in a couple of different implementations.

Forsberg created aperture based selection where a cone is cast from the users eye and goes through the users finger, and the distance between the finger and the eye controls the angle of diversion of the cone [Forsberg et al. 1996]. Because orientation information is not used to define the direction of the ray, they used it for disambiguation when the ray intersected multiple objects. When the ray intersected more than one object, the object whose orientation was most closely matched by the input device was selected.