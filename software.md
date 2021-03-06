- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- **[Software](/3-DPrintingCornealOrganoids/software)**
- [Materials](/3-DPrintingCornealOrganoids/materials)
- [Cells](/3-DPrintingCornealOrganoids/cells)

Open-source software tools were chosen for modularity and rapid-prototyping in mind with added benefit of lower costs than commercial software packages. The combination of these programs allow specific control/modification of machine movements, fast troubleshooting that is adaptable to our hardware platform. More information on these open-source softwares can be found at the reference listed. 

* Note: this inexpensive system is intended for use by trained lab technicians with some experience with 3D CAD design tools and assumed proficient to install and use these softwares on a desktop workstation. A desktop workstation was chosen as opposed to developing a custom mobile application due to the readily available open-source options that are simpler and more efficient for customizing/testing this process. All softwares listed below are free to download. 

Software| Features/Benefits & Download
------------ | -------------
**Autodesk Fushion 360** | CAD-based software for genearl solid modeling of 3D design/ creating STL file format: (https://www.autodesk.com/education/edu-software/overview)
**CuraEngine** | Third party slicer software for pre-processing featuring ready-made settings profiles and an intuitive user interface:  (https://www.github.com/ultimaker/curaengine)
**gCode Editor 1.0 (gCodeAPI.Net 1.0)** | Encapsulates g-Code commands into high-level functions (C#, python) with a graphical user interface for visualizing sliced formatted g-Code. It allows easy modifications/optimizing settings to adjust to printing living cells/ECM needs with the ability to edit raw gCode through the gCode Editor. Fast and simple method to identify errors and replace machine movement, insert or relocate points and edit raw g-Code by clicking. This g-Code editor will be necessary for the custom commands to control the relative gel flow rate and UV LED for PetriPrinter: (http://petriprinter.elte.hu/main/downloads) 
**PetriPrinter** | A g-code generator program which handles 3D model files by aligning into suitable positions for print in specified dimensions/culture dishes (see figure below). The interface provides the access to assign objects to positions, with collion-safe, optimized entry features and coordinated movement between dishes, wells and exits to distribute printer motion according to the defined pattern. Settings can be easily adjusted to accomodate our hardware by providing the starting height, printing temperature, row/column distance, extrusion speed, absolute position, etc: (http://petriprinter.elte.hu/main/downloads)
**Marlin** | An open-source firmware 3D printer driver based on the Arduino platform and primarily designed for RepRap based FDM prints using the Arduino platform. There are multiple step-by-step tutorials provided by Marlin and technology experts on downloading, editing the configuration and compiling the Marlin project into binary code for upload to the external Arduino board to manage the separate power sources using the stepper drivers and driver for the UV LED light. Editing can be performed using the Ardunio IDE or other text editing application: (https://marlinfw.org/meta/download/)

### Diagram of open-source softwares used to process imported 3D solid modeling file and generate, visualize and edit the g-Code for the Arduino microcontroller (modified from the reference below). ![Image of g-Code editors](/3-DPrintingCornealOrganoids/SoftwareImages/gCodeAPI.png)

### Diagram of overall information flow from desktop software (G-code) -> Firmware (translated signal) -> micro-controller (step pulses) -> stepper and UV LED drivers (UV LED on/off, motor X Y Z motion)
![Image of System Level Flow](/3-DPrintingCornealOrganoids/SoftwareImages/SystemLevelDiagram.png)

### PetriPrinter interface allows customization to the g-Code to accomodate desired Transwell plate pattern
![Image of PetriPrinter Interface](/3-DPrintingCornealOrganoids/SoftwareImages/PetriPrinter.png)
 
* Below is a g-Code example instructions for the microcontroller which are processed by the Marlin firmware and translated into step pulses for the stepper drivers/UV LED driver to move the stepper motors/switch the UV LED light on/off
```
// Example: Arduino microcontroller instructions
G1 X50 Y20 E15 
// G1 = linear movement
// X=_ Y =_ are coordinates
// E=_ extrusion drive instructions to deposit/retract bioink
```
## References
[1] _C. Pakhomova, D. Popov, E. Maltsev, I. Akhatov, and A. Pasko, ???Software for Bioprinting,??? Int J Bioprint, vol. 6, no. 3, Jun. 2020, doi: 10.18063/ijb.v6i3.279._
