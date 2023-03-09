---
geekdocCollapseSection: false
weight: 30
---

The standards enumerated herein are intended to facilitate data interoperability. How is the lunar SDI defining data interoperability? A user of data made available by a data provider, via a data portal that has adopted the Lunar SDI standards can reasonably assume that different data sets will:

- Be made available in the same, [GIS ready formats]({{< ref "data_formats" >}}). Data conforming to these standards are interoperable at a technical level by the tools and technologies used to analyze and view the data.
- Have been created or modified to use the same [underlying datums and map projections]({{< ref "data_standards" >}}). This ensures that the products will be co-aligned to the level of their control to a common geodetic coordinate reference frame[^1]. Data conforming to these standards are interoperable at the spatial level and can be used for spatial analyses.
- Be documented similarly, such that users are [provided with common metadata]({{< ref "metadata_standards" >}}) including information on data product accuracy, fitness-for-use, and known issues with the data. Data conforming to these standards are semantically interoperable and allow users to make informed decisions about whether data are suitable for the analyses they are performing. 
 
Lunar SDI data that are compliant with these standards are said to be interoperable. From a user's perspective, these data are suitable for data discovery, visualization, and analysis. From a data creator's perspective, making their data available in an interoperable way ensures that new products are used with the corpus of existing products, thereby increasing adoption. From a data provider's perspective, releasing interoperable data into a broader ecosystem ensures similar successes, a provider's offerings can be used immediately by users or aggregated into larger scope tools by other data providers.

For U.S. scientists, researchers, and technical staff, the standards described herein are designed to ensure compliance with the NASA published [SMD Policy Document SPD-41 a](https://science.nasa.gov/science-red/s3fs-public/atoms/files/SMD-information-policy-SPD-41a.pdf).

[^1]: See either [Laura and Beyer (2021)](https://iopscience.iop.org/article/10.3847/PSJ/abcb94) or the [Foundational Data Products webpage](https://fdp.astrogeology.usgs.gov/fdp/about/) for a description of the different levels of photogrammetric control.
