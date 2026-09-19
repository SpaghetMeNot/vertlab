# :construction: vertLab

!!! warning
    This site is currently placeholder/WIP

Welcome to the vertLab documentation. Here you'll find everything there is to know about the tools.

## What is vertLab?

VertLab is a collection of tools for controlling **vertex attributes** and **sculpting masks**.

Vertex attributes are versatile. Example use-cases include:

- Use to drive shader effects e.g. texture blending.
- Use to displace geometry.
- Bake to textures.
- Pack to vertex colors and export to a game engine.

!!! info "vertLab is Geometry Based"
    The resolution of vertLab is directly influenced by mesh density/topology.
    

### :material-plus-network: Create Attributes

Create attributes from advanced mesh analysis tools such as ray-traced occlusion and curvature. Other generators include noise, gradients and camera-based silhouette.

![create_attributes](./assets/create_attributes.png)

### :octicons-sliders-24: Modify Attributes

Modify attributes by remapping, mixing or flowing them down a mesh. You can also pack up to four attributes to a vertex color for exporting to game engines.

![modify_attributes](./assets/modify_attributes.png)

### :material-brush: Sculpting Masks

Use vertLab's powerful attribute tools directly on sculpting masks. This includes mask creation, manipulation and blending.


![sculpt_masks](./assets/sculpt_masks.png)
