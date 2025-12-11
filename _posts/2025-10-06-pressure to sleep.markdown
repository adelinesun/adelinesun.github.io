--- 
layout: post
title:  "You snooze you(r mitochondria) fuse"
date:   2025-10-06 09:53:00 -0700
categories: lit review
---
Written by Adeline Sun

<span style="color:green"> I came across this paper during the summer while studying mitochondrial dynamics with Prof. David Chan. In the age of massive datasets, I appreciated that the authors clearly de-emphasized the bioinformatics section in favor of mechanistic insights that those analyses made possible. </span>

<br>
![fig1](/images/2025-10-06-pressure to sleep.png)
<br>

**<span style="color:blue"> Dr. Raffaele Sarnataro is a postdoctoral scholar at the University of Oxford working in the Miesenböck group. He studies molecular and neural dynamics of sleep control. </span>**
<br><br>


## **Context** 
1. When NADH to NAD+ ratio is high, the mitochondria has a large protonmotive force but small demand for ATP. Excess electrons in the ETC leak prematurely from coenzyme Q, producing **ROS**.

2. In Drosophilia, neurons projecting to the **dorsal fan-shaped body** (dFBN) control sleep. These dFBNs have voltage-gated potassium channels that contain a redox-active subunit **Hyperkinetic** [<span style="color:blue">1</span>]. When dFBNs are in an OFF state during wakefulness, low ATP demand causes the leak of electrons from ETC and the generation of ROS (Kempf, 2019).

During wakefulnesss:<span style="color:red"> dFBNs accumulate ROS </span> &rarr; oxidation of NADPH-bound Hyperkinetic &rarr; K+ transport is impaired &rarr; dFBNs are hyperexcitable &rarr; **<span style="color:orange"> increased sleep pressure.</span>**

3. Mitochondria respond to stress from ROS by undergoing mitochondrial fission as a means of quality control. Fission/fusion also corrects mismatches between NADH supply and ATP demandby (Vance, 1990). Fission is thought to preclude mitophagy, the selective auto-degradation of damaged mitochondria by lysosome recruitment (Chan, 2020).


![fig2](/images/2025-10-06-hyperkinetic-A-redox-sensor-that-links-metabolism-to-sleep-homeostasis.png)
##### (Lyons & Rihel, 2020) Mechanism of Hyperkinetic and Shaker in response to ROS.

<br>


## **Methods**

1. **R23E10>mito-GFP** - **R23E10** is an enhancer fragment *selectively expressed in dFBNs* that regulate sleep in Drosophilia. Mito-GFP is GFP that localizes to the mitochondrial matrix. Here, flies expressing **R23E10-Gal4** are crossed with flies expressing Upstream Activating Sequence **(UAS)-mito-GFP**. In fly progeny, Gal4 binds the UAS and drives mito-GFP expression in dFBNs only. The presence of GAL4 without UAS by itself has little or no effect, and most cells have no UAS regions.

    <img src="/images/2025-10-06-gal4-driver-schematic.png" width="600">
    
    Schematic of UAS-Gal4 system. Created in Biorender.com.

<br>

2. Manipulating mitochondrial dynamics:
    **Inducing mitochondrial fission**: RNAi-mediated depletion of **Opa1** (fusion factor) or overexpression of **Drp1** (fission dynamin).
    **Inducing mitochondrial fusion**: **Drp1** conditional knockout in dFBNs or the overexpression of **Opa1**.

    <img src="/images/2025-10-06-fission-fussion-schematic.png" width="600">

    Mitochondrial factors affecting fusion and fission

<br>

3. **Optical photon reassignment microscopy (OPRM)** - a type of **super resolution microscopy** that adds an intermediate optical beam expansion to conventional confocal laser scanning microscopy (CLSM) based on the insight that the most probable position of detected photons is midway between the excitation point and detection point. This is contrary to a CLSM where all detected photons are assigned to the nominal excitation position. Here, OPRM provided "lateral super-resolution approximately twofold above the diffraction limit" for visualizing mitochondrial morphology (Roth, 2013).

![fig4](/images/2025-10-06-OPRM.png)
    Case in point: (a) uses OPRM. (b) uses CLSM. Scale bar is 5um,

<br>

## **Results**

#### Figure 3. Sleep pressure alters mitochondrial dynamics

Flies were sleep deprived through mechanical agitation or increased dopamine firing through an arousing heat stimulus. OPRM and volumetric renderings helped visualize mitochondrial morphology thorughout the neuron.
“A night of sleep loss... reduced the size, elongation and branching of dFBN mitochondria (Fig 3a) and led to the localization of fission dynamin Drp1 from the cytosol to the mitochondrial surface (Fig 3c)." **Sleep loss results in increased mitochondrial fission.**

Question: Is sleep &rarr; fission a secondary effect or a compensatory mechanism toward restoring normalcy?

