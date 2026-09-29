# Ambient Occlusion

![icon](../assets/icons/Occlusion.png){ width=128 }

Calculate ray-traced ambient occlusion on a mesh. For more information about the ray-casting process see [here](../common_settings.md#raycasting). You can reduce noise by increasing ray count (expensive) or blur (cheaper).

![ao](../assets/ambient_occlusion/ambient_occlusion.png)

You can preserve sharp edges by switching to the ***Face Corner*** domain. This can be useful on low poly meshes:

<div class="grid cards" markdown>
- __Point Domain__


    ![ao point](../assets/ambient_occlusion/ao_point.png)

- __Face Corner Domain__

    ![ao corner](../assets/ambient_occlusion/ao_corner.png)
</div>

***Ray Length*** will change the "size" of the AO as rays will not collide with surfaces further away:

<div class="grid cards" markdown>
- __Small Ray Length__

    ![ao small](../assets/ambient_occlusion/ao_small.png)

- __Large Ray Length__

    ![ao_large](../assets/ambient_occlusion/ambient_occlusion.png)
</div>



## Outputs
- **Point Occlusion:** Output occlusion attribute for points (no sharp edges).
- **Face Corner Occlusion:** Output occlusion attribute for face corners (allows sharp edges). Domain must be set to "Face Corner".
- **Color:** Output occlusion as color attribute (used for visualisation).
## Settings

- **Strength:** Raises calculated AO by a power. Increase to darken AO.
- **Domain:** Calculate AO per:
    - **Point:** Calculate AO per point. Cheaper but does not allow for sharp edges.
    - **Face Corner:** Calculate AO on face corners. More expensive but allows for sharp edges. Useful for low poly models

----
#### Rays
- **Accumilation:** How ray values are accumilated:
    - **Average Hit Distance:** Uses the average ray hit distance compared with the ray length. Often produces smoother results but values will change with the ray length.
    - **Hit Count:** Uses ray hit/miss ratio. Can be noisier but values are independent of ray length.
- **Ray Count:** Number of rays cast from each point.
- **Ray Length:** Maximum distance to check for ray collisions.
- **Cone Angle:** Maximum ray angle from the normal. Rays will be distributed evenly in a cone up to this angle.

----
#### Blur
Blur result. Can help improve noise on dense meshes.

- **Blur Iterations:** How many iterations to blur the result.

----
#### Occlusion Geometry
- **Occlusion Object:** Additional object to act as occluder.
- **Occlusion Collection:** Additional collection of objects to act as occluders.

