- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- [Software](/3-DPrintingCornealOrganoids/software)
- [Materials](/3-DPrintingCornealOrganoids/materials)
- **[Cells](/3-DPrintingCornealOrganoids/cells)**


# Cells

## Rationale for cell populations

The cell types used in this Bioplotter were selected to meet the goals of corneal organoid production for drug screening. Many biomedical models utilize animal cells to mitigate ethical and financial concerns, but such models provide inaccurate physiological conditions due to species’ differences in protein expression and immunological response. Current clinical models rely on primary sourced tissue from humans or animals, which often lose cellular functions and can be damaged during extraction. The use of human-induced pluripotent stem cells (hiPSCs) allows for a readily expandable, robust and tunable model system capable of better recreating human physiology. hiPSCs offer a more clinically relevant drug screening platform due to their analogous developmental schemes and reproduction of many biological functions. The cost of such a model is expected to decline in the future as differentiation protocols are optimized and new small molecules are mass produced for cell varieties. 

Using hiPSCs, an initial cell line can be expanded and cultivated to produce cell populations for each of the three cellular layers printed using this Bioplotter. The three cell lines should be maintained independently until fully differentiated, at which time they can be dissociated and prepared for the Bioplotter. The cornea *in vivo* is avascular and capable of receiving nutrients and oxygen from surrounding tissue, thus bioprinted organoids do not require vascularization. Differentiation protocols for the endothelial, stromal, and epithelial layers are outlined below, but more detailed descriptions can be found in their respective sources at the bottom of this page. A list of required media and small molecules is also included. 

## Differentiation of hiPSCs


![Differentiation Flowchart](/3-DPrintingCornealOrganoids/CHBE3890/Flowchart.jpg)

A general workflow is shown below. All plates should be coated with Matrigel unless otherwise stated. Be sure to check sources for small molecule concentration and specific cell culture practices. 

**Endothelial Differentiation [1]**

1. Culture hiPSCs in hESC Serum-free media until confluency
1. Change media to N2B27 priming media + bFGF
   1. Incubate for 2 days
3. Change media to N2B27 priming media + SB431542, LDN193189, IWP2
   1. Change fresh media daily for 6 days
4. Dissociate cells and transfer to new Matrigel coated plate
5. Change media to nueral crest induction media + CHIR
   1. Incubate for 2 days
6. Change media to CEC induction media + SB431542, H-1125
   1. Replace media daily until confluency

**Stromal Keratinocyte Differentiation [2,3]**

1. Culture hiPSCs in hESC Serum-free media until 60-80% confluency
1. Change media to KSR media + SB431542, LDN193189
   1. Replace media after 24 hr
3. Change media to KSR media + SB431542, LDN193189, CHIR 99021
4. After 24 hours, change media to KSR media + SB431542, CHIR 99021
5. After 24 hours, change media to a 75:25 mixture of KSR media + SB431542, CHIR 99021 and N2 media + CHIR
6. Every 48 hours, update mixture ratio by 25% until composition is 100% N2
7. Sort cells for HNK1+ and p75+ cells and transfer to new plate 
8. Replace media with Advanced DMEM + bFGF, ascorbic acid-2-phosphate
   1. Replace media every other day until confleuncy

**Corneal Epithelial Differentiation [4,5]**

1. Culture hiPSCs on laminin coated plates in Essential 8 media until confluency
1. Dissociate cells and transder to new plate with a halved concentration of laminin
   1. Change media to XF-ko-SR Media + GlutaMAX, mercaptoethanol, and blebbistatin
3. The next day, change media to XF-ko-SR Media + SB-505124 and bFGF
4. After 24 hours, change media to XF-ko-SR Media + BMP-4
   1. Replace media after 24 hours
5. Dissociate cells and transfer to new plate coated with laminin and collagen IV
   1. Change media to CnT-30, replace evey other day until confluency

**Bioplotting Workflow**

In brief, differentiated corneal endothelial cells are deposited on 12-well Transwell filters coated with Matrigel. The endothelium should be incubated for 2 days at 37 °C to allow the formation of a confluent monolayer. The first printed layer, comprising dispersed differentiated corneal keratinocytes, is deposited onto the endothelial monolayer. Corneal keratinocytes have been shown to organize into a stromal layer by directed self-assembly. Once the gel is cured, the acellular hydrogel support layer is printed. Finally, the differentiated epithelial cells are deposited on the hydrogel support. 

## Validation

At least three wells in each batch of corneal organoids should be designated for cell viability and validation assays. The three samples should be collected after the endothelium reaches confluency, after the stromal layer is printed, and after the epithelial layer is printed, respectively.

