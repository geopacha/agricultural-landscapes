# AI-Assisted Agricultural Infrastructure Survey
## GeoPACHA Project

This project integrates Artificial Intelligence (AI) into the virtual archaeological survey of agricultural fields in the southern Peruvian Andes, significantly augmenting the capabilities of archaeologists to efficiently cover vast geographical areas through satellite imagery surveys. Leveraging computer vision methods such as Convolutional Neural Networks (CNN), the AI autonomously identifies potential archaeological features, empowering experts to focus their efforts on verifying identified features and providing rich contextual knowledge to ensure the accuracy and significance of the findings. This form of CNN-aided virtual survey will enable archaeologists to quickly and efficiently survey tens or hundreds of thousands of square kilometers. Systematic survey at this inter-regional scale promises to produce new insights into late prehistoric (~1000-1532 CE) and colonial-era (1532-1821 CE) patterns of agricultural use and abandonment, economic variation and change, and the effects of Spanish colonialism in the southern Peruvian Andes.

## Agricultural Infrastructure
Agricultural fields and terracing are visible in the satellite imagery, and their maintenance status (active or abandoned) can be estimated using patterns of color, texture, and morphology. The extent of agricultural fields provides important information about the capacity for agricultural production on the landscape, while the rate of field abandonment provides key insights into social and economic transformations as a result of Spanish colonialism. However, mapping the boundaries of field complexes manually is a highly laborious process due to the complexity and scale of agricultural field boundaries. We have therefore created a semantic segmentation model to extract the boundaries of field complexes autonomously and produce estimations of field maintenance status. 

![ActiveResultExample](https://github.com/geopacha/GeoPACHA_machine_learning/assets/10229337/5fc8856e-963f-4f22-863b-cab4e1994da0)

Overall, the performance of this model at large scales rivals that which is reasonably achievable by human surveyors, however, there is often greater uncertainty regarding field boundaries for abandoned field complexes, which by definition lack the clear edges of active fields. As a result, the segmentation model is less reliable for abandoned fields. The next phase of this research will seek to improve particularly this aspect of the model.

Training data for this project is adapted from [GeoPACHA](https://geopacha.org/), a geospatial platform for manual systematic archaeological surveys over large areas of Andean South America. The full project has identified over 300k loci of archaeological interest across Peru. We are currently making use of the data collected as a part of the Southwestern Survey Project, containing nearly 40k loci of interest for our project. We will be expanding these efforts to include a new survey region as well.

## Project Goals
Pre-process imagery for the new region.



## Data Sources
- Imagery sources: We are in the process of obtaining Worldview II and Worldview III imagery covering the entirety of the Southwestern Peruvian Andes. Some
  - Worldview II
	- 8 spectral bands
	- 0.5 m resolution
  - Worldview III
	- 8 spectral bands
	- 0.3 m resolution

- Worldview imagery is housed in *\\\sarlserver06.cas.vanderbilt.edu\sarl_commons\Wernke_projects\GeoPACHA\Imagery_Machine_Learning* and is broken up by tiles that divide up the area of interest (AOI) in the Southwestern Andes.
- Tile overviews can be accessed using the Survey_Grid_Tiles shapefile in *\\\sarlserver06.cas.vanderbilt.edu\sarl_commons\Wernke_projects\GeoPACHA\Imagery_Machine_Learning\shape overview*
- Individual tile overviews can be viewed in the *\shape* folder for each tiled area
- Archaeological sources:
  - GeoPACHA Large-scale manual satellite survey data
  - (Details coming)



## Workflows
- [MAXAR Image Acquisition Workflow](https://youtu.be/oaxFunbKA4c)
- [Image Acquisition Spreadsheet](https://docs.google.com/spreadsheets/d/1D92Sd_oLbBomKRKuALRMWLWqf6fLLxWr9SFWJf3F27Y/edit#gid=0)
- [QGIS Setup Workflow](https://docs.google.com/document/d/1SK9DXbr6gVPkzM0M_rDVCgYObmK2ejOZJFXKSCVxuIE/edit?usp=sharing)
- [Digitizing Checklist](https://docs.google.com/document/d/1hLVGL2H0IrT56D92zcFVxWgrKxHBe_T8IAhDiQmTrTo/edit?usp=sharing)
- [Digitizing Spreadsheet](https://docs.google.com/spreadsheets/d/1ZW_h8xf1GakVpdAY4lwGi2kErBv7rtg6MsphRBznDvo/edit?usp=sharing)


## Team Contact information
James Zimmer-Dauphinee (Anthropology)
[email](mailto:james.r.zimmer-dauphinee@vanderbilt.edu)  

Natalie Robbins (SARL)
[email](mailto:natalie.n.robbins@vanderbilt.edu)

Junlin Guo (CS)
[email](mailto:junlin.guo@vanderbilt.edu)

### Faculty sponsors:
Steven Wernke (Anthropology)
[email](mailto:s.wernke@vanderbilt.edu)
[website](https://stevenwernke.com/)


Yuankai Huo (Computer Science)
[email](mailto:yuankai.huo@vanderbilt.edu)


