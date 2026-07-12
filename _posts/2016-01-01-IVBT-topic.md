---
title: 'Intravascular Brachytherapy'
date: 2016-05-01 00:00:00
description: Overview of my research in Intravascular Brachytherapy.
featured_image: '/images/IVBT-Research/IVBT.jpg'
category: research
---
<div class="post-body" markdown="1">
Intravascular brachytherapy (IVBT), is a technique in which **radiation is delivered to arterial walls** after coronary angioplasty and stenting, in order **to prevent scar tissue** from growing which can cause the arterial vessel to close once again. I have had ongoing research projects in IVBT since I began working in medical physics in the summer of 2016.


<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 500px;">
  <img src="/images/IVBT-Research/IVBT_BetaCath.jpg" alt="IVBT BetaCath setup" style="max-width: 75%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Schematic diagram of the Novoste Beta-Cath 3.5F device. The only remaining device in use for IVBT treatments as of 2026.
  </figcaption>
</figure>

## Elucidating dosimetric causes of treatment failure in IVBT  
  
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

## Designing a new device for IVBT

One of the major shortcomings of existing IVBT devices that my prior study identified, is the directionally dependent dose-attenuation by the cardiac guidewire. Over lunch at a restaurant across the street from the McGill University Health Center in 2017, I drew a sketch on a napkin of an idea for an IVBT device where the guidewire traverses through the center of an IVBT device and no longer directionally attenuates the dose around the device.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 650px;">
  <img src="/images/IVBT-Research/MyDevice.jpg" alt="IVBT BetaCath setup" style="max-width: 75%; height: auto; display: inline-block;">
    <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Percentage dose change around a Novoste Beta-Cath device with external heterogeneities compared to dose in water.
  </figcaption>
</figure>

My colleagues were pretty enthusiastic about the idea so I decided to run with it. We published the schematics and standardized dosimetric values (reported using the AAPM TG-43 and TG-60 formalism) in an article entitled _A new delivery system to resolve dosimetric issues in intravascular brachytherapy_.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/IVBT-Research/Article2.png" alt="IVBT BetaCath setup" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of my article on the design of a new device for IVBT.
  </figcaption>
</figure>

Unsurprisingly, with this device we found that the dose
  
</div>

<style>
.post-body p, 
.post-body li {
    text-align: justify !important;
}
</style>
