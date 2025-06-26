# Houdini LUT Volume
![image](https://github.com/user-attachments/assets/4420c124-7e13-434e-b3d9-e4b55f82209e)

Houdini LUT Volume is a package for Houdini that enables you to read LUT (Lookup Table) files as volume data and apply them to images or color data.  
This package includes the following two HDAs:

## Contents

- **Volume From LUT (SOP)**  
  A SOP node that loads a LUT file (currently `.cube` format) as a volume.

- **LUT (COP)**  
  A COP node that applies a LUT to an input image using the Volume From LUT SOP internally.

## Node Specifications

### Volume From LUT (SOP)

- **File parameter**  
  Specify a LUT file in `.cube` format.

- **Split Channels parameter**  
  - On: Outputs R, G, and B as three separate scalar volumes.  
  - Off: Combines R, G, and B into a single vector volume (vector field).

- **Supported Formats**  
  Currently supports `.cube` files only.  

### LUT (COP)

- Uses the Volume From LUT SOP internally to apply the LUT to the input image.
- Enables easy LUT conversion of images in the COP network.

## Installation

1. Clone This Repository into your `$HOUDINI_PREF_DIR/packages`.
2. Copy and paste `houdinilutvolume.json` in it into `$HOUDINI_PREF_DIR/packages`.

cf. [Houdini packages | Houdini help](https://www.sidefx.com/docs/houdini/ref/plugins.html)

## License / Other Notes

- Please specify your license and distribution policy as appropriate.

## Notes

- This version supports `.cube` LUT files only.  
  Support for other LUT formats is planned for future releases.
