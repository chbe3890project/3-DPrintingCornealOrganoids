- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- [Software](/3-DPrintingCornealOrganoids/software)
- **[Materials](/3-DPrintingCornealOrganoids/materials)**
- [Cells](/3-DPrintingCornealOrganoids/cells)

# Materials

## Rationale for materials selection
The cornea has 5 distinct layers, all of which have their own specific composition. Of the 5 layers, 3 are cellularized and contribute most to the function of the cornea. The bottom most layer is the endothelium, which is composed mostly of collagen. The middle layer is the stroma, and this layer contributes to the bulk of corneal thickness, and is also majorly composed of collagen. The main protein of the top layer, the epithelium, is keratin. An important function of the epithelium is to be at the air/liquid interface of the cornea, so the cells of this layer must have exposure to both air and the underlying hydrogel.

Since the main component of both the endothlium and stroma is collagen, the hydrogel material for these layers will be Type I collagen. For the epithelium, a keratin-based hydrogel using keratin extracted from hair will be used. Using a naturally occurring material that is found in these layers will better recapitulate the ECM to promote cell growth and organization, as well as create a platform that can be representative of in vivo corneas for drug screening.


## Chemistry: composition, crosslinking mechanism, and kinetics
The collagen-based gel for both the endothelium and stroma will be formulated from UV-crosslinkable [methacrylated collagen](https://advancedbiomatrix.com/photocol-irg.html) will be used for these layers of the print. The components of the PhotoCol-Irg Kit can be see in the image below. Briefly, the desired volume of photoinitiator (0.02%) will be solubilized in ethanol and mixed with the methacrylated collagen solution (8mg/mL; PhotoCol-Irg, Advanced BioMatrix, San Diego, CA) (Nguyen et al.). The endothelial layer will be cast in the well plate and cured, and then cells seeded directly onto the surface of the gel. The stromal layer will include encapsulated cells and will be printed directly onto the endothelial layer. 
![PhotoCol(R)-Irg Kit](/3-DPrintingCornealOrganoids/Chemistry/PhotoCol.jpg)
PhotoCol-Irg Kit from Advanced Biomatrix

The keratin-based epithelial layer will be composed of UV-crosslinkable allylated keratin. Keratin will be extracted from hair and allylated via two-step reaction consisting of oxidative elimination of sulfhydryl group of cysteine (−SH group) to Dha followed by the conversion of Dha to s-allyl cysteine was used to functionalize keratin at cysteine residues (Barati et al.). The structure can be seen in the figure below. Briefly, a solution of the allylated keratin in PBS (10 mg/mL) will be combined with the photoinitiator solution in PBS (0.75wt% keratin solution). The keratin extracellular matrix and cells that comprise the layer will be deposited in two steps: first, the acellular keratin hydrogel will be printed and cured directly onto the collagen-based stromal layer. Next, cells suspended in Matrigel will be printed onto the cured keratin layer to recapitulate the air/liquid interface of the epithelium. 

![Allylated Keratin](/3-DPrintingCornealOrganoids/Chemistry/Keratin.jpg)
Allylation and UV crosslinking of keratin bioink

Both the collagen and keratin-based hydrogels will use Irgacure as a photoinitiator. Irgacure has shown to be an effective photoinitiator in bioprinting applications. It allows the hydrogels to be crosslinked at 365nm UV light, which is within the range of wavelengths of UV suitable for gels encapsulating cells. Cure time for the collagen layers will include 30 minutes of thermal gelation at 37 degrees Celsius, followed by 1 minute of UV crosslinking. The keratin layer will be crosslinked with UV for 5 minutes immediately after deposition.

![Irgacure](/3-DPrintingCornealOrganoids/Chemistry/Irgacure.jpeg)

Photoinitiator (Irgacure 2959) used for all bioinks 

## Extrusion design
### Nozzle Sizes 
- [30G blunt needle](https://www.cellink.com/product/sterile-standard-blunt-needles-30g-50-pieces/) (160um inner diameter): This nozzle will be used to print the collagen-based stromal layer with encapsulated cells of the corneal organoid. This layer is about 500um in thickness in vivo, so the resolution using this nozzle will be around 500-600um. 
- [34G blunt needle](https://www.cellink.com/product/sterile-standard-blunt-needles-34g-50-pcs/) (80um inner diameter) : This nozzle will be used to print the keratin-based epithelial layer as well as the top-most matrigel layer with encapsulated cells. Although a resolution of 50um will not be achievable with this size of a nozzle, a resolution of 100um will be suitable for this application.  

### Extrusion Speed
Initial extrusion speed employed will be 6mm/s (Isaacson et al.). Cell viability and organoid integrity will be analyzed, and extrusion speed and rate will be optimized based on these results. Ideally, a low speed will be used because of the small nozzle diameters in order to achieve best cell viability and organoid integrity following printing. 

### Shear Stress Considerations
Since nozzle sizes for this application are small, shear stress induced on encapsulated cells could affect viability. To reduce shear stress as much as possible, a small extrusion speed will be used to deposit bioinks into the organoid. Cell viability will be analyzed and extrusion speed optimized to achieve highest possible viability.


## GMP considerations
### In order to reduce contamination risks and protect cells during printing, lab technicians will follow these procedures:
- Aseptic technique: using  sterile gowns, gloves, and masks while operating or preparing materials for the bioprinter. 
- Separate bioreactors will be used for culturing each cell type
- New material will be added and sterile filted using Millex-GP Syringe Filter 0.22 µm polyethersulfone units fore adding to extruders 
- Components will be autoclaved (ex. nozzles after use to reduce risk of contamination) before installation
- The unit will be housed in a standard Biosafety Hood
- For safety: amber UV-protective goggles should be worn at all times to provide eye protection
- The proposed order of printing the 3 matrix layers (onto prepared endothelial monolayer) is shown below in the schematic from reference [5]: [PrintingSchematic](3-DPrintingCornealOrganoids/SoftwareImages/PrintConcept.png)

## References
[1] T. F. Dyrlund, E. T. Poulsen, C. Scavenius, C. L. Nikolajsen, I. B. Thøgersen, H. Vorum, and J. J. Enghild, “Human Cornea Proteome: Identification and Quantitation of the Proteins of the Three Main Layers Including Epithelium, Stroma, and Endothelium,” Journal of Proteome Research, vol. 11, no. 8, pp. 4231–4239, 2012. 

[2] T. U. Nguyen, K. E. Watkins, and V. Kishore, “Photochemically crosslinked cell‐laden methacrylated collagen hydrogels with high cell viability and functionality,” Journal of Biomedical Materials Research Part A, vol. 107, no. 7, pp. 1541–1550, Feb. 2019. 

[3] D. Barati, S. Kader, S. R. Pajoum Shariati, S. Moeinzadeh, R. H. Sawyer, and E. Jabbari, “Synthesis and Characterization of Photo-Cross-Linkable Keratin Hydrogels for Stem Cell Encapsulation,” Biomacromolecules, vol. 18, no. 2, pp. 398–412, Dec. 2016. 

[4] A. Isaacson, S. Swioklo, and C. J. Connon, “3D bioprinting of a corneal stroma equivalent,” Experimental Eye Research, vol. 173, pp. 188–193, Aug. 2018. 

[5] S. Shafaie, V. Hutter, M. T. Cook, M. B. Brown, and D. Y. S. Chau, “In Vitro Cell Models for Ophthalmic Drug Development Applications,” Biores Open Access, vol. 5, no. 1, pp. 94–108, Apr. 2016, doi: 10.1089/biores.2016.0008.



