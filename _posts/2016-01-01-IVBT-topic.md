---
title: 'Intravascular Brachytherapy'
date: 2016-05-01 00:00:00
description: Overview of my research in Intravascular Brachytherapy.
featured_image: '/images/IVBT-Research/IVBT.jpg'
category: research
---
<div class="post-body" markdown="1">

## <a id="top"></a>Quick links / on this page

- [Introduction](#intro){: .custom-link-style }
- [Project 1: Causes of treatment failure in IVBT](#paper1){: .custom-link-style }
- [Project 2: Designing a new device for IVBT](#paper2){: .custom-link-style }
- [Project 3: Creating the first IVBT treatment planning system](#paper3){: .custom-link-style }
- [Project 4: A prospective clinical trial on IVBT outcomes](#paper4){: .custom-link-style }

## <a id="intro"></a> Introduction 

Intravascular brachytherapy (IVBT), is a technique in which **radiation is delivered to arterial walls** after coronary angioplasty and stenting, in order **to prevent scar tissue** from growing which can cause the arterial vessel to close once again. I have had ongoing research projects in IVBT since I began working in medical physics in the summer of 2016.


<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 500px;">
  <img src="/images/IVBT-Research/IVBT_BetaCath.jpg" alt="IVBT BetaCath setup" style="max-width: 75%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Schematic diagram of the Novoste Beta-Cath 3.5F device. The only remaining device in use for IVBT treatments as of 2026.
  </figcaption>
</figure>

## <a id="paper1"></a> Elucidating dosimetric causes of treatment failure in IVBT  
  
The first project I embarked on in IVBT, involved **retrospective modelling of all FDA-approved beta-emitting IVBT devices**. I was interested in determining the extent to which our standard assumption for IVBT dosimetry, that all tissues and external devices around the radioactive source train could be considered water-equivalent was appropriate. In reality, calcified plaques lining the arterial walls, metallic cardiac guidewires which bring the device to the irradiated site, and metallic stents implanted all attenuate radiation which emanates from the device. We published on this work in an article entitled _A retrospective analysis of catheter-based sources in intravascular brachytherapy_.


<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/Article1.png" alt="IVBT BetaCath setup" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> My first article and first, first-authored article written back in ye olden days of 2016.
  </figcaption>
</figure>


In this study, I performed calculations using a Monte Carlo-based radiation transport technique to determine the amount of dose attenuated by heterogeneities around IVBT devices. I discovered that behind guidewires, plaques, and stents the dose delivered from an IVBT device was reduced by up to 70% compared to the expected dose delivered.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/NovostePercentDiff.jpg" alt="IVBT BetaCath setup" style="max-width: 75%; height: auto; display: inline-block;">
    <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Percentage dose change around a Novoste Beta-Cath device with external heterogeneities compared to dose in water.
  </figcaption>
</figure>

While none of the evidence from this study provides any causal information that compromised dosimetric outcomes lead to treatment failures, I find it pretty convincing suggestive information that with such severe dose "cold-spots" being common during therapy, that improving dosimetric outcomes could likely improve clinical outcomes as well.

## <a id="paper2"></a> Designing a new device for IVBT

One of the major shortcomings of existing IVBT devices that my prior study identified, is the directionally dependent dose-attenuation by the cardiac guidewire. Over lunch at a restaurant across the street from the McGill University Health Center in 2017, I drew a sketch on a napkin of an idea for an IVBT device where the guidewire traverses through the center of an IVBT device and no longer directionally attenuates the dose around the device.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 650px;">
  <img src="/images/IVBT-Research/MyDevice.jpg" alt="IVBT BetaCath setup" style="max-width: 75%; height: auto; display: inline-block;">
    <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Diagram of the new device for IVBT I designed.
  </figcaption>
</figure>

My colleagues were pretty enthusiastic about the idea so I decided to run with it. We published the schematics and standardized dosimetric values (reported using the AAPM TG-43 and TG-60 formalism) in an article entitled _A new delivery system to resolve dosimetric issues in intravascular brachytherapy_.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/Article2.png" alt="IVBT BetaCath setup" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of my article on the design of a new device for IVBT.
  </figcaption>
</figure>

Unsurprisingly, with this device we found that the dose was essentially uniform and unperturbed by any external guidewire. We were interested in the possibility of commercializing this device, but with Best Medical being the only current vendor in the market for IVBT devices they were uninterested in modifying a device which already works for them. Similarly, other vendors were uninterested in expanding in to what (at the time) seemed to be modality which was on the way out. 

## <a id="paper3"></a> Creating a treatment planning system for IVBT

Following my time at McGill, a graduate student, Maryam Rahbaran joined Dr. Enger's lab. She continued working on IVBT related projects. In collaboration with clinicians from the Brigham and Women's Hospital she embarked on a project to create the first treatment planning system for IVBT. Maryam integrated models of IVBT devices I had developed in Geant4 and elements of the Monte Carlo engine I had created in my prior work. Using optical coherence tomography (OCT) images taken prior to IVBT treatment, she was able to develop a digital three dimensional model of the coronary artery which was treated. These OCT images were then used for planning purposes. 

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/OCT.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Optical coherence tomography image of a coronary artery to be treated with IVBT. Various features are annotated.
  </figcaption>
</figure>

The treatment planning engine created was entitled RapidBrachyIVBT. We published on this work in Medical Physics in 2024.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/Article3.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of our article on RapidBrachyIVBT.
  </figcaption>
</figure>

Even with the existence of a treatment planning system (TPS) for IVBT in my opinion a major issue still remains; that being, unlike other forms of brachytherapy where we have multiple factors to optimize on like dwell position, needle position, etc. In IVBT, the guidewire lands wherever the cardiologist can get it. The only real factor we have that we can optimize on is time. In the next generation of IVBT research I expect we will see developments in means to center IVBT devices, directionally target their radiation, or optimize seed position within the coronary artery.

## <a id="paper4"></a> Prospective clinical trial on IVBT effectiveness

During my medical physics residency at the University of Washington, I was fortunate to work at the same institution as Dr. Kent Wallner. Dr. Wallner had emailed me almost a decade prior to my work at UW, recognizing that he and I were among the very few individuals still publishing articles on IVBT at the time. Dr. Wallner was enthusiastic about my presense at UW and immediately involved me with his ongoing research. I have been able to work with Dr. Wallner on his ongoing (as of 2026) prospective clinical protocol investigating clinical outcomes following IVBT.

The approach Dr. Wallner has taken is quite clever. Using what is referred to as an "N-of-1" approach, each patient receiving IVBT after recurrent drug eluting stent (DES) failure has their time to failure recorded after DES implantation. Then, once they receive IVBT each patient's time to failure following IVBT is recorded as well. I find that the results supporting the efficacy of IVBT to be stunning:

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/kaplan.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Kaplan-Meier curves of time to failure prior to IVBT vs. time to failure following IVBT.
  </figcaption>
</figure>

We have found that the median time to failure following DES implantation (96 days) more than triples after a patient receives IVBT (317 days). In 2026, we published on this work in Advances in Radiation Oncology.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/Article4.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of our article on initial findings of a prospective clinical trial related to IVBT efficacy.
  </figcaption>
</figure>

[Back to top](#)
  
</div>

<style>
.post-body p, 
.post-body li {
    text-align: justify !important;
}

a.custom-link-style {
font-weight: 400 !important;
color: #0192D4 !important; /* Red indicator color */
}
</style>
