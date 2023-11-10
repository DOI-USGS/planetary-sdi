---
title: Lunar Data Format Standards
weight: 50
---
**DRAFT**

### Formats for Offline Data Access
- Data in raster format will be provided as [cloud optimized GeoTiffs](https://www.cogeo.org)(COG), complying with the [cartographic standards]({{< ref "cartographic_standards" >}}). 
- Data in vector format will be provided in [OGC GeoPackage format](https://www.geopackage.org) with information stored in decimal degrees (i.e., no map projection applied) or in a map projected form complying with the [cartographic standards]({{< ref "cartographic_standards" >}})


### Formats for Online Data Access
- Data in raster format can be provided as [cloud optimized GeoTiffs](https://www.cogeo.org), complying with the above projection standards. These data will be accessed via their [STAC](https://stacspec.org/en) data files.
- Data in raster format can be provided using an OGC compliant [WMS](https://www.ogc.org/standards/wms) service. This service must encode a proper [IAU 2015/2018 projection code](https://ui.adsabs.harvard.edu/abs/2021LPICo2549.7012H) or via the aforementioned STAC/COG standard.
- Data in vector format can be served using an OCG compliant [WFS](https://www.ogc.org/standards/wfs) or [WMTS](https://www.ogc.org/standards/wmts) service using the standards defined above. The server must encode a proper IAU 2015/2018 projection code.
- The [STAC](https://stacspec.org)-API specification (a remotely accessible search service) will be used to support metadata query and data discoverability. 
- Lidar (point cloud) data will be provided using the [Cloud Optimised Point Cloud (COPC)](https://copc.io) or [Entwine Point Tile (EPT)](https://entwine.io/entwine-point-tile.html) format with proper WKT or `proj:json` projection information.

### Discussion

{{< comments >}}