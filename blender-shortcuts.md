# Blender Fiddles

### Glass Material
  - Render Settings:
    - Render Engine: `EEVEE`
    - Screen Space Reflections: `true`
    - Refraction: `true`
    - Half Res Trace: `true`
  - Material Settings:
    - Base Color: `light grey/white`
    - Transmission: `1`
    - Roughness: `0`
    - IOR: `1.52`
    - Alpha: `.9`
    - Settings: 
      - Blend Mode: `Alpha Hashed`
      - Screen Space Refraction: `true`
      - Refraction Depth: `.5 to 1 mm`

# Keyboard Shortcuts

### Move Origin on Object
  - Object Mode > Axis View
  - `Shift` + `.`

### Separate by Selection
  - Edit Mode > Select Target faces/lines/vertices
  - `Shift` + `D`

### Bring Vertices to Flat Plane
  - Side View
  - Delete bottom vertices (if necessary)
  - `s` , `z` , `0`


# Videos

### Turn 2D Image to 3D
[Youtube - 2D Logo to 3D](https://www.youtube.com/watch?v=BcjPCjxsCZo)
  - Starts with a plane (Should be same size as image in pixels)
  - Subdivide x2
  - Modifier > Deform > Displace
  - Texture > Open Image
  - Apply Displace (Use negative strength)
  - Remvoe Bottom vertices (Removes background vertices)
  - Select all vertices to same layer
    (s > zz > 0 > enter)
  - Select sharp edges and separate by selection
  - Fill Vertices
  - Solidify


### Pivot Joints and Parenting Objects
[Youtube - Create Pivots and Parent Objects](https://www.youtube.com/watch?v=sis3Okfp2Ps)
  - Move an objects origin
  - Parent objects so that rotating/moving one object will move a child object with it
  - `ctrl` , `.` to move the pivot point



### Camera View
  - Num Pad `0` - puts you to the perspective of the camera, when a camera is added to the workspace
  - Use for taking a 2d image of a 3d model
    - Might need to manually adjust camera postion so it captures you image as close to its dimensinons as close as possible.


### Multi-Color printing

#### Light Text on Dark Background
  - Determine object layer count
  - Bambu Studio Slice Settings:
    - `Bottom Paint Penetration Layers`:
      - Set deept enought relative to total layers
        - If total layers = `100` and want a light text on dark background:
          - Set `Bottom paint penetration layers` high but at least one less than total layers.
          - Set Bottom shell layers (assuming color print is coming from bottom) to at least 3 layers.


### Level Vertices
  - Select axis view
    - Select plane view (X, Y, Z)
    - `s`, `$PLANE_TO_LEVEL`, `<enter>`
