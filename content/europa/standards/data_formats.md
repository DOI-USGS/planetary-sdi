---
title: Data Format Standards
weight: 60
---

### Formats for Offline Data Access
- Data in raster format will be provided as [cloud optimized GeoTiffs](https://www.cogeo.org)(COG), complying with the above projection standards. 
- Data in vector format will be provided in [OGC GeoPackage format](https://www.geopackage.org) with information stored in decimal degrees (i.e., no map projection applied)


### Formats for Online Data Access
- Data in raster format can be provided as [cloud optimized GeoTiffs](https://www.cogeo.org), complying with the above projection standards. These data will be accessed via their [STAC](https://www.google.com/search?client=safari&rls=en&q=spatio-temporal+asset+catalog&ie=UTF-8&oe=UTF-8) data files.
- Data in raster format can be provided using OGC compliant WMS service. Said service must encode a proper IAU 2015 projection code.
- Data in vector format can be served using an OCG compliant WFS or WMTS service using the standards defined above. The server must encode a proper IAU 2015 projection code.
- The STAC-API specification (a remotely accessible search service) will be used to support metadata query and data discoverability. 
