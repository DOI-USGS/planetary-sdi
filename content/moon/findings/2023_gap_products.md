---
title: DRAFT - 2023 Gap Products
weight: 2
---

## Summary
In September, 2021 the Final Report of the Lunar Critical DAta Products Specific Action Team found <X,Y,Z>. Since that time additional foundational data products have been created and released by the community such as the Lunar Orbiter Laser Altimeter (LOLA) Digital Elevation Models (DEMs) created by Barker, et al. at Goddard Space Flight Center and the Mini-RF polar mosaics released to the Planetary Data System (PDS), both linked below.

## Source Data
The Lunar SDI working group, with support from members of the lunar exploration community, maintains a listing of [foundational lunar data products](https://fdp.astrogeology.usgs.gov/fdp/moon/). These are products that are controlled (photogrammetrically, radargrammetrically, altimetrically) to the current lunar geodetic coordinate reference frame.

## Timliness and Importance
The scope of potential work is significant larger than the available person power and financial resources to complete that work. Therefore, we rank two axes of potential work in order to identify the most impactful data products. These axes are importance using a 5-point Likert scale: (1) Low impact, (2) Minimal impact, (3) Neutral impact, (4) Impactful, (5) High impact, and timeliness, also using a 5-point Likert scale: (1) Completed when able, (2) Needed in the next 3-5 years (3) Needed in the next 1-2 years, (4) Needed in the next 6-12 months, (5) Needed immediately.

## Assessed Missions
Current and upcoming NASA flight missions, both robotic and human can benefit immensely from the creation of new foundational data products and targeted framework data products. Therefore, the impact of those products must also be assessed by the breadth of impact to one or more missions. A third dimension of this assessment is mission impact. 

The missions assessed for impact within this document are: VIPER, Artermis III, Nova-C IM-1, Peregrine Mission 1, JAXA SLIM.

Text about the needs of these missions as it relates to these products.

## Terminology and Definitions
This document uses the following...
### Product Type

### Availability

 ## Foundational Data Products
 [Foundational data products](https://fdp.astrogeology.usgs.gov/#foundational-data-products) are foundational to the proper spatialization of all other, framework data products. Foundational data products are the geodetic coordinate reference frame (or proxy product), topographic data (which is often the proxy for the geodetic coordinate reference frame), and orthoimages. In order to be a foundational data product, the product must report and support rigorous spatial error assessment and reporting. All other products are framework data products which support one or more science or engineering tasks. These framework data products should all be derived from the common geodetic foundation encoded in all foundational data products.

 The identified foundational data products for the moon are tracked [here](https://fdp.astrogeology.usgs.gov/fdp/moon/). Note that gravity data and uncontrolled image mosaics are **not** foundational.

The Lunar Critical Data Product Specific Action Team identified a number of gaps in the availability of lunar foundational data products to support robotic and human exploration of the Moon. The table below tracks the gaps identified in the 2021 report, highlighting where progress has been made creating the needed products. The table also includes newly identified gaps.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| LROC-NAC south pole mosaics | Controlled images / Image mosaics | Landing site assessment | Impactful | ?? | Continually adding more? | | USGS / LROC, team (look in PDS) |
| LROC-NAC DEMs (Shape-from-Shading) | Topography | Landing site assessment, mission operations | Impactful | ?? | ? | | NASA Ames (Artemis landing sites), don't know about others.|
| LROC-NAC DEMs (Stereophotogrammetry) | Topography | Landing site assessment | Impactful | ?? | ? | | LROC Team, others?[^1] |
| LOLA DEMs (They made a carpet. /81 on the URL.) | Topography | Landing site assessment | Impactful | Available now | ?? | https://pgda.gsfc.nasa.gov/products/78 / https://doi.org/10.1016/j.pss.2020.105119| Delivered; GSFC |
| SELENE / Kaguya TC Mosaics[^2] | Controlled images / Image mosaics | Context |  Minimal impact | Completed when able | ?? | ?? | USGS |
| SELENE / Kaguya TC DEMs[^3] | Topography | Context / LOLA updates | Neutral Impact | Needed in the next 1-2 years | LOLA | ?? | USGS | 
| Chang'E-2 Image Mosaics (in MoonTrek?) | ?? | Landing site assessment | ?? | ?? | ?? |  GRAS Lunar and Planetary Data Release System | Completed (No ARD / challenging to discover?) |
| Chang'E-2 7 m/pixel DEM | Topography | ? | ? | Available Now | ?? | GRAS Lunar and Planetary Data Release System | Completed (No ARD / challenging to discover?) |
| Chandryaan-2 5m / pixel DEMs | Landing site assessment | High Impact | ?? | ?? | Available via the ISRA web portal | Completed |
| Chandryaan-2 Ortho Image | Controlled images / Image mosaics | Landing site assessment | High Impact | ?? | ?? | Available via the ISRA web portal | Completed |
| Constellation data sets (e.g., LMMP DTMs)| Topography | Landing site assessment | Neutral Impact | Completed when able | ?? |  Some available, but not all? | Completed |
| GSFC Long Swath Approach Topography | Topography | Landing site assessment | High Impact | Needed in the next 1-2 Years | Commercial Lunar landings | Not available | GSFC? |

### Globally Controlled Foundational Products
The focus is and has been on the lunar south pole to support human and robotic missions. These global foundational data products are also of critical importance for commercial landing attempts and a longer time horizon for human operations outside the south pole region.

- LROC NAC mosaic
- LROC NAC SfS DEM
- Chandrayaan-2 TMC2 mosaic
- Chandrayaan-2 TMC2 DEM
- LOLA DEM (improved, e.g., co-registered with mosaic or DEM products)
  - ?? Isn't this done (above?)
- Chang’E 2 CCD Camera mosaic
  - Listed above and accessible. What else needs to be done?
- Kaguya TC mosaic
  - JAXA has a version released. Does not seem controlled. USGS is controlling now. What needs doing?
- Kaguya TC DEM
  - A global product exists from JAXA
  - USGS is making more of these now to support GSFC
  - What else needs doing?

## Framework Products to Support Landed Missions
Framework data products are all other products not identified as [foundational data products](https://fdp.astrogeology.usgs.gov/#foundational-data-products). These are raw and derived data products that support the innumerable science, engineering, and outreach tasks that the lunar exploration community engages in.

### Multi- and Hyper-spectral Image Mosaics
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| Kaguya / SELENE Spectral Profiler Mosaic | Hyper-spectral images and image mosaic | ?? | ?? | ?? | ?? | Does not exist | No |
| Kaguya / SELENE Multiband Imager Mosaic | Multi-spectral images and image mosaic | ?? | ?? | ?? | ?? | Does not exist | No |
| LROC WAC Mosaic | Multi-spectral images and image mosaic | ?? (not controlled) | - | - | ?? | LINK | Completed |
| Chandrayaan-1 M3 Mosaic | Hyper-spectral images and image mosaic | ?? | ?? | ?? | ?? | https://astrogeology.usgs.gov/maps/moon-mineralogy-mapper-geometric-data-restoration | ?? |
| Clementine Mosaic | Multi-spectral images and image mosaic | ?? (old datum?) | ?? | ?? | ?? | LINK | Completed / redo? |
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |

### Quantitative Mineral Mosaics
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |

  - Don't these fall out of the above?
  - Status?

### Regional Image Mosaics
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| High resolution Mini-RF south pole mosaics | Controlled images / Image mosaics | Landing site assessment? | High impact | Not available now | ?? |  ?? | Not yet delivered; Mini-RF Team |
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |

### Topographic Maps
Topography and topographic maps are two different types of data products. The latter are derived in part from the former and in part form other ancillary data sets. Many cartographic decisions are applied to these composite data sets, such as choice or projection, scale, symbology, and feature labeling. These decisions result in a map that impart the information that the cartographer(s) wish to convey. 

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
|[Topographic Map of the the Moon's South Pole (80˚S to Pole)](https://repository.hou.usra.edu/handle/20.500.11753/1254) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [Topographic Map of the Moon’s South Pole (85°S to Pole)](https://repository.hou.usra.edu/handle/20.500.11753/1256) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [Topographic Map of the Moon’s South Pole](https://repository.hou.usra.edu/handle/20.500.11753/1259) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [Topography and Permanently Shaded Regions (PSRs) 85°S to Pole of the Moon](https://repository.hou.usra.edu/handle/20.500.11753/1258) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [Topographic Map of the Moon’s South Polar Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1262) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [Topographic Contour Map of the Moon’s South Pole Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1326) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [MIIGAiK Hypsometric Map of the Lunar Polar Areas](https://www.lpi.usra.edu/lunar/lunar-south-pole-atlas/maps/Hypsometric_map_of_lunar_poles.pdf) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| USGS Scientific Investigations Map, South Pole Image Map](https://www.lpi.usra.edu/lunar/lunar-south-pole-atlas/images/300dpi/USGS-Moon.jpg) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| [USGS Scientific Investigations Map, South Pole Topographic Map](https://www.lpi.usra.edu/lunar/lunar-south-pole-atlas/images/300dpi/topographic-moon.jpg) | Map product | ?? | - | - | Impacted Missions | As PDF, no GIS solution | Completed. |
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |
### Geologic maps
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| [Shaded Relief Geological Map of the South Polar Region of the Moon](https://repository.hou.usra.edu/handle/20.500.11753/1720) | Map product, Scale: ??? | ?? | - | - | ?? | As PDF, no GIS solution | Completed . |
| [Geologic Map of the South Pole of the Moon, Krasilnikov et al.](https://www.hou.usra.edu/meetings/lpsc2021/pdf/1428.pdf) Scale: 1:300,000
| Larger scale map efforts? 1:200,000, 1:24000? | Map product, Scale: ??? | ?? | - | - | ?? | As PDF, no GIS solution | Completed . |
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |
### Terrain / Hazard
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| [Slope Map of the Moon’s South Pole (85°S to Pole)](https://repository.hou.usra.edu/handle/20.500.11753/1366) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Slope Map of the Moon’s South Pole (85°S to Pole) – Map 3](https://repository.hou.usra.edu/handle/20.500.11753/1382)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topographic Map and >1 km-diameter Craters in the Artemis Exploration Zone](https://www.lpi.usra.edu/lunar/lunar-south-pole-atlas/maps/ArtemisExplorationZone_Craters_1kmPlus.pdf)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topographic Slopes (5-meter) of the Moon’s South Polar Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1265)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topographic Slopes of the Moon’s South Polar Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1266)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topography and Relatively Flat Areas of the Moon’s South Polar Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1267)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Slope Map between Shackleton and de Gerlache Craters, Lunar South Pole](https://hdl.handle.net/20.500.11753/1360)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Slope Map Between Shackleton and de Gerlache Craters, Lunar South Pole – Map 3](https://hdl.handle.net/20.500.11753/1441)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Slope Map of the Moon’s South Pole Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1327)| Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| VIPER[^4] mission derived products | ?? | ?? | ?? | ?? | ?? | ?? |?? |
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |

### Viewshed
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ |
| VIPER[^4] mission derived products | ?? | ?? | ?? | ?? | ?? | ?? |?? |
| ... | ?? | ?? | ?? | ?? | ?? | ?? |?? |

### Illumination / Time Dependent Illumination
Description of the data, what are these. Why are they broadly important.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ |
| [Topography and Permanently Shaded Regions (PSRs) 87°S to Pole of the Moon](https://repository.hou.usra.edu/handle/20.500.11753/1261) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topography and Permanently Shaded Regions (PSRs) of the Moon’s South Pole (85°S to Pole)](https://repository.hou.usra.edu/handle/20.500.11753/1257) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topography and Permanently Shaded Regions (PSRs) of the Moon’s South Pole (80°S to Pole)](https://repository.hou.usra.edu/handle/20.500.11753/1255) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Lunar South Pole Radar Images and Earthshine Model (85°S to Pole)](https://hdl.handle.net/20.500.11753/1488) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topography and Permanently Shaded Regions (PSRs) of the Moon’s South Polar Nearside](https://repository.hou.usra.edu/handle/20.500.11753/1756) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topography and Permanently Shaded Regions (PSRs) of the Moon’s South Pole](https://repository.hou.usra.edu/handle/20.500.11753/1260) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Topography and Permanently Shaded Regions (PSRs) of the Moon’s South Polar Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1263) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [Annual Illumination and Topographic Slope of the Moon’s South Polar Ridge](https://repository.hou.usra.edu/handle/20.500.11753/1264) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [WAC Percentage-Based South Pole Illumination Map](https://wms.lroc.asu.edu/lroc/view_rdr/WAC_POLE_ILL_PCT_SOUTH) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| [WAC Time-Weighted South Pole Illumination Map](https://wms.lroc.asu.edu/lroc/view_rdr/WAC_POLE_ILL_TWI_SOUTH) | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| GSFC, [Mazarico, et al. 2018](https://www.sciencedirect.com/science/article/pii/S0273117718306501?via%3Dihub) and [Barker, et al., 2019](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2019JE006020) have published on their IllumNG tool. The former paper describes the tool and has some sample results, while the latter paper uses the tool. Are any of these products available anywhere? | Map product | Engineering | - | - | ?? | As PDF, no GIS solution | Completed. |
| VIPER[^4] mission derived products | ?? | ?? | ?? | ?? | ?? | ?? |?? |
| Early morning illumination NAC mosaics | ?? | ?? | ?? | ?? | ?? | ?? |?? |
### Temperature Maps
  - [Near-Surface Temperatures Modeled for the Moon’s South Pole (85°S to Pole)](https://repository.hou.usra.edu/handle/20.500.11753/1336)


[^1]: Need a clearinghouse for these, a common standard for metadata, and a common vocabulary for describing quantitative and qualitative metrics.
[^2]: Uncontrolled available at https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-evening-map-v4.0, https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-morning-map-v4.0, https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-ortho-map-seamless-v2.0
[^3]: Need a quality assessment and processing description of https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-dtm-map-seamless-v2.0
[^4]: We believe that the VIPER mission is creating these, but the potential and timeline for release is unknown.