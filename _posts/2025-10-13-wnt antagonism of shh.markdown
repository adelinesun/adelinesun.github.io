---
layout: post
title:  "Cre-LoxP offers insights on critical windows in mouse embryonic development"
date:   2025-10-20 09:53:00 -0700
categories: lit review
---

Written by Adeline Sun


<span style="color:blue">While reading this paper for class, an experiment stood out to me as a clever way to study critical time windows in embryonic development using different Cre drivers. </span>

<br>

![fig3](/images/2025-10-13-wnt antagonism of shh.png)

<br>

This paper was published in 2009. Dr. Milan Joksimovic is now with the Department of Cell Biology, Neurobiology and Anatomy at the Medical College of Wisconsin. At time of publication, he was working in Dr. Rajeshwar Awatramani, a professor of neurology at the Northwestern University Feinberg School of Medicine.

<br>

## **Context** 
1. The ***Ctnnb1*** gene encodes **β catenin**, the key transcription factor in the **canonical Wnt signaling pathway**. Under basal conditions, β-catenin is constitutively degraded by the proteasome. When Wnt ligand binds to its membrane receptor, the β-catenin "destruction complex" is phosphorylated, β-catenin accumulates in the cytosol and moves into the nucleus where it activates expression of TCF transcription factors. A major result of this paper is that Wnt is sufficient in promoting dopaminergic neurogenesis in the neural tube floorplate. 

2. Biologically, Shh is expressed in the midbrain floor plate before gradually disappearing between **9.5 dpc to 11.5 dpc**.

3. **Nestin** is expressed in neural progenitor cells **starting from 11.5-12.5 dpc**.


## **Methods**

1. **Shh::Cre; Shh conditional knockout (cKO)** - Conditional deletion of Shh using a Shh-Cre driver. Shh is knocked out at the first instance of Shh expression.
2. **Shh::Cre; Ctnnb1 conditional knockout (cKO)** - Conditional deletion of Ctnnb1 using a Shh-Cre driver. Ctnnb1 gene is knocked out at the first instance of Shh expression. 
3. **Shh::Cre; Ctnnb1 lox(ex3) conditional knockout (cKO)** - Conditional deletion of Ctnnb1 exon 3 using a Shh-Cre driver. When exon 3 is knocked out, β-catenin can no longer be phosphorylated and degraded.
4. **Nestin::Cre; Ctnnb1 cKO** - Conditional deletion of Ctnnb1 exon 3 using a Nestin-Cre driver. 
5. **BrdU pulse labeling** - BrdU is a synthetic thymidine analog used to lineage trace proliferating cells. Pregnant dams were injected with BrdU, and embryos were harvested an hour later.
6. **Ngn2 immunohistochemistry** - Ngn2 is a dopaminergic progenitor marker. 1:25 dilution was used.

![fig1](/images/2025-10-13-wnt antagonism of shh cre loxp diagram.jpeg)
##### (Khan Academy, n.d.). Schematic of the Cre-LoxP recombination system. Cre recombinase recognizes LoxP sites and excises the DNA sequence that lies between them. 

A Shh-Cre::Ctnnb1 cKO mouse describes a mouse in which Cre is expressed under the control of the Shh promoter and in which Ctnnb1 is flanked by a LoxP-STOP-LoxP sequence, has been inserted into the Rosa26 locus. In animals expressing both constructs, Cre specifically activates the reporter in cells that express the promoter by excising the STOP sequence.


## **Results**

#### BrdU pulse labeling detects proliferating cells. Ngn2 is a proneural gene marker

Left half of figure: 
- Shh is normally expressed in the **hindbrain** floor plate at 11.5 dpc. <span style="color:red">Proliferation and differentiation are not observed.</span> 
- In **Shh::Cre; Shh cKO** mutant embryos, Shh expression is expectedly abolished. <span style="color:green">Ectopic proliferation and differentiation are observed.</span>
- In **Shh::Cre; Ctnnb1 lox(ex3) cKO** mutant embyros, β-catenin exon 3 is deleted. β-catenin can no longer be degraded, permanently activating the Wnt/β-catenin signaling pathway. <span style="color:green">Ectopic proliferation and differentiation are observed.</span>

Right half of figure: 
- Shh is *not* normally expressed in the midbrain floor plate at 11.5 dpc. <span style="color:green">Proliferation and differentiation are observed.</span>
- In Shh::Cre; Ctnnb1 cKO (referred to as **Shh::Cre; Ctnnb1 cKO**) mutant embryos, Shh is *ectopically* expressed in the midbrain floor plate at 11.5 dpc. <span style="color:red">Proliferation and differentiation are not observed.</span>
- <span style = "color:blue">**Surprising**</span>: On the other hand, the midbrain floor plate of **Nestin::Cre; Ctnnb1 cKO** embryos developed normally.




![fig2](/images/2025-10-13-wnt antagonism of shh fig3.png)


## **Discussion**

1. Left half: Shh expression is necessary for suppressing proliferation and differentation of floor plate neurons.
2. Right half: Wnt signaling is nessecary for promoting proliferation and differentation of floor plate neurons
3. Coolest part: β-catenin knockout at 9.5 dpc abolished midbrain dopaminergic neurogenesis, while deletion after 11.5 dpc had no effect. <br><span style = "color:blue">**β-catenin signaling is required within a critical period between 9.5 dpc and 11.5 dpc to achieve normal dopaminergic neuron development.**</span>

<br>


## **Closing thoughts**
Nestin was chosen as the Cre driver to delay β-catenin knockout by a couple of days. I was impressed because this design choise is only possible with the knowledge that Nestin is expressed in floor plate cells later than Shh. In retrospect, spatio-temporal considerations in Cre driver selection probably come second nature to experienced researchers. After all, the use of Nestin::Cre was hidden behind a single line in the paper. I still thought it was pretty cool, though.

Other food for thought: Why use Shh::Cre; Shh cKO instead of global knockout?

References:

Joksimovic, M., Yun, B. A., Kittappa, R., Anderegg, A. M., Chang, W. W., Taketo, M. M., McKay, R. D., & Awatramani, R. B. (2009). Wnt antagonism of Shh facilitates midbrain floor plate neurogenesis. Nature Neuroscience, 12(2), 125–131. https://doi.org/10.1038/nn.2243 





