---
title: Lunar Data Format Standards
weight: 50
---
**DRAFT**

### Formats for Offline Data Access
- Data in raster format should be provided as [cloud optimized GeoTiffs](https://www.cogeo.org)(COG), complying with the [cartographic standards]({{< ref "cartographic_standards" >}}). 
  - Rationale: a COG is "just" a GeoTiFF with additional header information that supports data streaming. COGs are preferable as data volumes increase and local analyses of large data volumes become less tractable. Legacy TIFFs can be converted to COGs with little overhead beyond the (re)processing costs.
- Data in vector format should be provided in [OGC GeoPackage format](https://www.geopackage.org) with information stored in decimal degrees (i.e., no map projection applied) or in a map projected form complying with the [cartographic standards]({{< ref "cartographic_standards" >}})
  - Rationale: More widely used vector data standards such as [Shapefile](http://switchfromshapefile.org) are rapidly approaching their End-of-Life. Therefore, we suggest that data users (who often create vector data sets) consider shifting their workflows slightly. See the [data examples]({{< ref "data_examples" >}}) for suggestions creating GeoPackage files natively **or** converting shapefiles into GeoPackage files.


### Formats for Online Data Access
- Data in raster format should be provided as [cloud optimized GeoTiffs](https://www.cogeo.org), complying with the above projection standards. These data will be accessed via their [STAC](https://stacspec.org/en) data files. Alternatively, data in raster format can be provided using an OGC compliant [WMS](https://www.ogc.org/standards/wms) service. This service must encode a proper [IAU 2015/2018 projection code](https://ui.adsabs.harvard.edu/abs/2021LPICo2549.7012H) or via the aforementioned STAC/COG standard.
- Data in vector format should be served using an OCG compliant [WFS](https://www.ogc.org/standards/wfs) or [WMTS](https://www.ogc.org/standards/wmts) service using the standards defined above, or a vector tile server. Most importantly, the server must encode a proper IAU 2015 projection code.
- The [STAC](https://stacspec.org)-API specification (a remotely accessible search service) will be used to support metadata query and data discoverability. 
- Lidar (point cloud) data will be provided using the [Cloud Optimised Point Cloud (COPC)](https://copc.io) or [Entwine Point Tile (EPT)](https://entwine.io/entwine-point-tile.html) format with proper WKT or `proj:json` projection information.

### Discussion

{{< comments >}}