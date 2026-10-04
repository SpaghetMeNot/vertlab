# Common Settings

## Raycasting

Modifiers that use ray casting use the same underlying method:

1. Rays are cast from a point in a Fibonacci cone up to the specified angle.

    ![rays](./assets/rays/ray_distribution_angle.gif "Ray Distribution"){ width=512 }

2. Collisions with geometry and their distance are recorded.
3. The collision data is averaged for the point using one of two methods:
    - **Hit count**: Collisions / Total rays
    - **Average Distance**: Hit Distance / (Total Rays * Ray Length)


## S-Curve

Many vertLab tools have "S-Curve" controls to quickly add contrast to 0:1 values.

There are two settings to control a S-curve:

- **Intensity/Amount** {-1:1} How much of a curve to add. 0 = linear interpolation.
- **Midpoint** {0:1} Where the center of the S is. At fully 0 or 1 the S-curve becomes a bias.

![s-curve](./assets/values/s-curve.gif "S-Curve Settings")

## Histogram Operations

These settings remap the 0:1 value range. You can see their effect on both a noise and linear gradient below.

<div class="grid cards" markdown>

- __Input Values__

    ![input](./assets/values/values_input.png)

    Base values, no operation.

- __Splits__

    ![split](./assets/values/values_split1.png)

    Scales and loops the value range. Introduces harsh transitions.

- __Offset__

    ![offset](./assets/values/values_offset_third.png)

    Offsets and loops values.

- __Fold: Peaks__

    ![fold_peaks](./assets/values/values_fold_peaks.png)

    Values above a threshold will be inverted. The threshold becomes the new white point.

- __Fold: Valleys__

    ![fold_valleys](./assets/values/values_fold_valleys.png)

    Values below a threshold will be inverted. The threshold becomes the new black point.

- __Split + Fold__

    ![combined](./assets/values/values_split_fold.png)

    Folding values removes the harsh changes introduced with using "Split".
    

</div>

