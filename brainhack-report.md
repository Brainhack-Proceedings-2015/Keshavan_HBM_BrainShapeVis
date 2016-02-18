---
event: '2015 OHBM Hackathon (HI)'

title: 'Interactive online brain shape visualization'

author:

- initials: AK
  surname: Keshavan
  firstname: Anisha
  email: keshavan@berkeley.edu
  affiliation: aff1
  corref: aff1
- initials: AK
  surname: Klein
  firstname: Arno
  email: arno@binarybottle.com
  affiliation: aff2
- initials: BC
  surname: Cipollini
  firstname: Ben
  email: bcipolli@ucsd.edu
  affiliation: aff3

affiliations:

- id: aff1
  orgname: 'The UC Berkeley - UCSF Graduate Program in Bioengineering'
  street: 306 Stanley Hall #1762, University of California
  postcode: 94720
  city: Berkeley
  state: California
  country: USA
- id: aff2
  orgname: 'Sage Bionetworks'
  street: 1100 Fairview Avenue North, M1-C108
  postcode: 98109
  city: Seattle
  state: Washington
  country: USA
- id: aff3
  orgname: 'UC San Diego'
  street: 9500 Gilman Drive
  postcode: 92093
  city: La Jolla
  state: California
  country: USA

url: https://github.com/binarybottle/roygbiv

coi: None

acknow: The authors would like to thank the organizers and attendees of the 2015 OHBM Hackathon. This project is supported in part by a grant from the NSF (award 1429999).

contrib: AK and AK performed the project and wrote the report. BC extended this work and is actively maintaining ROYGBIV.

bibliography: brainhack-report

gigascience-ref: REFXXX
...

# Introduction
Our goal for the hackathon was to create an interactive Web browser application to visualize human brain image data processed by the [Mindboggle software package](url{http://mindboggle.info/)[1].

The Mindboggle project was initiated to improve the labeling as well as morphometry of brain imaging data, and to promote open science by making all data, software, and documentation freely and openly available. An interface for interactive visualization is essential for assessing issues in brain image processing and analysis, including surface reconstruction, labeling, and morphometry. Mindboggle processes human brain cortical surface meshes in the [VTK format](http://www.vtk.org/), and generates label and shape information for each anatomical region, where labels follow the Desikan-Killiany-Tourville protocol [2].

# Approach
Over the course of two afternoons at the Human Brain Mapping 2015 conference’s hackathon, we evaluated several JavaScript libraries for creating browser-based WebGL visualizations of brain surfaces, including [three.js](http://threejs.org/), [XTK](https://github.com/xtk/X\#readme), and [BrainBrowser](https://brainbrowser.cbrain.mcgill.ca/). Three.js was chosen for ease of use and degree of active development and community support. To accompany these surface visualizations with graphical plots, we chose the [d3 JavaScript library](http://d3js.org/) for its flexibility and widespread use.

# Results
We completed an initial version of our browser-based interactive visualization tool; a left hemisphere of a human brain is available at [http://roygbiv.mindboggle.info](http://roygbiv.mindboggle.info). Click and drag to rotate this brain, scroll to zoom in and out, and click on any region of the brain while pressing the shift key to produce an accompanying plot of shape measures for that region. This will render all other regions transparent. Shift-click outside the brain to return opacity to all regions.

![Example visualization](https://github.com/Brainhack-Proceedings-2015/Keshavan_HBM_BrainShapeVis/blob/master/roygbiv.png "Example visualization")


After the hackathon, we refactored the code to use an object-based approach. This allows multiple brains to be shown simultaneously. This approach was used to create a master-slave interaction: selection of a ROI in one hemisphere loads data for display on a second hemisphere. This approach was used in a [dynamic poster presented at Society for Neuroscience in 2015](http://cseweb.ucsd.edu/~bcipolli/docs/posters/SfN2015/) [3].


![Dynamic poster visualization](https://github.com/Brainhack-Proceedings-2015/Keshavan_HBM_BrainShapeVis/blob/master/rogybiv-master-slave.png "Example master/slave visualization")


# Conclusions

We have received very positive feedback for our efforts at the hackathon, and have since received several requests and encouragement to build this visualization out to accommodate other data besides shape information and to enable the visual evaluation of thousands of brains. We hope to continue this work with the help of others!


# References
[1] Klein, A., & Hirsch, J. (2005). Mindboggle: a scatterbrained approach to automate brain labeling. NeuroImage, 24(2), 261-280.
Chicago.
[2] Klein, A., & Tourville, J. (2012). 101 labeled brain images and a consistent human cortical labeling protocol. Front. Neurosci 6.171, 10-3389.
[3] Cipollini, B, Bartsch, H & Cottrell, G. (2015). Exploring the anatomy and genetics of cortical asymmetries in surface area and thickness. Society for Neuroscience, 2015.