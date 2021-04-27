- **[Home](/3-DPrintingCornealOrganoids/index)**
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- [Electrical](/3-DPrintingCornealOrganoids/electrical)
- [Software](/3-DPrintingCornealOrganoids/software)
- [Materials](/3-DPrintingCornealOrganoids/materials)
- [Cells](/3-DPrintingCornealOrganoids/cells)

# Project Overview

## Summary
We designed a parsimonious bioprinting process to construct a packageable model of the human cornea that replicates the anatomy of this tissue system that is necessary for preclinical screening of ocular drug candidates. This process intensifies targeted culturing of human induced pluripotent stem cells (hIPSCs), differentiated into key cellular types of the corneal lamina, with sequential extrusion of these cells to form *in vitro* corneas with physiologically representative thickness of key layers. Herein, we believe our work represents an early opportunity to increase the quality of pharmacokinetic assessments of hits in the ophthalmic drug discovery space. Our use of 3D printing with tunable linear motion control, as well as our adoption of packageable approaches to cell management, support the reproducibility of the platform for which our goal is to demonstrate proof of concept. Therefore, our work also uses bioprinting in an attempt to address the central challenge of standardizing organoid technology.

## Significance
The ophthalmic drug development market is expected to reach $30.8B in revenue for fiscal year 2021, of which topically formulated agents are likely to retain 62% market revenue share. Of these agents, eye drops are projected to contribute 35% of market revenue share this year [1]. Therefore, the ophthalmic drug discovery space remains a lucrative opportunity for the pharmaceutical industry to invest in clinical candidate discovery. Enhanced approaches to hit discovery could improve both the quality and quantity of information on therapeutics for diseases of the eye, translating to increased probability of market breakthrough in these spaces. 

Therefore, we propose that the application of 3D models of the human cornea could more directly replicate human anatomy for characterization of therapeutic hits than the 2D, single-layer models presently employed in the ophthalmic drug development space [2]. The cornea is the first tissue layer that any ophthalmic drug contacts and is therefore critical to model in drug development, to characterize the absorption, distribution, and metabolism of potential therapeutics. Herein, more accurate models of drug interaction with the human cornea could allow for discovery of hits with higher potential for translation through clinical trials. Such 3D models would replicate the structurally and functionally diverse strata of the cornea displayed in the following image [3] far better than existing screening systems. We discuss the cellular and physiological profiles of these layers on the “Cells” and “Materials” sections of our website, respectively.

![Drawing of corneal anatomy](/3-DPrintingCornealOrganoids/CHBE3890/cornea-anatomy.png)

## Innovation
Our proposed design offers several advantages over existing techniques for corneal construct development, including the following items:

* We are developing elements of a drug screening platform.
  * A majority of previous research in corneal modeling has attempted clinical translation, intensifying designs with several complex elements of physiology that do not allow for reuse at earlier stages of drug development [4]. Therefore, there remains a general lack of anatomically representative models of the cornea to empower ocular drug screening, despite the associated market size.

* We employ hIPSCs.
  * As we discuss in “Cells,” most models of the human cornea poised for drug screening use terminally differentiated cells from patients (which are expensive and comprise cellular memory) or animal model cell lines (which are not sufficiently representative of human physiology).

* We model 3 layers of the cornea, to better allow for characterization of drug transport within this tissue system.
  * Most papers have focused on modeling 1 layer, in great depth, *in vitro* [5].

* We employ extrusion printing to deposit organoids in each layer of our construct.
  * A central challenge with organoid technology is standardization, which can complicate attempts to use organoids for drug screening. Bioplotting can help provide standardization via automated control of the printing process. Bioplotting is a very pliable method of printing for establishing proof of concept and therefore fits the purpose of our design project.
  * There remain few papers that have attempted 3D printing of the cornea, most of which have only tackled one layer of the tissue system and do not incorporate the intentionality and cellularity we describe above.

## Approach
To satisfy the drug screening purpose of our design, we sought to develop conceptual setting 3 within the fabrication timeline in the figure below [4]:

![Drawing explaining different levels of complexity among fabricated corneas](/3-DPrintingCornealOrganoids/CHBE3890/fabrication-levels.png)

Details about our model construction are available on the tabs linked above. Briefly, our process considers hIPSCs differentiated to the epithelial, stromal, and endothelial subtypes of corneal cells within separate bioreactors. We validate cell identity following differentiation using immunohistochemistry methods. Then, we apply a syringe pump adapted from an open-source design to print each layer of cells in an order representing the natural anatomy of these layers, with relative thickness of each layer that is also physiologically representative. We print atop a glass support and maintain the epithelium as a thin air-liquid interface, mimicking the function of this layer in the human eye. Between printing each new layer, we allow for gelation of the previously-printed, natural bioink solution using UV light. Then, once we have a complete corneal construct, we validate its absorption using standard permeability assays, given our interest in developing a physiologically representative transport model for drug screening.

We hope our proof-of-concept model is both interesting and helpful to pharmaceutical scientists with an interest in the development of more physiologically representative models of the human eye. 

## References
[1] “Global Ophthalmic Drugs Market Size Report, 2021-2028.” [https://www.grandviewresearch.com/industry-analysis/ophthalmic-therapeutics-drug-market?utm_source=prnewswire&utm_medium=referral&utm_campaign=hc_15-feb-21&utm_term=ophthalmic-drugs-market&utm_content=rd](https://www.grandviewresearch.com/industry-analysis/ophthalmic-therapeutics-drug-market?utm_source=prnewswire&utm_medium=referral&utm_campaign=hc_15-feb-21&utm_term=ophthalmic-drugs-market&utm_content=rd) (accessed Apr. 26, 2021).

[2] J. W. Foster, K. Wahlin, S. M. Adams, D. E. Birk, D. J. Zack, and S. Chakravarti, “Cornea organoids from human induced pluripotent stem cells,” Sci. Rep., vol. 7, no. 1, Art. no. 1, Jan. 2017, doi: [10.1038/srep41286](10.1038/srep41286).

[3] “Corneal Anatomy, Symptoms, and Examination,” American Academy of Ophthalmology, Mar. 07, 2018. [https://www.aao.org/image/corneal-anatomy-symptoms-examination](https://www.aao.org/image/corneal-anatomy-symptoms-examination) (accessed Apr. 26, 2021).

[4] “3D bioprinting for artificial cornea: Challenges and perspectives - ScienceDirect.” [https://www.sciencedirect.com/science/article/abs/pii/S1350453319300888](https://www.sciencedirect.com/science/article/abs/pii/S1350453319300888) (accessed Apr. 26, 2021).

[5] O. S. Fenton, M. Paolini, J. L. Andresen, F. J. Müller, and R. Langer, “Outlooks on Three-Dimensional Printing for Ocular Biomaterials Research,” J. Ocul. Pharmacol. Ther., vol. 36, no. 1, pp. 7–17, Jun. 2019, doi: [10.1089/jop.2018.0142](10.1089/jop.2018.0142).