**Viability Assay**

Cell viability can be assessed using LIVE/DEAD imaging assays. Live cells are indicated by green-fluorescent calcein-AM and dead cells are indicated by red-fluorescent ethidium homodimer-1. Prep the LIVE/DEAD solution by mixing 1.25 uL of 4 mM calcein-AM and 2 mM of ethidium homodimer-1 in 10 mL of 1X PBS. Incubate completed organoid in 0.5 mL of the staining solution for 30 minutes at 37 °C. Images can be analyzed using the ImageJ Fiji macro “live dead quantification” by [Allevi3D](https://www.allevi3d.com/livedead-assay-quantification-fiji/). [6]

**Validation of Cell Populations**

Organoids can be removed at any stage in the printing process for validation of cell identities through immunohistochemistry. Excised filters can be carefully moved to microscope slides for staining. Samples should be washed twice with Tris Buffered Saline containing 0.1% Triton X-100 (TBS-T) and fixed in 4% PFA overnight at 4 °C. Samples can then be incubated in blocking solution consisting of 5% Donkey Serum in TBS-T for one hour at 37 °C. After three additional washes, primary antibody can be introduced and samples incubated overnight at 4 °C. After three additional washes appropriate secondary antibodies should be added and allowed to incubate for at least 1 hour at room temperature. Recommended primary antibodies are provided in the following table.

Cell Type | Primary Antibody Recommendations
------------ | -------------
Endothelial  | anti-Pax6; anti-Chx10; anti-Na/K ATPase
Stromal      | anti-Sox2; anti-P75; anti-keratocan
Epithelial   | anti-ck14; anti-p40

**Functional Assay**

Trans-corneal drug permeability is evaluated using diffusion experiments for three model drugs (pilocarpine hydrochloride [PHCl], hydrocortisone [HC], and befunolol hydrochloride [BHCl]). Diluted concentrations of each drug is administered to the Transwell media chamber and the cells are incubated for 420 minutes at 37 °C. Samples are collected from the lower media chamber every 60 minutes and quantitively analyzed using HPLC. Permeation parameters can be calculated by plotting amount of permeated drug (ug/sq. cm) over time. The slope of the linear portion of the permeation curve can be used to calculate the permeation coefficient Kp.


## Bill of Materials

**Media Required**

Item         | Vendor
------------ | -------------
hESC SFM     | StemPro
N2B27 Priming M.     | Thermo
Neural Crest Induction M.     | StemCell
CEC Induction M.     | Sigma
Knockout Serum Replacement (KSR) M.     | Thermo
N2 M.     | Thermo
Advanced DMEM     | Thermo
Essential 8 M.     | Thermo
Xeno free-knockout-SR M.     | Thermo
CnT-30 M.     | CELLnTEC

**Small Molecules Required**

Item         | Vendor
------------ | -------------
hESC SFM     | 1


## References

[1] Zhao, Jiagang J, and Natalie A Afshari. “Generation of Human Corneal Endothelial Cells via In Vitro Ocular Lineage Restriction of Pluripotent Stem Cells.” Investigative ophthalmology & visual science 57.15 (2016): 6878–6884. doi:10.1167/iovs.16-20024.

[2] Naylor, Richard W et al. “Derivation of Corneal Keratocyte-Like Cells from Human Induced Pluripotent Stem Cells.” PloS one 11.10 (2016). doi:10.1371/journal.pone.0165464.

[3] Chambers, Stuart M et al. “Dual-SMAD Inhibition/WNT Activation-Based Methods to Induce Neural Crest and Derivatives from Human Pluripotent Stem Cells.” Human Embryonic Stem Cell Protocols 1307 (2013): 329–343. doi:10.1007/7651_2013_59. 

[4] Puistola, Paula. “Novel bioink design for 3D bioprinting of human pluripotent stem cell derived corneal epithelial cells.” Tampere University Degree Programme in Bioengineering (Thesis). (2020). https://core.ac.uk/download/pdf/354675205.pdf. 

[5] Hongisto, Heidi et al. “Xeno- and Feeder-Free Differentiation of Human Pluripotent Stem Cells to Two Distinct Ocular Epithelial Cell Types Using Simple Modifications of One Method.” Stem cell research & therapy 8.1 (2017): 291–291. doi:10.1186/s13287-017-0738-4.

[6] Reichl, S, J Bednarz, and C C Müller-Goymann. “Human Corneal Equivalent as Cell Culture Model for in Vitro Drug Permeation Studies.” British journal of ophthalmology 88.4 (2004): 560–565. doi:10.1136/bjo.2003.028225.


