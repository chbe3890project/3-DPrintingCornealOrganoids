- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- [Software](/3-DPrintingCornealOrganoids/software)
- [Materials](/3-DPrintingCornealOrganoids/materials)
- **[Cells](/3-DPrintingCornealOrganoids/cells)**


# Cells

## Rationale for cell populations

The cell types used in this Bioplotter were selected to meet the goals of corneal organoid production for drug screening. Many biomedical models utilize animal cells to mitigate ethical and financial concerns, but such models provide inaccurate physiological conditions due to species’ differences in protein expression and immunological response. The use of human-induced pluripotent stem cells (hiPSCs) allows for a readily expandable, robust and tunable model system capable of better recreating human physiology. hiPSCs offer a more clinically relevant drug screening platform due to their analogous developmental schemes and reproduction of many biological functions. The cost of such a model is expected to decline in the future as differentiation protocols are optimized and new small molecules are mass produced for cell varieties. 

Using hiPSCs, an initial cell line can be expanded and cultivated to produce cell populations for each of the three cellular layers printed using this Bioplotter. The cornea *in vivo* is avascular and capable of receiving nutrients and oxygen from surrounding tissue, thus bioprinted organoids do not require vascularization. Differentiation protocols for the endothelial, stromal, and epithelial layers are outlined below, but more detailed descriptions can be found in their respective sources at the bottom of this page. A list of required media and small molecules is also included. 

## Differentiation of hiPSCs


In brief, differentiated corneal endothelial cells are deposited on 12-well Transwell filters coated with Matrigel. The endothelium should be incubated for 2 days at 37 °C to allow the formation of a confluent monolayer. The first printed layer, comprising dispersed differentiated corneal keratinocytes, is deposited onto the endothelial monolayer. Corneal keratinocytes have been shown to organize into a stromal layer by directed self-assembly. Once the gel is cured, the acellular hydrogel support layer is printed. Finally, the differentiated epithelial cells are deposited on the hydrogel support. 

![Differentiation Flowchart](/3-DPrintingCornealOrganoids/CHBE3890/Flowchart.jpg)

A general workflow is shown below. Be sure to check sources for small molecule concentration and specific cell culture practices. 

**Endothelial Differentiation**

1. Culture hiPSCs in hESC Serum-free media until confluency
1. Change media to N2B27 priming media + bFGF
   1. Incubate for 2 days
3. Change media to N2B27 priming media + SB431542, LDN193189, IWP2
   1. Change fresh media daily for 6 days
4. Dissociate cells and transfer to new Matrigel coated plate
5. Change media to nueral crest induction media + CHIR
   1. Incubate for 2 days
6. Change media to CEC induction media + SB431542, H-1125

**Stromal Keratinocyte Differentiation**

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

**Corneal Epithelial Differentiation**

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b



## Validation using viability and activity assays

At least three wells in each batch of corneal organoids should be designated for cell viability and validation assays. The three samples should be collected after the endothelium reaches confluency, after the stromal layer is printed, and after the epithelial layer is printed, respectively.

Cell viability can be assessed using LIVE/DEAD imaging assays. Live cells are indicated by green-fluorescent calcein-AM and dead cells are indicated by red-fluorescent ethidium homodimer-1. Prep the LIVE/DEAD solution by mixing 1.25 uL of 4 mM calcein-AM and 2 mM of ethidium homodimer-1 in 10 mL of 1X PBS. Incubate completed organoid in 0.5 mL of the staining solution for 30 minutes at 37 °C. Images can be analyzed using the ImageJ Fiji macro “live dead quantification” by [Allevi3D](https://www.allevi3d.com/livedead-assay-quantification-fiji/).

Organoids can be removed at any stage in the printing process for validation of cell identities through immunohistochemistry. Excised filters can be carefully moved to microscope slides for staining. Samples should be washed twice with Tris Buffered Saline containing 0.1% Triton X-100 (TBS-T) and fixed in 4% PFA overnight at 4 °C. Samples can then be incubated in blocking solution consisting of 5% Donkey Serum in TBS-T for one hour at 37 °C. After three additional washes, primary antibody can be introduced and samples incubated overnight at 4 °C. After three additional washes appropriate secondary antibodies should be added and allowed to incubate for at least 1 hour at room temperature. Recommended primary antibodies are provided in the following table.

Cell Type | Primary Antibody 
------------ | -------------


Trans-corneal drug permeability is evaluated using diffusion experiments for three model drugs (pilocarpine hydrochloride [PHCl], hydrocortisone [HC], and befunolol hydrochloride [BHCl]). Diluted concentrations of each drug is administered to the Transwell media chamber and the cells are incubated for 420 minutes at 37 °C. Samples are collected from the lower media chamber every 60 minutes and quantitively analyzed using HPLC. Permeation parameters can be calculated by plotting amount of permeated drug (ug/sq. cm) over time. The slope of the linear portion of the permeation curve can be used to calculate the permeation coefficient Kp.

