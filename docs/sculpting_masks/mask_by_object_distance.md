# Mask by Object Distance

![icon](../assets/icons/mask_distance.png){ width=128 }

## Settings

#### Mix
- **Blend Mode:** Blend mode with existing mask:
    - **Disable:** Disable blend.
    - **Replace:** Replace A with B.
    - **Multiply:** Muliply A by B.
    - **Add:** Add B to A.
    - **Min:** Minimum value of A and B.
    - **Max:** Maximum value of A and B.
    - **Screen:** Brighten A using the brightness of B.
    - **Overlay:** Brighten/darken A using values above/below 0.5 on B.
    - **Divide:** Divide A by B.
    - **Subtract:** Subract B from A.
- **Opacity:** Opacity of blend.

----
#### Objects
- **Objects/Collection:** Choose up to 6 objects or a collection:
    - **Objects.**
    - **Collection.**
- **Object Count:** Number of objects to include
- **Union Manifold Islands:** Union manifold mesh islands. This removes areas of mesh overlap.

----
#### Distance
- **Distance:** How to measure distance from surface.
    - **Unsigned:** Absolute distance from the surface.
    - **Signed:** Areas inside the surface have negative distance, outside areas have positive distance.
- **Min Distance:** Points closer than this will be black.
- **Max Distance:** Points further away than this will be white.
- **Interpolation:** Interpolation of distance to value.
    - **Linear.**
    - **Smooth Step.**
    - **Smoother Step.**
- **Invert:** Invert the values of the distance attribute.

----
#### Blur
Blur the distance mask.

- **Iterations:** How many times to blur the values for all elements.
