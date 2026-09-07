---
title: 'Microdosimetry'
date: 2018-06-01 10:00:00
description: Overview of my research in microdosimetry.
featured_image: '/images/Microdosimetry-Research/Microdosimetry.jpg'
category: research
---
<div class="post-body" markdown="1">


## <a id="top"></a>Quick links / on this page

- [Introduction](#intro){: .custom-link-style }

**Photon microdosimetry:** 
- [Project 1: Development of 3D models based on clinical pathology slices](#p1){: .custom-link-style }
- [Project 2: Patient-specific microdosimetry](#p2){: .custom-link-style }

**Proton and heavy ion microdosimetry:** 
- [Project 3: GPU-accelerated proton microdosimetry](#p3){: .custom-link-style }
- [Project 4: Proton microdosimetry in RayStation TPS](#p4){: .custom-link-style }

## <a id="intro"></a> Introduction 

Microdosimetry refers to the study of the statistical properties of energy deposition by ionizing radiation. In general, the goal of microdosimetry studies is to be able to better characterize what the biological effects of ionizing radiation will be by enhancing our understanding of their energy deposition properties. I started my work in microdosimetry in the summer of 2018 at McGill University. I continued my work in microdosimetry through my PhD studies at MD Anderson and continue to work on related topics through to the present day.

## <a id="p1"></a> Development of 3D models based on clinical pathology slices 
The first project I worked on in the microdosimetry space involved showing that the calculation of patient-specific microdosimetric spectra (i.e. lineal energy or specific energy spectra) was possible. In order to do this, I had to develop an image analysis framework to extract information from scanned histopathological samples. As part of this work I developed an algorithm which extracted center-to-center spacing from stained haemotoxylin and eosin slides to yield cellular spacing, as well as using color channel analysis to determine the nucleus diameter:
<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Method1_2.png" style="max-width: 100%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Three panel image showing the extraction of cellular centers, cellular diameter, and then on the right, nucleus content from H&E stained slides.
  </figcaption>
</figure>
With cell and nucleus size information, I performed a pouring simulation using a molecular dynamics simulator (LAMMPS). Spheres corresponding to cellular volumes were "poured" into a box and interacted dynamically to make a highly compacted three dimensional model. Within each sphere the distribution of nucleus size was randomly sampled and placed in order to generate a model containing both cells and nuclei that are representative of a patient's cell/nucleus size.
<figure class="expanded-gif">
  <img src="/images/Microdosimetry-Research/pouring.gif" alt="Pouring simulation">
  <figcaption>
    <strong>Above:</strong> Animation of the pouring simulation to make 3D cellular models.
  </figcaption>
</figure>
This work was published in Physica Medica:
<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Paper1.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of my article on development of 3D models for microdosimetry.
  </figcaption>
</figure>

## <a id="p2"></a> Patient-specific microdosimetry 
Taking the three dimensional models developed above, I then created a Geant4-based user application entitled "MicroTrack". MicroTrack can take generic cellular volumes or three dimensional models based upon a patient's own cell and nucleus size and determine energy deposition by ionizing radiation within those models. Using MicroTrack we calculated patient-specific lineal energy depositions for some common and experimental brachtherapy sources including Cobalt-60, Iridium-192, Ytterbium-169, and Iodine-125:
<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Method2.jpg" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Patient specific lineal energy distributions for various brachytherapy isotopes.
  </figcaption>
</figure>

We were able to show for the first time, that determination of patient-specific microdosimetric distributions is possible. We published on this work in Physics in Medicine and biology:

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Paper2.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of my article on patient-specific microdosimetry in PMB.
  </figcaption>
</figure>

## <a id="p3"></a> GPU-accelerated proton microdosimetry 
Moving into my PhD studies at The University of Texas MD Anderson Cancer Center (MDA), I focused my attention on proton therapy rather than brachytherapy as I had formerly specialized. Early in my time at MDA it was becoming clear to me and others that the use of the quantity dose-averaged linear energy transfer (LET) had some major shortcomings that may hinder predictions of proton relative biological effectiveness (RBE) which are made with it. The obvious solution (in my opinion biased towards microdosimetry) was to use microdosimetric quantities like lineal energy rather than dose-averaged LET.

The key barrier standing in the way of this is that the calculation of microdosimetric quantities is enormously computational expensive (or was at the time in 2020). Because of this, I developed SuperTrack. SuperTrack is a GPU-accelerated (developed with CUDA) application for the rapid calculation of proton and heavy ion microdosimetry.
<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Method3.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> A slide that I commonly present when showing off SuperTrack.
  </figcaption>
</figure>
Using SuperTrack, we were able to generate proton lineal energy spectra which were indistinguishable from those generated by Geant4 and agreed with experimental studies in the literature. However, SuperTrack is up to 5000x faster than using Geant4 directly (depending on how many times you re-use the tracks). With SuperTrack we created the largest known library of proton lineal energy spectra (at the time) and showed how this library could be used to calcualte proton lineal energy spectra on a voxel-by-voxel level. We published on this work in PMB:
<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Paper3.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> My article in PMB describing SuperTrack and the library of proton lineal energy spectra we calculated.
  </figcaption>
</figure>

## <a id="p4"></a> Proton microdosimetry in RayStation TPS
In the months following the publication of my work on SuperTrack I had a very fortunate encounter with Erik Traneus of RaySearch AB. He was invited to join one of our group meetings, under my PhD advisor Dr. Radhe Mohan. He recounted how he was interested in integrating the calculation of proton lineal energy spectra into the RayStation treatment planning system, however he needed a library of lineal energy spectra for monoenergetic protons in order to make this happen. I almost jumped out of my seat. What a fortunate encounter, I had already computed exactly that library (more or less).

In the months to come I expanded the library of proton lineal energy spectra up to 300 MeV using new physics libraries incorporated into Geant4-DNA. I also spent my time at the International Congress for Radiation Research (ICCR) 2023 in Montreal trying my best to track down an experimental microdosimetrist who would share data with me to experimentally validate my calculations of proton lineal energy spectra. I was extremely fortunate to meet Dr. Marta Missiaggia that year, who became a collaborator and a friend, and was willing to share her experimental measurements of proton lineal energy spectra with me.

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Method4.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Comparison of methods for determination of proton lineal energy spectra along a proton spread-out bragg peak. SuperTrack (blue) is compared to Marta's measurements (black line) and our model incorporated into RayStation IonPG (red line).
  </figcaption>
</figure>
Later that year we were able to incorporate my technique for calculation of proton lineal energy spectra into RayStation-IonPG 2023B. Allowing for rapid, voxel-by-voxel determination of proton lineal energy spectra within a treatment planning system for the first time. We published on this work in Medical Physics:

<figure style="display: block; margin-left: auto; margin-right: auto; text-align: center; max-width: 800px;">
  <img src="/images/Microdosimetry-Research/Paper4.png" style="max-width: 85%; height: auto; display: inline-block;">
  <figcaption style="font-size: 0.85em; color: #666; margin-top: 8px;">
    <strong>Above:</strong> Header of my article on incorporating my work for calculation of proton lineal energy spectra into the RayStation TPS.
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

figure.expanded-gif {
  display: block;
  margin: 2rem auto;
  text-align: center;
  width: 100%;
  max-width: 350px; /* Adjust this value to set maximum width */

  img {
    width: 100% !important; /* Forces upscaling */
    height: auto !important;
    display: block;
    margin: 0 auto;
  }

  figcaption {
    font-size: 0.85em;
    color: #666;
    margin-top: 8px;
  }
}
</style>
