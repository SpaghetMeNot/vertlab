# Mask Flow

![icon](../assets/icons/mask_flow.png){ width=128 }

## Settings

#### Mix
Mix generated mask with existing one.

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
#### Direction
Direction of flow.

- **Space:** Coordinate space of flow direction:
    - **Local:** Flow direction is in local space (uses object rotation).
    - **Global:** Flow direction is in global space (ignores object rotation).
- **Direction:** Flow direction vector.
- **Random:** Mix in random noise to flow direction. A value of 1 will completely ignore specified direction.

----
#### Random Noise
Noise settings for the random direction.

- **Noise Scale:** Size of the largest features in the noise.
- **Octaves:** The number of noise octaves. Higher values give more detailed noise but increase render time.
- **Roughness:** Blend factor between an octave and its previous one. A value of zero corresponds to zero detail.
- **Noise Offset:** Offset the noise W position. Effectively a smooth transition between seeds.

----
#### Flow Steps
Flow simulation settings.

- **Flow Iterations:** How many iterations of flow to calculate.
- **Step Size:** Maximum distance travelled by each flow step. Bigger step sizes are cheaper to calculate but can result in stepping artifacts.
- **Fade:** Fade the head/tail of the flow simulation. Positive values will fade the tail (allowing darker areas to flow over lighter areas). Negative values fade the head resulting in a smooth fade out of the flow.
- **Minimum Angle Speed:** Decrease flow speed depending on surface angle. 0 will completely stop flow on surfaces perpendicular to the flow direction. 1 will ignore the surface angle and full flow speed will occur everywhere.

----
#### Streaks
Add streaks/noise to the flow simulation.

- **Amount:** Intensity of streaks applied to flow simulation.
- **Thickness:** Scale of the noise used for streaks. Higher value = thicker streaks.
- **Offset:** Offset the streak noise W position. Effectively a smooth transition between seeds.

----
#### Noise Values
- **Noise Octaves:** The number of noise octaves. Higher values give more detailed noise but are more expensive. Stop increasing when there is no visual impact.
- **Noise Roughness:** Blend factor between an octave and its previous one. A value of zero corresponds to zero detail.
- **Stretch:** Stretch the noise used for streaks in the flow direction. 0 = No stretch, uniform noise. 1 = Maximum stretch, 2D noise.
- **Contrast:** Increase value contrast of noise, giving higher contrast streaks.
- **Bias:** Midpoint of contrast operation. Higher values will produce a darker noise.