Experiments showed that sleep deprivation also increase mitochondrial-ER contact points and recruitment of the lysosome, both indicative of increased mitophagy (data not shown here). Here, the authors made an interesting remark: increased mitochondrial–ER contact may also indicate enhanced **mitochondrial biogenesis**, *which would explain* the abundance of transcripts for mitochondrial proteins observed in the RNA-seq data.

Question: How does the cell signal mitochondrial biogenesis? Is it an autoregulatory mechanism like mitophagy?


![fig5](/images/2025-10-06-fig3a.png)
##### Volumetric renderings of automatically detected mitochondria in OPRM image stacks of dFBN dendrites in rested flies, sleep-deprived flies, and flies recovered from sleep deprivation. 


<img src="/images/2025-10-06-fig3c.png" width="500">

<br>


### Figure 4. Mitochondrial dynamics alter sleep pressure

Note: Zeitgeber time is a 24-hour notation for tracking an organism's circadian rhythm, where ZT 0 represents the start of the light (day) phase and ZT 12 is the start of the dark (night) phase. 

Also note: neurons studied here are noted as $R23E10 \cap VGlut$ to describe a subpopulation of R23E10-containing dFBNs that are also glutaminergic, thus excluding the GABAergic dFBNs that didn't seem to be involved in showing mitochondrial changes to sleep. 

Fig 4b shows that Drp1 overexpression decreased the fly's sleep time and Opa1 overexpression increased sleep time. Fig 4c establishes the same narrative. **Artificially induced fission decreases sleep pressure, and fusion increases sleep pressure.**

![fig7](/images/2025-10-06-fig4bc.png)

Daily sleep time in flies expressing R23E10 ∩ VGlut-GAL4-driven fission or fusion proteins or RNAi transgenes and their parental controls. Manipulations that increase fission are green, and manipuations that increase are blue. Green and blue alter sleep in opposite directions.

<br>

**Electrophysiology**:

Whole-cell patch-clamp recordings were made on GFP-labeled dFBNs in vivo. Concordant with behavioral results, Fig 4e shows that Drp1 overexpression decreased the amount of spiking frequency of Glutaminergic dFBNs, while Opa1 overexpression increased it.

<img src="/images/2025-10-06-fig4e.png" width="400">
Voltage responses to current steps of dFBNs

## **Discussion**

"An overwhelming sense of tiredness (which is unrelated to muscle fatigue) is in fact a common symptom of human mitochondrial disease." 

Question: Is tiredness in mitochondrial diseases a result of poor fission?

"In the mammalian hypothalamus, populations of orexigenic neurons expressing agouti-related protein (AgRP) and anorexigenic neurons expressing pro-opiomelanocortin undergo antiphasic cycles of fission and fusion... Deletions of mitofusins from AgRP neurons impair the consumption of food , just as interference with mitochondrial fusion in dFBNs impairs the induction of sleep." 

Question: Are other cyclic behaviors also regulated by mitochondria and Hyperkinetic?

<br>

## **Closing thoughts**

When reading this paper, I thought back to Dr.Ying-Hui Fu's studies on superhumans, those who function on 4-6 hr of sleep per night, are healthier than average, and carry a lower risk of AD. Additionally, I was also reminded of Dr. David Holtzman's studies showing that sleep deprivation increases Aβ and tau in AD mice. 

Food for thought: Do people with more efficient mitochondria sleep less? Does more efficient mitochondria lead to protection from AD? Maybe superhumans are a result of having more fiss-able mitochondria!

<br>

One of the biggest challenges in studying cellular changes is establishing whether a given alteration, such as abnormal neuronal activity or differential gene expression, is a cause or merely a consequence of another process. I think this paper did an excellent job of avoiding this pitfall by showing a strong bidirectional relationship between mitochondrial dynamics and sleep behavior.

As they say, it's always the mitochondria!

<br>

**Works Cited**

* Roth, S., Sheppard, C., Wicker, K. et al. Optical Photon Reassignment Microscopy (OPRA). arXiv:1306.6230. (2013)
* Kempf, A., Song, S.M., Talbot, C.B. et al. A potassium channel β-subunit couples mitochondrial electron transport to sleep. Nature 568, 230–234 (2019).
* Lyons, D. G., & Rihel, J. (2020). Sleep circuits and physiology in non-mammalian systems. Current Opinion in Physiology, 15, 245–255.
* Vance, J. E. Phospholipid synthesis in a membrane fraction associated with mitochondria. J. Biol. Chem. 265, 7248–7256 (1990).
* Chan, D. C. (2020). Mitochondrial dynamics and its involvement in disease. Annual Review of Pathology: Mechanisms of Disease, 15(1), 235–259.


## Comments
<div id="comments"></div>

<script src="https://utteranc.es/client.js"
        repo="adelinesun/adelinesun.github.io"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>