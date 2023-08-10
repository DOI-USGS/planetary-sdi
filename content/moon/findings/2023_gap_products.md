---
title: DRAFT - 2023 Gap Products
weight: 2
---

## Summary
In September, 2021 the Final Report of the Lunar Critical DAta Products Specific Action Team found <X,Y,Z>. Since that time additional foundational data products have been created and released by the community such as the Lunar Orbiter Laser Altimeter (LOLA) Digital Elevation Models (DEMs) created by Barker, et al. at Goddard Space Flight Center and the Mini-RF polar mosaics released to the Planetary Data System (PDS), both linked below.

## Source Data
The Lunar SDI working group, with support from members of the lunar exploration community, maintains a listing of [foundational lunar data products](https://fdp.astrogeology.usgs.gov/fdp/moon/). These are products that are controlled (photogrammetrically, radargrammetrically, altimetrically) to the current lunar geodetic coordinate reference frame.

A similar collection of framework data products should be collected and maintained.

## Timliness and Importance
The scope of potential work is significant larger than the available person power and financial resources to complete that work. Therefore, we rank two axes of potential work in order to identify the most impactful data products. These axes are importance using a 5-point Likert scale: (1) Low impact, (2) Minimal impact, (3) Neutral impact, (4) Impactful, (5) High impact, and timeliness, also using a 5-point Likert scale: (1) Completed when able, (2) Needed in the next 3-5 years (3) Needed in the next 1-2 years, (4) Needed in the next 6-12 months, (5) Needed immediately.

## Assessed Missions
Current and upcoming NASA flight missions, both robotic and human can benefit immensely from the creation of new foundational data products and targeted framework data products. Therefore, the impact of those products must also be assessed by the breadth of impact to one or more missions. A third dimension of this assessment is mission impact. 

The missions assessed for impact within this document are: VIPER, Artermis III, Nova-C IM-1, Peregrine Mission 1, JAXA SLIM.

Text about the needs of these missions as it relates to these products.

| Product Identifier | Product Type | Purpose | Importance | Timeliness | Impacted Missions | Availability | In creation? | 
| ------------------ | ------------ | ------- | ---------- | ---------- | ----------------- | ------------ | ------------ | 
| Mini-RF south pole mosaics| Topography | Landing site assessment? | High impact | Available now | ?? |  https://pds-geosciences.wustl.edu/lro/lro-l-mrflro-4-cdr-v1/lromrf_0005/data/sar/mosaics/ | Delivered; Mini-RF Team |
| LROC-NAC south pole mosaics | Controlled images / Image mosaics | Landing site assessment | Impactful | ?? | Continually adding more? | | USGS? |
| LROC-NAC DEMs (Shape-from-Shading) | Topography | Landing site assessment, mission operations | Impactful | ?? | ? | | NASA Ames? |
| LROC-NAC DEMs (Stereophotogrammetry) | Topography | Landing site assessment | Impactful | ?? | ? | | LROC Team, others?[^1] |
| LOLA DEMs | Topography | Landing site assessment | Impactful | Available now | ?? | https://pgda.gsfc.nasa.gov/products/78 / https://doi.org/10.1016/j.pss.2020.105119| Delivered; GSFC |
| SELENE / Kaguya TC Mosaics[^2] | Controlled images / Image mosaics | Context |  Minimal impact | Completed when able | ?? | ?? | USGS |
| SELENE / Kaguya TC DEMs[^3] | Topography | Context / LOLA updates | Neutral Impact | Needed in the next 1-2 years | LOLA | ?? | USGS | 
| Chang'E-2 Image Mosaics | ?? | Landing site assessment | ?? | ?? | ?? |  GRAS Lunar and Planetary Data Release System | Completed (No ARD / challenging to discover?) |
| Chang'E-2 7 m/pixel DEM | Topography | ? | ? | Available Now | ?? | GRAS Lunar and Planetary Data Release System | Completed (No ARD / challenging to discover?) |

## Globally Controlled Products
Are these as important as the regional products? It does not seem that they have as much immediate impact? There also seems to be duplication here.

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

Multi-color/spectral:
- Kaguya SP mosaic (6-8 m/pixel, 296 channels)
  - JAXA has many mineral maps released. What does this mean?
- Kaguya MI mosaic (20 m/pixel, 9 channels)
  - JAXA has released, no? Uncontrolled, but exists. What gap does this fill, particularily if a SP mosaic is made?
- LROC WAC mosaic (100 m/pixel nominal; 75 m/pixel visible, 5 channels; 385 m/pixel UV, 2 channels)
  - Exists. Uncontrolled. What gap?
- Chandrayaan-1 M3 (140 m/pixel global; 70 m/pixel targeted, 260 channels)
  - What gap? Different wavelengths than SP?
Clementine (~>110 m/pixel, 12 channels)
  - Exists. Is the base. Controlled to old datum?

## Framework Products to Support Landed Missions

- Early morning illumination NAC mosaics
  - Still need to be done? Is anyone working on these? What is the fallback product that exists?
- Multi- and hyperspectral mosaics
  - Rationale?
  - Status?
- Quantitative mineral maps
  - Don't these fall out of the above?
  - Status?
- Geologic maps
  - Status?
- Terrain / Hazard
  - Ross - are you all making these for VIPER? Releasing them?
- Viewshed
  - Ross, as above.
- Time dependent illumination
  - Ross....
- 

[^1]: Need a clearinghouse for these, a common standard for metadata, and a common vocabulary for describing quantitative and qualitative metrics.
[^2]: Uncontrolled available at https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-evening-map-v4.0, https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-morning-map-v4.0, https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-ortho-map-seamless-v2.0
[^3] Need a quality assessment and processing description of https://darts.isas.jaxa.jp/pub/pds3/sln-l-tc-5-dtm-map-seamless-v2.0