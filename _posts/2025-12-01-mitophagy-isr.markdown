--- 
layout: post
title:  "The odd one out? Mitochondria respond uniquely to the integrated stress response"
date:   2025-12-01 08:33:00 -0700
categories: lit review
---
Written by Adeline Sun

<br>
<span style="color:green"> This paper is authored by my previous mentor, Dr. Yoga Chakrabarty. It is a lovely paper that showcases mastery of experimental design. </span>

First, a cellular phenomenon is observed: HRI activity is necessary for DFP-induced mitophagy. Subsequent experiments show mitophagy is induced only when p-eIF2α is phosphorylated by HRI, complicating the question. Finally, more targeted approaches such as a chemically-induced dimerization assay provides a clearer understanding: p-eIF2α localization to the mitochondria is sufficient for mitophagy. Here, I look back on this paper and the design choices worth emulating.

**<span style="color:blue"> Dr. Yogaditya Chakrabarty is a postdoctoral scholar at the California Institute of Technology working in Professor David Chan's group. He studies autophagy of mitochondria and the ER in response to stress. </span>**
<br>

<br>
![fig1](/images/2025-12-01-hri-mitophagy paper.png) 
<br>
<hr>
<br>

[Context](#context)

[I. DFP-induced iron deprivation promotes mitophagy](#i-dfp-induced-iron-deprivation-promotes-mitophagy)

* Methods: mito-mKeima mitophagy reporter system
* Notable: Loss and rescue experiments using Balifomycin and Haemin strengthen causal inference: iron deficiency &rarr; mitophagy.

[II. The HRI branch of ISR is necessary for DFP-induced mitophagy](#ii-the-hri-branch-of-isr-is-necessary-for-dfp-induced-mitophagy)
* Methods: CRISPRi screen
* Notable: Deducing the role of a gene based on phenotypic effects of its knockdown
* Lingering questions: Why does eIF2B knockdown increase mitophagy levels?

[III. p-eIF2α, not common ISR outputs, promote mitophagy](#iii-p-eif2α-not-common-isr-outputs-promote-mitophagy)
* Methods: Puromycylation assay, translation inhibitors
* Notable: systematic treatment controls for puromycylation

[IV. p-eIF2α controls mitophagy, but only when activated via the HRI-ISR pathway](#iv-p-eif2α-controls-mitophagy-but-only-when-activated-via-the-hri-isr-pathway)
* Methods: ISR agonists and antagonists
* Notable: Salubrinal results imply basal HRI-mitophagy


[V. p-eIF2α localizes to the mitochondria only by the HRI branch](#v-p-eif2α-localizes-to-the-mitochondria-only-by-the-hri-branch)
* Methods: mitochondrial fractionation, colocalization measurements
* Notable: ER markers appears in the mitochondrial fraction, but not the other way around

[VI. Recruitment of p-eIF2α to mitochondria is sufficient to trigger mitophagy](#vi-recruitment-of-p-eif2α-to-mitochondria-is-sufficient-to-trigger-mitophagy)
* Methods: Rapalog-induced dimerization assay
* Notable: Use of phosphomimetic and phosmomutant protein variants

[Discussion](#discussion)

[Closing thoughts](#closing-thoughts)

<hr>
<br>

## Context

### **Mitophagy**

Autophagy of damaged mitochondria, or *mitophagy*, is a major degradation pathway in which damaged mitochondria is engulfed by an autophagosome and fuses with a lysosome. Mitophagy prevents the accumulation of defective mitochondria and is vital to the cell. 
In 2013, Allen et al. found that [**iron deficiency triggers mitophagy in primary human fibroblasts**](https://doi.org/10.1038/embor.2013.168). However, there has been few attempts to characterize this iron-responsive pathway.


**Known distinct mitophagy pathways:**
* Mitochondrial membrane depolarization &rarr; PINK1/Parkin-mediated mitophagy.
* Hypoxia &rarr; BNIP3L-NIX-mediated mitophagy.
* **Iron deficiency &rarr; ???-mediated mitophagy.**

<img src="/images/2025-12-01-PINK1-Parkin-schematic.png" width="700"> [Sekine & Youle 2018](https://doi.org/10.1186/s12915-017-0470-7) 
<h6> Mitophagy example: Pink1/Parkin pathway. PINK1/Parkin is activated when the mitochondrial membrane can no longer maintain a proton gradient and generate ATP effeciently. Under normal conditions, PINK1 is constitutively degraded after entering the mitochondrial matrix. When the proton motive foce is dissapated, PINK1 fails to import and activates a ubiquitination cascade on the mitochondrial surface that causes the recruitment of the autophagosome.</h6>


<br>

### **HRI branch of the integrated stress response**

Eukaryotic cells activate the integrated stress response (ISR) in response to a variety of stressors. The core event in this pathway is the phosphorylation of eukaryotic translation initiation factor 2 α (eIF2α) by one of four members of the eIF2α kinase family: heme-regulated eIF2α kinase (HRI), PKR-like ER kinase (PERK), general control non-depressible 2 (GCN2) and double stranded RNA dependent protein kinase (PKR). 

Phosphorylated eIF2α (p-eIF2α) decreases global translation and selectively upregulates expression of ATF4 and stress-responsive genes. HRI specifically responds to **loss of heme**, reflecting deficient cellular iron levels. 

**Cellular iron deficiency &rarr; reduced heme production &rarr; HRI kinase activity &rarr; ISR**


<img src="/images/2025-12-01-isr-detailed-schematic.png" width="500"> [Bravo-Jimenez 2025](https://doi.org/10.1186/s13024-025-00811-6)

<h6> ISR schematic. eIF2α kinases (PERK, PKR, GCN2, HRI) phosphorylate eIF2α (p-eIF2α) under different stressors. p-eIFα competitively inhibits eIF2B, the guanine nucleotide exchange factor for eIF2. This inhibits eIF2's abillity to deliver Met-tRNA to the ribosome, inhibiting protein synthesis. The common output of ISR is reduced global translation and selective upregulation of transcription factor ATF4. ATF4 forms dimers with other transcription factors and effects gene expression. </h6>

<br>

### **Mitochondria activate the HRI branch of ISR**
Mitochondria activate ISR pathway via the OMA1–DELE1–HRI signaling axis. When mitochondria are put under stress, DAP3-binding cell death enhancer 1 (DELE1) is cleaved by  m-AAA protease 1 homolog (OMA1) and released into the cytosol where it activates HRI and promotes ISR.

<img src="/images/2025-12-01-fig2a-hri-isr-schematic.png" width="500"> [Tremblay & Haynes 2020](
https://www.nature.com/articles/d41586-020-00552-0)
<h6>OMA1–DELE1–HRI signaling axis in the mitochondrial ISR. Mitochondrial stress activates the protease OMA1, which cleaves the inner-membrane protein DELE1. Cleaved DELE1 accumulates in the cytosol and binds the heme-regulated inhibitor kinase HRI, leading to HRI activation. Active HRI phosphorylates eIF2α, triggering ISR signaling and downstream transcriptional and translational responses.</h6>


<br>

<hr>\
**<span style="color: blue;">Knowledge gap: Is the HRI branch of ISR involved in mitophagy? If so, how? </span>**

<hr>
<br>

On to the paper...

### I. DFP-induced iron deprivation promotes mitophagy

#### **Methods**
* **Deferiprone (DFP)** is an iron chelator and is used to treat iron overload in thalassaemia major. Here, it is used to simulate iron starved conditions in the cell.

<img src="/images/2025-12-01-dfp.png" width="500"> [Waseem 2020](https://www.intechopen.com/chapters/77500)
<h6>Chelation of iron with Deferiprone.</h6>

* Mitophagy levels can be visualized and measured by red/green excitation ratio by **mito-mKeima reporter system.** Mito-mKeima is a a pH-sensitive fluorescent protein targeted to the mitochondrial matrix. It has a bimodal excitation spectra that shift from 440 nm in neutral mitochondria to 550 nm in acidic lysosomes. Mitophagy levels can be assessed with flow cytometry by the ratio of fluorescence at these two wavelengths. 

<img src="/images/2025-12-01-mKeima.png"> 
<h6> Fig S1B: Visualization of mitophagy with mito-mKeima . Images are post-digitally overlaid with red and green according to mKeima's bimodal excitation wavelengths. Fig 1A: Staining images of mito-mKeima expressing HeLa cells. Red mitochondria have a high acidic/neutral ratio. Fig S1D: Flow cytometry density plots for cells expressing mito-mKeima. The polygon indicates the gate used to score cells as positive for mitophagy.</h6>


#### **Results**

* mito-mKeima-expressing K562 cells treated with iron chelator DFP showed greater mitophagic activity (Fig 1B). This effect was dose-dependent (Fig S1B) and abrogated by the addition of Bafilomycin A1 (BFA1), a vacuolar H+-ATPase inhibitor that inhibits lysosome function and, by proxy, mitophagy.

* The addition of Haemin, a Fe3+ porphyrin carrier, also reduced mitophagy to basal levels, confirming that iron loss was the cause of DFP-induced mitophagy increase (Fig S1C).

<span style="color:blue">Note</span>: These loss-and-rescue experiments strengthens causal inference between iron levels and mitophagy.

<img src="/images/2025-12-01-fig1B.png">
<h6>Fig 1B: Quantification of mitophagy in mito-mKeima-expressing K562 cells by analysis of the mKeima acidic/neutral ratio with flow cytometry. BFA1 was used to block mitophagy. Fig S1B: K562 cells were treated with the indicated concentrations of DFP for 24 h, and mitophagy was quantified by flow cytometry. Fig S1C: Mitophagy levels in cells treated with both DFP and varied concentrations of haemin. P-value designations are as followed: ****, p≤0.0001; ***, p≤0.001; **, p≤0.01; *, p≤0.05; ns, p≥0.05. </h6>

<hr>
<br>

### II. The HRI branch of ISR is necessary for DFP-induced mitophagy

#### **Methods**

**CRISPRi mitophagy screen** - CRISPRi screen can pair large-scale sgRNA libraries with the CRISPR-dCas9-KRAB system to individually knock down many genes at once. Here, cells harboring the CRISPRi library were treated with DFP to induce mitophagy. 

<img src="/images/2025-12-01-fig1C-CRISPRi.png" width="700">
<h6>CRISPRi mitophagy screen schematic. Mito-mKeima-expressing K562 Cells were infected with CRISPRi library and treated with DFP. Cells showing the 25% lowest and highest mitophagy levels were collected for high-throughput sequencing.</h6>

<br>

#### **Results**

* The CRISPRi screen revealed that knockdowns of HRI, DAP3-binding cell death enhancer 1 (DELE1), and m-AAA protease 1 homolog (OMA1) significantly reduce mitophagy levels. This finding strongly suggests that **the OMA1-DELE1-HRI signaling axis is required for DFP-induced mitophagy** (Fig1D). Related sgRNAs include mitochondrial protein ABCB7, an iron-sulfer cluster transporter, and TOM20, a subunit of the outer mitochondrial membrane translocase. 

<img src="/images/2025-12-01-fig1D-HRI-components.png" width="550"> 
<h6> Fig 1D and Fig S1I: Results of from the CRISPRi screen. The x-axis denotes the mitophagy effect size, while the y axis denotes significance. The dotted line indicates the threshold for sgRNA hits, and hits of interest are labeled. Fig 1E: Validation of hits from mitophagy screen against non-targeting (NT) sgRNA control. P-value designations are as followed: ****, p≤0.0001; ***, p≤0.001; **, p≤0.01; *, p≤0.05; ns, p≥0.05.</h6>


* Note: Knocking down eIF2B subunits increased DFP-induced mitophagy. Because eIF2B loss functionally mimics p-eIF2α and activates the ISR. 

It's not immediately clear why eIF2B knockdown increases mitophagy beyond the level seen in DFP-treated controls. One possibility is that the treatment dosage used did not fully saturate ISR-dependent mitophagy, allowing eIF2B loss to further amplify translation inhibition. If inhibition of translation is the primary driver of mitophagy, it would suggest that the downstream consequences of p-eIF2α rather than p-eIF2α itself are important in this pathway. Note: **this is disproven by later experiments using ISRIB**

The article provides an alternative explanation: since eIF2B typically forms a stable complex with p-eIF2α, **<span style="color:green">the loss of eIF2B increases the amount of free-floating p-eIF2α. The presence of p-eIF itself regulates mitophagy.</span>** 

It might be interesting to measure mitophagy following eIF2B knockdown in the absence of DFP to examine eIF2B's involvement in basal mitophagy.

* p-eIF2α ⇒ eIF2B inhibition

* eIF2B knockdown → ↑ mitophagy

Lingering thoughts: Why did eIF2 not show up in the CRISPRi screen?

<hr>
<br>

**<span style="color:blue">...which brings us to the next question. Do common outputs of ISR control DFP-induced mitophagy? Or is it p-eIF2α itself?</span>**

### III. p-eIF2α, not common ISR outputs, promote mitophagy

#### **Methods**
* **Puromycylation assay** - uses puromycin, which mimics an aminoacyl-tRNA, to label actively translating ribosomes. The ribosome mistakenly incorporates puromycin, causing premature release of the polypeptide and tagging it with puromycin, which can be pulled down by an antibody. Here, puromycin served helped study how protein translation activity affects mitophagy.

<img src="/images/2025-12-01-puromycylation-assay-schematic.png" width="500"> [David 2012](https://doi.org/10.1083/jcb.201112145)
<h6>Puromycin is added to living cells, and nascent chains are tagged. Anti-puromycin monoclonal antibodies detect the puromycylated nascent chains thorugh indirect immunofluorescence.</h6>

* Translation inhibitors - harringtonine (Htn) and cycloheximide (CHX)

* ISR inhibitor - ISRIB prevents the formation of the p-eIF2α 


#### **Results**
ATF4 knockdown does not affect DFP-induced mitophagy (Fig2D). Neither do translation inhibitors harringtonine (Htn) and cycloheximide (CHX) (Fig2E). To further discrediting the role of Puromycylation assay confirms that DFP causes reduced translation (Fig S2I). Mitophagy is unaffected when cells are treated with ISRIB, ruling out the possibility that mitophagy is caused effects downstream of eIF2B inhibition. **Thus, the common outputs of ISR, including inhibition of eIF2B, are not sufficient in causing mitophagy.**

<img src="/images/2025-12-01-fig2D-isr-downstream.png">
<h6> Fig2D: sgRNA knockdown of ATF4 has no effect on DFP-induced mitophagy, measured by flow cytometry. Fig 2E: harringtonine (Htn) and cycloheximide (CHX) have no effect on mitophagy either. Fig S2I: Cells were exposed to to puromycin after treatment with DMSO, Htn, CHX, or DFP, as indicated. Cell lysates collected and analyzed by Western blot. Fig S2F: Effect of ISRIB treatment on mitophagy levels with and without DFP.</h6>

* Note: The pyromycylation assay assess puromycin levels for the following groups
    * Positive control: puro + control vehicle (DMSO for hydrophobic drugs)
    * Negative control: drug treatment without puro
    * Experiment: puro + treatment
<br>
<hr>
<br>

**<span style="color:blue">If not ISR outputs, mitophagy must be controlled by...</span>**

### IV. p-eIF2α controls mitophagy, but only when activated via the HRI-ISR pathway

#### **Methods** 

* **ISR agonists** - BTdCPU (BTd) activates HRI, BEPP activates PKR, CCT020312 (CCT) activates PERK, histidinol (Hst) activates GCN2. Salubrinal (Sal) inhibits p-eIFα phosphatases, sustaining ISR. Tunicamycin (Tun) and Thapsigargin (Tg) activate the PERK-ISR pathway by causing ER stress. Here, these drugs were used to study the relationship between different ISR branches and mitophagy.

<img src="/images/2025-12-01-fig3-HRI-specific.png" width="500"> 
<h6>A schematic of the chemical reagents activating the four branches of the ISR. Salubrinal (Sal) can increase p-eIF2α by inhibiting phosphatases regulated by GADD34 and CReP.</h6>

#### **Results**

Continuing this investigation of which component of HRI-ISR controls mitophagy, we then studied p-eIF2α. 

Knocking down HRI abrogated the expected increase in mitophagy levels observed in controls after both Sal or Btd treatment (Fig 3B). Consistent with the Sal result, overexpression of its target CReP suppressed DFP-induced mitophagy (Fig3D). When HRI is activated by BTd treatment, overexprssing CReP abrogates mitophagy levels. These opposing effects of Sal treatment and CReP overexpression suggest that **the level of p-eIF2α controls the level of mitophagy.**


* Note: The Sal result (Fig 3B) is interesting. Sal inhibits eIF2α phosphatases and sustains ISR signaling. Sal amplifies whatever kinase is active, so the fact that HRI knockdown decreases mitophagy after Sal treatment implies that HRI is active in basal cell conditions. 


Experiments detailed above showed that the HRI–DELE1–OMA1 axis is required for DFP-induced mitophagy. The next question is whether the other ISR branches, PERK, GCN2, and PKR, might contribute as well. Canonically, PERK is activated by ER stress and resides in the ER membrane. GCN2 is cytosolic and responds to amino acid deprivation through sensing uncharged tRNAs. PKR is also cytosolic and is activated by double-stranded RNA during antiviral responses. Although the CRISPRi screen did not identify these pathways, it gives no indication of whether these processes are capable of inducing mitophagy under any condition.

Cells were treated with PKR, PERK, or GCN2 agonists. In all cases, mitophagy levels remained unchanged. In contrast, activation of HRI by BtdCPU or indirectly through DFP treatment increased mitophagy, consistent with previous results (Fig 3D). **Together, these data support that p-eIFα activated by the HRI branch of ISR is uniquely required to drive mitophagy.**

<img src="/images/2025-12-01-fig3-HRI-specific-results.png" width="700"> 
<h6> Fig 3B: Mitophagy levels were assessed through flow cytometry after BTd or Sal treatment. Fig 3C:  ISR activity assessed by Western blot following BTd and Sal treatment. LC3B-II is the lipidated form of LC3B induced during autophagy. Fig 3D: p-eIF2α phosphatase CReP was overexpressed, leading to reduced mitophagy levels as expected. Fig 3E: Mitophagy was measured in K562 cells expressing after treatment with the indicated compounds. </h6>

<br>
<hr>
<br>

**<span style="color:blue">But why is the HRI branch of ISR exclusive in promoting mitophagy, even though p-eIF2α can be generated by all ISR kinases?</span>**

### V. p-eIF2α localizes to the mitochondria only by the HRI branch

There must be another factor specific to the HRI branch that regulates p-eIFα and mitophagy. Here, one hypothesis presented is that p-eIF2α localizes to the mitochondria only by HRI induction. 

While HRI is a cytosolic protein, it likely coordinates with the mitochondria due to the mitochondria's role as heme producers. Perhaps p-eIF2α affects mitophagy simply when it is in close proximity to the mitochondria.

#### Methods
* **Subcellular fractionation** - Mitochondrial, ER, and cytosolic cell fractions were isolated from cells by centrifugation. TOM20 and VDAC1 were selected as mitochondrial markers, and CNX was used as an ER marker.

* **Colocalization analysis** - Mander's coefficient was used to quantify the percent of p-eIF2α that occupies regions marked by TOM20 staining.

#### Results
**p-eIF2α was found in the mitochondrial fraction but not the cytosolic fraction after DFP treatment** (Fig 4A, 4B). When visualized through imaging, increased colocalization of p-eIF2α and TOM20. Additionally, ER stress caused by Thapsigargin (Tg) failed to cause comparable colocalization between TOM20 and p-eIF2α caused by Sal, BTd, or DFP. 

<img src="/images/2025-12-01-fig4-peif2a-localization.png" width="800">
<h6>Fig 4A: Mitochondrial and cytosolic subcellular fractions were collected and assessed for p-eIF2α, ATF4, and eIF2α expression. after DFP or Tg treatment. TOM20 is a mitochondrial marker, and a-TUB is the loading control. Fig 4B: Quantification of p-eIF2α mitochondrial localization by densitometric analysis. Fig S4C: p-eIF2α expression was assessed in mitochondrial, ER, and cytosolic fractions of Hela cells treated with DFP. 
Endoplasmic reticulum (ER) fractions were obtained by ultracentrifugation of postmitochondrial supernatant. Cyto-II denotes cytosolic supernatant of post-ER fractionation. CNX (Calnexin) and VDAC1 were used as ER and mitochondrial markers, respectively. Fig 4C: Staining of p-eIF2α in HeLa cells after DMSO, Tg, or DFP treamtents. Fig 4D: Colocalization between p-eIF2α and TOM20 were quantified by the mean Mander’s coefficient of 10 images per experiment. Two-way ANOVA was conducted for n=4 independent experiments. P-values are as followed: ****, p≤0.0001; ***, p≤0.001; **, p≤0.01; *, p≤0.05; ns, p≥0.05. </h6>


* The area occupied by p-eIF2α and TOM20 are morphologically similar (Fig 4C)
* Staining images were done in HeLa cells, while western blot was done in free floating K562 cells.

* Note: ER marker CNX appeared in the mitochondrial fraction, but mitochondrial marker VDAC1 did not appear in the ER fraction. This is a known phenomenon. ER → mitochondria contamination is common. Although CNX is an ER-resident chaperone, CNX-positive ER membranes form physical contacts with mitochondria. These contact sites co-pellet with mitochondria at 10,000 g. Since mitochondria are dense organelles, they pellet earlier and rarely appear in the ER fraction. 


<br>
<hr>
<br>


### VI. Recruitment of p-eIF2α to mitochondria is sufficient to trigger mitophagy

#### Methods
* **Rapalog-induced dimerization assay** - takes advantage of the ability of rapamycin to induce heterodimer formation between the FK506 binding protein (FKBP) and the FKBP-rapamycin binding (FRB) domain of the mammalian target of rapamycin (mTOR).

<img src="/images/2025-12-01-rapalog-schematic.jpg" width="500"> [Czapinksi, 2017](https://doi.org/10.3389/fchem.2017.00012)


#### Results

Cells were modified to express FKBP-GFP-HA-eIF2α and FRB-Fis1 fusion constructs containing wild-type (WT), phosphomimetic (S51D), or phosphomutant (S51A) eIF2α (Fig 5A). When rapalog is added, FKBP and FRB constructs shoud heterodimerize, bringing the eIF2α fusion protein to the mitochondrial surface. In both K562 cells (Fig 5B) and HeLa cells (Fig 5C), rapalog-induced localization of phosphomimetic p-eIF2α caused a significant increase in mitophagy. This increase was not observed in cells expressing WT nor phosphomutant eIF2α. **Thus, mitochondrial localization of p-eIF2α is sufficient to trigger mitophagy.**


* Note: eIF2α-S51D triggered mitophagy only after rapalog was added, strengthening causal inference between p-eIF2α localization and mitophagy.

**p-eIF2α &rarr; autophagy is unique to mitochondria.** 
When an analogous rapalog system was generated for peroxisomes using peroxisomal targeting sequence from PEX26, rapalog treatment successfully induced peroxisomal localization (Figure S5C), but it failed to promote pexophagy (Figure 5D). Thus, between peroxisomes and mitochondria, only the latter undergoes autodegradation in response to p-eIF2α targeting.

<img src="/images/2025-12-01-fig5-rapalog.png">
<h6> Fig 5A: Rapalog-induced FRB-FKBP dimerization assay and the expressed fusion constructs. FRB-hFis1 contained the mitochondrial targeting sequence of human Fis1. Mitophagy levels were measured in K562 cells (Fig 5B) or HeLa cells (Fig 5C) upon recruitment of eIF2α to mitochondria by rapalog treatment. eIF2αWT, eIF2αS51A (phosphomutant), or eIF2αS51D (phosphomimetic) eIF2α variants were analyzed. EtOH served as a vehicle control. Fig 5D: The rapalog system was generated for peroxisomes using an FRB construct fused to the peroxisomal targeting sequence of PEX26. Pexophagy was measured in cells contained peroxisomally targeted mKeima, analogous to mito-mKeima. Fig 5SB and 5SC: Immunostaining eIF2αS51A or eIF2αS51D upon rapalog treatment. GFP-tag was expressed in the eIF2α construct, Hsp60 is a mitochondrial marker, and PEX14 is a peroxisome marker.</h6>

<hr>
<br>

The paper goes on to conduct more experiments delineating p-eIFα's role in other mitophagy pathways. However, the core narrative is nearly complete by this point. For completeness-sake, here are some later findings involving PINK1/Parkin mitophagy and Hypoxia-induced (BNIP3) mitophagy:

* p-eIF2α accumulates in PINK1/PARKIN-mediated mitophagy as well, and knocking down HRI/OMA1/DELE1 abrogates it. However, HRI knockdown did not prevent PINK1/Parkin from localizing to the mitochondria, nor did it prevent the ubiquitination of the mitochondrial surface, the primary mechanism of autophagosome recruitment. In fact, overexpression of ubiquitin on the outer mitochondrial membrane was sufficient in driving mitophagy, even when HRI was knocked down. 

* Lastly, recruiting phosphomimetic eIF2α to mitochondria did not result in an increase in phospho-ubiquitin. Thus, the HRI/p-eIF2α mitophagy mechanism runs parallel but remains mechanistically distinct from ubiquitin-mediated PINK1/Parkin mitophagy

<br>
<hr>
<br>

## **Discussion**

Mitochondria play a crucial role in not only generating ATP but also in synthesizing iron-sulfur clusters used for enzymatic processes throughout the cell. As the central regulator of iron metabolism, mitochondria activate heme-regulated inhibitor (HRI) in response to iron deficiency. HRI then initiates the highly conserved integrated stress response (ISR), shifting the cell into a protective state. Failure to coordinate iron-responsive mitophagy signaling with mitophagy can be fatal. Impaired mitophagy causes dysfunctional mitochondria to accumulate and is a hallmark of neurodegenerative diseases such as Parkinson’s disease and frontotemporal dementia. 

**Here, the Chan group found that p-eIF2 is critical for mitophagy. However, p-eIF2 must also localize to the mitochondria for mitophagy to occur.** 

The paper notes that recent studies by [Sekine et al (2023)](https://doi.org/10.1016/j.molcel.2023.05.031) have shown that DELE1 may activate HRI at the mitochondrial surface. This suggests an attractive mechanistic explanation that p-EIF2 directly contacts the mitochondrial outer membrane. 

Some personal lingering questions:

* Why is the mitochondria "unique" in responding to p-eIF2? What components might mediate their interactions that are absent in peroxisomes? Can this be linked to mitochondria's evoluationary origins?

* What is the role of HRI-ISR in basal mitophagy i.e. mitophagy in unstressed cells?

* In treating cells with DFP, how can one separate the direct effects of iron deficiency versus downstream mitochondrial damage caused by heme loss? 

* What takes precedence in promoting mitophagy, ubiquitination or HRI-ISR components? Do they work synergistically?



<br>

## **Closing thoughts**

It can often feels like biology is too messy to study. Its complexity is part of what makes it fascinating, but it can also create a sense of impending doom for the experimentor. Zoologist Donald Griffin, who co-discovered bat sonar, once said that biologists are overly swayed by what he called “simplicity filters," i.e. the tendency to assume a result cannot possibly reflect the full picture because the underlying biology feels too complex to capture.

I often find myself falling into this trap, second-guessing whether the results of any single experiment represent a real biological phenomenon. I’ve realized that this is a dangerous mentality. Instead, it’s important to approach science with the understanding that everything can, in principle, be explained. 

A scientist’s explanations are shaped by the data they can collect, which in turn depend on the questions they ask and the controls they design. When the scope of a problem is too broad or overwhelmingly complex, one must narrow the question to something that can be answered with certainty. While modest differences in expression levels or measureable phenotypes can make someone wonder whether everything is just coincidence, good experimental design and technique is what ultimately provides confidence in whether those effects are real.

In cell biology especially, it is difficult to account for all the possible ways related pathways might interact. I appreciated that this paper characterized a single pathway piece by piece, identifying exactly which components of that pathway are critical and presenting a nuanced, spatially informed understanding of its mechanism. The techniques presented here showcase a mastery of experimental control, and I believe everyone can learn from it.
<br>

**Works Cited**

Chakrabarty, Y., Yang, Z., Chen, H. et al. The HRI branch of the integrated stress response selectively triggers mitophagy. Molecular Cell 85, 1090-1100.e6 (2024)