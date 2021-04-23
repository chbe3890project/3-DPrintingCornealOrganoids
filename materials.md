- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- [Software](/3-DPrintingCornealOrganoids/software)
- **[Materials](/3-DPrintingCornealOrganoids/materials)**

# Materials

## Rationale for materials selection
The cornea has 5 distinct layers, all of which have their own specific composition. Of the 5 layers, 3 are cellularized and contribute most to the function of the cornea. The bottom most layer is the endothelium, which is composed mostly of collagen. The middle layer is the stroma, and this layer contributes to the bulk of corneal thickness, and is also majorly composed of collagen. The main protein of the top layer, the epithelium, is keratin. An important function of the epithelium is to be at the air/liquid interface of the cornea, so the cells of this layer must have exposure to both air and the underlying hydrogel.

Since the main component of both the endothlium and stroma is collagen, the hydrogel material for these layers will be Type I collagen. For the epithelium, a keratin-based hydrogel using keratin extracted from hair will be used. Using a naturally occurring material that is found in these layers will better recapitulate the ECM to promote cell growth and organization, as well as create a platform that can be representative of in vivo corneas for drug screening.


## Chemistry: composition, crosslinking mechanism (UV radical initiation) and kinetics
The collagen-based gel for both the endothelium and stroma will be formulated from UV-crosslinkable [methacrylated collagen](https://advancedbiomatrix.com/photocol-irg.html) will be used for these layers of the print. The structure of the methacrylated collagen can be seen in Figure X. Briefly, the desired volume of photoinitiator (0.02%) will be solubilized in ethanol and mixed with the methacrylated collagen solution (8mg/mL; PhotoCol-Irg, Advanced BioMatrix, San Diego, CA) (Nguyen et al.). The endothelial layer will be cast in the well plate and cured, and then cells seeded directly onto the surface of the gel. The stromal layer will include encapsulated cells and will be printed directly onto the endothelial layer. 

The keratin-based epithelial layer will be composed of UV-crosslinkable allylated keratin. Keratin will be extracted from hair and allylated via two-step reaction consisting of oxidative elimination of sulfhydryl group of cysteine (−SH group) to Dha followed by the conversion of Dha to s-allyl cysteine was used to functionalize keratin at cysteine residues (Barati et al.). The structure can be seen in Figure X. Briefly, a solution of the allylated keratin in PBS (10 mg/mL) will be combined with the photoinitiator solution in PBS (0.75wt% keratin solution). The keratin extracellular matrix and cells that comprise the layer will be deposited in two steps: first, the acellular keratin hydrogel will be printed and cured directly onto the collagen-based stromal layer. Next, cells suspended in Matrigel will be printed onto the cured keratin layer to recapitulate the air/liquid interface of the epithelium. 

Both the collagen and keratin-based hydrogels will use Irgacure as a photoinitiator. Irgacure has shown to be an effective photoinitiator in bioprinting applications. It allows the hydrogels to be crosslinked at 365nm UV light, which is within the range of wavelengths of UV suitable for gels encapsulating cells. Cure time for the collagen layers will include 30 minutes of thermal gelation at 37 degrees Celsius, followed by 1 minute of UV crosslinking. The keratin layer will be crosslinked with UV for 5 minutes immediately after deposition.


## Extrusion design/rate
- Extruder details (dimensions, components for each layer)
- Shear stress considerations

## GMP considerations
- Sterility: aseptic technique – separate bioreactors, new material/swapping between nozzles


## References
