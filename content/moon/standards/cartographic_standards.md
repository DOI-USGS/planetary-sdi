---
title: Lunar Cartographic Standards
weight: 51
---
**DRAFT**

### Map Projections
- Data are provided in a simple cylindrical (equirectangular) map projection.
- Data are orthorectified to a sphere using the IAU radius => 1737.4km ([Archinal, et al. 2018](https://doi.org/10.1007/s10569-017-9805-5))
- Data are made available in 0 – 360 positive East coordinate system with a center longitude of 180 degrees using planetocentric latitude. 
- For observational data, pixel scale or resolution should be maintained at native scale or better, (i.e., do not average data.) 
- For derived data (e.g., DTMs), data should be made available at a reasonable resolution that avoids interpolation of information.
- Data for polar areas (latitudes > 65˚ North or South) should use a polar stereographic projection centered at the pole.

### Vector Symbology
- The OGC maintained [Styled Layer Descriptor](https://www.ogc.org/standards/sld) standard will be used for vector symbology for all data in the GeoPackage format.

### Discussion

{{< comments >}}