- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- **[Software](/3-DPrintingCornealOrganoids/software)**
- [Materials](/3-DPrintingCornealOrganoids/materials)
- [Cells](/3-DPrintingCornealOrganoids/cells)


# Explaination of design choice
### Open-source software tools were chosen for modularity and rapid-prototyping benefits and to avoid premium costs of commercial software packages. Combined these programs will allow specific control/modification of machine movements, fast troubleshooting that can be easily adapted to our hardware platform. More information on these open-source softwares can be found at this source: C. Pakhomova, D. Popov, E. Maltsev, I. Akhatov, and A. Pasko, “Software for Bioprinting,” Int J Bioprint, vol. 6, no. 3, Jun. 2020, doi: 10.18063/ijb.v6i3.279.

_This inexpensive system is intended for use by trained lab technicians with some experience with 3D CAD design tools and assumed proficient enough to implement the bioplotter design by interating through softwares installed on a desktop workstation. This option was chosen as opposed to developing a mobile application due to the readily available open-source components that is simpler and more efficeint for customizing and testing than a mobile application. All softwares listed below may be downloaded free of charge. _

Software| Features/Benefits & Download
------------ | -------------
**Autodesk Fushion 360** | CAD-based software for genearl solid modeling of 3D design/ creating STL file format **[Autodesk]**(https://www.autodesk.com/education/edu-software/overview)

**CuraEngine** | Third party slicer software and pre-processing featuring ready-made settings profiles and an intuitive user interface **[CuraEngine]** (https://www.github.com/ultimaker/curaengine)

**gCode Editor 1.0 (gCodeAPI.Net 1.0)** | Encapsulates g-Code commands into high-level functions (C#, python) with a graphical user interface for visualizing sliced formatted g-Code. It allows easy modifications/optimizing settings to adjust to printing living cells/ECM needs with the ability to edit raw gCode through the gCode Editor. Fast and simple method to identify errors and replace machine movement, insert or relocate points and edit raw g-Code by clicking. This g-Code editor will be necessary for the custom commands to control the relative gel flow rate and UV LED for PetriPrinter. **[gCodeAPI]** (http://petriprinter.elte.hu/main/downloads) 

**PetriPrinter** | A g-code generator program handles 3D model files by aligning into suitable positions for print in specified dimensions/culture dishes (see figure below). The interface provides the access to assign objects to positions, with collion-safe, optimized entry features and coordinated movement between dishes, wells and exits to distribute printer motion according to the defined pattern. Settings can be easily adjusted to accomodate our hardware by providing the starting height, printing temperature, row/column distance, extrusion speed, absolute position, etc. **[PetriPrinter]** (http://petriprinter.elte.hu/main/downloads)

**Marlin** | An open-source firmware 3D printer driver based on the Arduino platform and primarily designed for RepRap based FDM prints using the Arduino platform. There are multiple step-by-step tutorials provided by Marlin and technology experts on downloading, editing the configuration and compiling the Marlin project into binary code for upload to the external Arduino board to manage the separate power sources using the stepper drivers and driver for the UV LED light. Editing can be performed using the Ardunio IDE or other text editing application. **[Marlin]**(https://marlinfw.org/meta/download/)

### Diagram of open-source softwares used to process imported 3D solid modeling file and generate, visualize and edit the g-Code for the Arduino microcontroller. ![Image of g-Code editors](https://github.com/chbe3890project/3-DPrintingCornealOrganoids/SoftwareImages/gCodeAPI.png)

### Diagram of information flow from desktop software (G-code) -> Firmware (translated signal) -> micro-controller (step pulses) -> stepper drivers/motor X Y Z + UV LED driver
![Image of PetriPrinter Interface](https://github.com/chbe3890project/3-DPrintingCornealOrganoids/SoftwareImages/PetriPrinter.png)
 
Below is g-Code example instructions for the microcontroller which are processed by the Marlin firmware and translated into step pulses for the stepper drivers and UV LED driver to move the stepper motors/switch the UV LED light on/off
```
// Example: Arduino microcontroller instructions
G1 X50 Y20 E15
// G1 = linear movement
// X=_ Y =_ are coordinates
// E=_ extrusion drive instructions to deposit/retract bioink
```
