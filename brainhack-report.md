---
event: '2015 OHBM Hackathon (HI)'

title:  'DueCredit: automated collection of citations for software, methods, and data'

author:

- initials: AK
  surname: Keshavan
  firstname: Anisha
  email: keshavan@berkeley.edu
  affiliation: aff1
  corref: aff1
- initials: ArK
  surname: Klein
  firstname: Arno
  email: arno@binarybottle.com 
  affiliation: aff2

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
  street: 110 Fairview Avenue North, M1-C815
  postcode: 98109
  city: Seattle
  state: Washington
  country: USA
  
url: https://github.com/duecredit/duecredit

coi: None

acknow: The authors would like to thank the organizers and attendees of the 2015 OHBM Hackathon. This project is supported in part by a grant from the NSF (award 1429999).

contrib: KA and KA performed the project and wrote the report.
  
bibliography: brainhack-report

gigascience-ref: REFXXX
...

#Introduction
Create an interactive Web browser application to visualize human brain image data processed by the Mindboggle software package\footnote{\url{http://mindboggle.info/}}.

The Mindboggle project was initiated to improve the labeling as well as morphometry of brain imaging data, and to promote open science by making all data, software, and documentation freely and openly available. An interface for interactive visualization is essential for assessing issues in brain image processing and analysis, including surface reconstruction, labeling, and morphometry. Mindboggle processes human brain cortical surface meshes in the VTK format\footnote{\url{http://www.vtk.org/}}, and generates label and shape information for each anatomical region, where labels follow the Desikan-Killiany-Tourville protocol\footnote{\url{http://mindboggle.info/data}}\cite{Klein2012}.

#Approach
Over the course of two afternoons at the Human Brain Mapping 2015 conference’s hackathon, we evaluated several JavaScript libraries for creating browser-based WebGL visualizations of brain surfaces, including three.js\footnote{\url{ http://threejs.org/}}, XTK\footnote{\url{https://github.com/xtk/X\#readme}}, and BrainBrowser\footnote{\url{https://brainbrowser.cbrain.mcgill.ca/}}. Three.js was chosen for ease of use and degree of active development and community support. To accompany these surface visualizations with graphical plots, we chose the d3 JavaScript library for its flexibility and widespread use\footnote{\url{http://d3js.org/}}.

#Results
The current version of our browser-based interactive visualization of a left hemisphere of a human brain is available at roygbiv.mindboggle.info. Click and drag to rotate this brain, scroll to zoom in and out, and click on any region of the brain while pressing the shift key to produce an accompanying plot of shape measures for that region. This will render all other regions transparent. Shift-click outside the brain to return opacity to all regions.

\begin{figure}[h!]
  \includegraphics[width=.42\textwidth]{roygbiv.png}
  \caption{\label{centfig} Example visualization.}
\end{figure}

# Conclusions
We have received very positive feedback on our efforts at the hackathon, and have since received several requests and encouragement to build this visualization out to accommodate other data besides shape information and to enable the visual evaluation of thousands of brains. We hope to continue this work with the help of others!