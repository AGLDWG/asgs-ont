# ASGS Ontology - ABS Structures and non-ABS structures
Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE)


## Metadata
* **IRI**
  * `http://linked.data.gov.au/def/asgs`
* **Publisher(s)**
  * Australian Bureau of Statistics
* **Creators(s)**
  * <a href="https://orcid.org/0000-0002-4305-6085">Laurent Lefort</a> (<a href="mailto:laurent.lefort@abs.gov.au">laurent.lefort@abs.gov.au</a>) of <a href="https://www.abs.gov.au">Australian Bureau of Statistics</a>
  * <a href="https://orcid.org/0000-0002-3884-3420">Simon J.D. Cox</a> (<a href="mailto:simon.cox@csiro.au">simon.cox@csiro.au</a>) of <a href="https://www.csiro.au">CSIRO</a>
* **Contributor(s)**
  * <a href="https://orcid.org/0000-0002-8742-7730">Nicholas J. Car</a> (<a href="mailto:nicholas.car@surroundaustralia.com">nicholas.car@surroundaustralia.com</a>) of <a href="https://surroundaustralia.com">SURROUND Australia Pty Ltd</a>
* **Created**
  * 2018-11-23
* **Modified**
  * 2020-04-29
* **Imports**
  * <a href="http://www.opengis.net/ont/geosparql">http://www.opengis.net/ont/geosparql</a>
* **Rights**
  * &copy; 2018 Australian Bureau of Statistics.
* **Source**
  * <a href="https://www.abs.gov.au/websitedbs/D3310114.nsf/home/Australian+Statistical+Geography+Standard+(ASGS)">https://www.abs.gov.au/websitedbs/D3310114.nsf/home/Australian+Statistical+Geography+Standard+(ASGS)</a>
* **Ontology RDF**
  * <a href="asgs.ttl">RDF (turtle)</a>
* **Code Repository**
  * <https://github.com/AGLDWG/asgs-ont/>
### Description
<p>Ontology for the Australian Statistical Geography Standard (ASGS), a framework of statistical areas used by the Australian Bureau of Statistics (ABS) and other organisations to enable the publication of statistics that are comparable and spatially integrated. This ontology contains the definitions for the ABS Structures which are areas that the ABS designs specifically for outputting statistics.</p>
<p>ABS structures: </p>
<ul>
<li>Mesh Block, Statistical Areas (Level 1 to Level 4), Greater Capital City Statistical Areas, State or Territory, Country classes</li>
<li>Indigenous location, Indigenous area, Indigenous region </li>
<li>Urban Centre and Locality, Section of State Range, Section of State, Significant Urban Area</li>
</ul>
<p>Non ABS Structures which are not defined or maintained by the ABS but represent administrative areas for which the ABS is committed to providing a range of statistics. 
The classes defined here corresponds to ABS approximations of spatial areas or regions which are defined elsewhere</p>
<ul>
<li>Local Government Areas (LGAs)</li>
<li>Postal Areas (POAs)</li>
<li>State Suburbs (SSCs)</li>
<li>Commonwealth Electoral Divisions (CEDs)</li>
<li>State Electoral Divisions (SEDs)</li>
<li>Australian Drainage Divisions (ADDs)</li>
<li>Natural Resource Management Regions (NRMRs)</li>
<li>Tourism Regions (TRs)</li>
</ul>
<p>The ASGS uses Mesh Blocks as a common building block for all structures. Mesh Blocks are small enough that they can accurately approximate the changing administrative areas maintained by other organisations, without changing themselves.</p>
<p>The publication of the ASGS ontology is part of the Australian Bureau of Statistics contribution to a joint effort to publish authoritative, interconnected spatial products (Location Index project).</p>
<p>The ASGS Ontology is packaged in multiple graphs:</p>
<ul>
<li>http://linked.data.gov.au/def/asgs (this graph) contains the core classes for ASGS statistical units, and a small number of properties relating to their identity, classification, and containment hierarchy</li>
<li>http://linked.data.gov.au/def/asgs-cat contains the meshblock classification scheme</li>
<li>http://linked.data.gov.au/def/asgs-id contains specialised string types for identifiers and labels</li>
<li>http://linked.data.gov.au/def/asgs-path contains association classes and properties relating to paths between instances of the core classes</li>
<li>http://linked.data.gov.au/def/asgs-isof (deprecated) contains specialized predicates for containment relationships - this functionality is provided by generic 'within' and 'isComposedOf' relations instead</li>
<li>http://linked.data.gov.au/def/asgs-code (deprecated) contains specialised annotation properties for identifiers and labels - this functionality has been superseded by a set of data-types to be used in conjunction with more generic properties</li>
<li>http://linked.data.gov.au/def/asgs-prop (deprecated) contains specialised ASGS properties for relationships, classifiers, identifiers and labels - this functionality has been superseded by use of types from standardized RDF vocabularies</li>
</ul>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Annotation Properties](#annotationproperties)
1. [Namespaces](#namespaces)  


## Overview

**Figure 1:** Ontology overview  
## Classes
[ASGS Feature](#ASGSFeature),
[Australian Drainage Division](#AustralianDrainageDivision),
[Commonwealth Electoral Division](#CommonwealthElectoralDivision),
[Country ](#Country),
[Destination Zone](#DestinationZone),
[Greater Capital City Statistical Area](#GreaterCapitalCityStatisticalArea),
[Indigenous Area](#IndigenousArea),
[Indigenous Location](#IndigenousLocation),
[Indigenous Region](#IndigenousRegion),
[Local Government Area](#LocalGovernmentArea),
[Mesh Block](#MeshBlock),
[Meshblock category](#Meshblockcategory),
[Natural Resource Management Region](#NaturalResourceManagementRegion),
[Organization](#Organization),
[Person](#Person),
[Postal area](#Postalarea),
[Remoteness Area](#RemotenessArea),
[Section of State](#SectionofState),
[Section of State Range](#SectionofStateRange),
[Significant Urban Area](#SignificantUrbanArea),
[State Electoral Division](#StateElectoralDivision),
[State Suburb](#StateSuburb),
[State or Territory](#StateorTerritory),
[Statistical Area Level 1](#StatisticalAreaLevel1),
[Statistical Area Level 2](#StatisticalAreaLevel2),
[Statistical Area Level 3](#StatisticalAreaLevel3),
[Statistical Area Level 4](#StatisticalAreaLevel4),
[Tourism Region](#TourismRegion),
[Urban Centre and Locality](#UrbanCentreandLocality),
### Australian Drainage Division <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#AustralianDrainageDivision`
Description | Australian Drainage Divisions (ADD) are an ABS approximation of Bureau of Meteorology Drainage Divisions. Drainage Divisions are defined by major landscape features and climatic zones to form broad hydrological regions as represented in the Australian Hydrological Geospatial Fabric (Geofabric) 2014 version 2 developed by the Bureau of Meteorology. ADDs are approximated using one or more Mesh Blocks (MBs). ADDs can cross State and Territory (S/T) boundaries. ADDs cover the whole of geographic Australia without gaps or overlaps. The ADDs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br />
### Commonwealth Electoral Division <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#CommonwealthElectoralDivision`
Description | Commonwealth Electoral Divisions (CED) are an ABS approximation of Australian Electoral Commission (AEC) electoral division boundaries. An Australian Electoral Commission electoral division boundary is an area legally prescribed for the purpose of returning one member to the House of Representatives Australia's Federal Lower House of Parliament. Commonwealth Electoral Divisions may change as the Australian Electoral Commission revise their boundaries. Where the Australian Electoral Commission revise their boundaries the CEDs will be updated on an annual basis in July in conjunction with updates of other Non ABS Structures. CEDs are approximated using whole Statistical Areas Level 1 (SA1s). CEDs cover the whole of Australia without gaps or overlaps.The CEDs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br />
### Country  <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#Country`
Description | Australia (AUS) represents the geographic extent of Australia. This is set out in section 2B of the Acts Interpretation Act 1901 which currently defines Australia or the Commonwealth as meaning: 'the Commonwealth of Australia and when used in a geographical sense includes Norfolk Island the Territory of Christmas Island and the Territory of Cocos (Keeling) Islands but does not include any other external Territory'.Prior to 2016 Norfolk Island was not included in the ASGS. However in line with Australian Government announced reforms to the governance of Norfolk Island and its inclusion into the definition of Geographic Australia the Territory of Norfolk Island was included in the 2016 ASGS. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br />
### Destination Zone <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#DestinationZone`
Description | Destination Zones (DZN) are geographic areas primarily used for the analysis of Census Place of Work data. They are designed to represent the distribution of workplaces rather than residential dwellings. This means there is greater spatial detail in areas with high concentrations of workplaces. DZNs are jointly developed between the ABS and each State or Territory Transport Authority. DZNs are built from whole Mesh Blocks (MB) and aggregate to Statistical Areas Level 2 (SA2s). DZNs cover the whole of Australia without gaps or overlaps. The DZN regions are not an Australian Statistical Geography Standard (ASGS) structure however the ABS publishes Census data on these areas. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StatisticalAreaLevel2">asgs:StatisticalAreaLevel2</a><sup class="sup-c" title="class">c</sup><br />
### ASGS Feature <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#Feature`
Description | Super-class for all ABS Structures and Non-ABS Structures. Use

- dcterms:identifier for the code, with a suitable datatype from `asgs-id`
- rdfs:label for the name, with a suitable datatype from `asgs-id`
- `asgs:within`, `asgs:isComposedOf` for containment and composition relations
Super-classes |<a href="http://www.opengis.net/ont/geosparql#Feature">geo:Feature</a><sup class="sup-c" title="class">c</sup><br />
Sub-classes |<a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br /><a href="#StatisticalAreaLevel4">asgs:StatisticalAreaLevel4</a><sup class="sup-c" title="class">c</sup><br /><a href="#GreaterCapitalCityStatisticalArea">asgs:GreaterCapitalCityStatisticalArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#IndigenousRegion">asgs:IndigenousRegion</a><sup class="sup-c" title="class">c</sup><br /><a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#IndigenousArea">asgs:IndigenousArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#Country">asgs:Country</a><sup class="sup-c" title="class">c</sup><br /><a href="#NaturalResourceManagementRegion">asgs:NaturalResourceManagementRegion</a><sup class="sup-c" title="class">c</sup><br /><a href="#IndigenousLocation">asgs:IndigenousLocation</a><sup class="sup-c" title="class">c</sup><br /><a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br /><a href="#Postalarea">asgs:PostalArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#AustralianDrainageDivision">asgs:AustralianDrainageDivision</a><sup class="sup-c" title="class">c</sup><br /><a href="#StatisticalAreaLevel3">asgs:StatisticalAreaLevel3</a><sup class="sup-c" title="class">c</sup><br /><a href="#CommonwealthElectoralDivision">asgs:CommonwealthElectoralDivision</a><sup class="sup-c" title="class">c</sup><br /><a href="#SectionofStateRange">asgs:SectionOfStateRange</a><sup class="sup-c" title="class">c</sup><br /><a href="#StatisticalAreaLevel2">asgs:StatisticalAreaLevel2</a><sup class="sup-c" title="class">c</sup><br /><a href="#LocalGovernmentArea">asgs:LocalGovernmentArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#UrbanCentreandLocality">asgs:UrbanCentreAndLocality</a><sup class="sup-c" title="class">c</sup><br /><a href="#SignificantUrbanArea">asgs:SignificantUrbanArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#TourismRegion">asgs:TourismRegion</a><sup class="sup-c" title="class">c</sup><br /><a href="#SectionofState">asgs:SectionOfState</a><sup class="sup-c" title="class">c</sup><br /><a href="#RemotenessArea">asgs:RemotenessArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#DestinationZone">asgs:DestinationZone</a><sup class="sup-c" title="class">c</sup><br /><a href="#StateElectoralDivision">asgs:StateElectoralDivision</a><sup class="sup-c" title="class">c</sup><br /><a href="#StateSuburb">asgs:StateSuburb</a><sup class="sup-c" title="class">c</sup><br />
### Greater Capital City Statistical Area <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#GreaterCapitalCityStatisticalArea`
Description | Greater Capital City Statistical Areas (GCCSAs) are designed to represent the functional extent of each of the eight State and Territory capital cities. They include the people who regularly socialise shop or work within the city but live in the small towns and rural areas surrounding the city. GCCSAs are defined using the capital city labour markets. The labour market is sometimes used as a de-facto measure of the functional extent of a city as it contains the majority of the commuting population. It is important to note that GCCSAs do not define the built up edge of the city this is better represented by Urban Centres and Localities (UCLs) or Significant Urban Areas (SUAs). The GCCSA is designed to provide a stable definition of the capital cities to enable production of economic indicators which integrate variables collected over long periods of time. GCCSAs are aggregations of whole Statistical Areas Level 4 (SA4s) in the ASGS Main Structure. Whole GCCSAs aggregate to State and Territory (S/T). GSSCAs are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br /><a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel4">asgs:StatisticalAreaLevel4</a><sup class="sup-c" title="class">c</sup><br />
### Indigenous Area <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#IndigenousArea`
Description | Indigenous Areas (IAREs) are medium sized geographical areas designed to facilitate the release of statistics with multiple variables for Aboriginal and Torres Strait Islander Peoples. IAREs provide a balance between spatial resolution and population size which provides the ability to release more detailed socio-economic attribute data than is available on Indigenous Locations (ILOCs). IAREs are aggregates of Indigenous Locations (ILOCs) and aggregate up to Indigenous Regions (IREGs). They cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#IndigenousRegion">asgs:IndigenousRegion</a><sup class="sup-c" title="class">c</sup><br /><a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#IndigenousLocation">asgs:IndigenousLocation</a><sup class="sup-c" title="class">c</sup><br />
### Indigenous Location <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#IndigenousLocation`
Description | Indigenous Locations (ILOCs) represent small Aboriginal and Torres Strait Islander communities (urban and rural) with a minimum population of 90 Aboriginal and Torres Strait Islander usual residents. An ILOC is an area designed to allow the release of statistics relating to Aboriginal and Torres Strait Islander people with a high level of spatial detail whilst maintaining the confidentiality of individuals. ILOCs are aggregates of Statistical Areas Level 1 (SA1s). ILOCs aggregate to Indigenous Areas (IAREs) and cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#IndigenousArea">asgs:IndigenousArea</a><sup class="sup-c" title="class">c</sup><br />
### Indigenous Region <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#IndigenousRegion`
Description | Indigenous Regions (IREGs) are large geographical areas loosely based on the former Aboriginal and Torres Strait Islander Commission boundaries. They are designed for the release of detailed statistical data with multiple variables on Aboriginal and Torres Strait Islander Peoples. The greater population of IREGs enables greater cross classification of variables when compared with Indigenous Areas (IAREs) or Indigenous Localities (ILOCs). IREGs are aggregates of IAREs and aggregate up to State and Territory (S/T). They cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br /><a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#IndigenousArea">asgs:IndigenousArea</a><sup class="sup-c" title="class">c</sup><br />
### Local Government Area <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#LocalGovernmentArea`
Description | Local Government Areas (LGAs) are an ABS approximation of gazetted local government boundaries as defined by each State and Territory Local Government Department. LGAs cover incorporated areas of Australia. Incorporated areas are legally designated parts of a State or Territory over which incorporated local governing bodies have responsibility. The major areas of Australia not administered by incorporated bodies are the northern parts of South Australia and all of the Australian Capital Territory and the Other Territories. These regions are identified as 'Unincorporated' in the Australian Statistical Geography Standard (ASGS) LGA structure. A small number of LGA boundaries and names change each year and the ABS LGAs are updated on an annual basis to reflect these changes. LGAs are approximated using whole Mesh Blocks (MBs). In aggregation LGAs cover Australia without gaps or overlaps. The LGAs are Non ABS Structures within the ASGS. These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br /><a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br />
### Mesh Block <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#MeshBlock`
Description | Mesh Blocks (MB) are the smallest geographical area defined by the ABS. They are designed as geographic building blocks rather than as areas for the release of statistics themselves. All statistical areas in the Australian Statistical Geography Standard (ASGS) both ABS and Non ABS Structures are built up from one or more MBs.As a result the design of MBs takes into account many factors including administrative boundaries such as Cadastre (property boundaries) Suburbs and Localities and Local Government Areas (LGAs) as well as land uses and dwelling distribution. Most MBs contain 30 to 60 dwellings although some are specifically designed to have zero. This provides an additional level of confidentiality for data released on the ASGS as the difference in data released on multiple statistical areas is always at least one MB. Mesh Blocks like other ABS structures in the ASGS are stable for 5 years and are updated to reflect changes such as new housing developments every 5 years. The MB table includes a Mesh Block Category field that broadly defines primary land uses such as Residential and Commercial. MB boundaries are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="http://purl.org/dc/terms/type">dcterms:type</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#Meshblockcategory">asgs:MeshblockCategory</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br />
### Meshblock category <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#MeshblockCategory`
Description | The class of meshblock categories, as defined in ASGS
Super-classes |<a href="http://www.w3.org/2004/02/skos/core#Concept">skos:Concept</a><sup class="sup-c" title="class">c</sup><br />
### Natural Resource Management Region <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#NaturalResourceManagementRegion`
Description | Natural Resource Management Regions (NRMR) are an ABS approximation of Natural Resource Management regions (NRMs) which are defined through the Australian Government National Landcare Program. They are administrative regions primarily used by the Department of the Environment and Energy and the Department of Agriculture and Water Resources who share responsibility for delivery of the Australian Government's environment and sustainable agriculture programs which are broadly referred to as Natural Resource Management (NRM). NRMRs change occasionally as States and Territories revise their boundaries. NRMRs are approximated using one or more Mesh Blocks (MBs). NRMRs do not cross State and Territory (S/T) boundaries except for Jervis Bay which is included in a NSW region. NRMRs cover the whole of geographic Australia without gaps or overlaps. The NRMRs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br />
### Postal area <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#PostalArea`
Description | Postal Areas (POAs) are an ABS approximation of postcodes created to enable the release of ABS data on areas that as closely as possible approximate postcodes. This enables the comparison of ABS data with other data that has been collected using postcodes as the geographic reference. POAs exclude non-mappable Australia Post postcodes such as: post office box postcodes some delivery route postcodes which are also covered by other postcodes (a situation which often occurs in rural areas).POAs are approximated using one or more Mesh Blocks (MBs). POAs cover the whole of geographic Australia without gaps or overlaps. The POAs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br />
### Remoteness Area <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#RemotenessArea`
Description | Remoteness Areas (RAs) divide Australia into five classes of remoteness on the basis of relative access to services. RAs are based on the Accessibility and Remoteness Index of Australia (ARIA+) produced by the Hugo Centre for Migration and Population Research at the University of Adelaide. RAs are aggregates of Statistical Areas Level 1 (SA1s) that are grouped together based on their average ARIA+ score. Ras aggregate up to State and Territory (S/T) and cover Australia without gaps or overlaps.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br />
### Section of State <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#SectionOfState`
Description | Section of State (SOS) provides a set of geographic areas classifying Urban Centres and Localities (UCLs) into four different classes within each State and Territory (S/T). These four classes are an aggregation of the more detailed Section of State Range (SOSR) classification. SOS groups Urban Centres into 2 classes one of 100 000 people or more and the other less than 100 000 people. The remaining two classes are Localities and Rural Balance. This broad summary of UCLs enables detailed statistical comparisons of differently sized Urban Centres Localities and the Rural areas. SOS are aggregates of SOSR and aggregate up to State and Territory (S/T). SOS regions cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#SectionofStateRange">asgs:SectionOfStateRange</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br />
### Section of State Range <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#SectionOfStateRange`
Description | Section of State Range (SOSR) provides a set of geographic areas classifying Urban Centres and Localities (UCLs) into 11 different classes within each State and Territory (S/T). The 11 classes are made up of; 8 different population size classes grouping Urban Centres; 2 population size classes grouping Localities; and a Rural Balance. This detailed summary of UCLs enables statistical comparisons of differently sized Urban Centres Localities and the Rural areas. SOSR are aggregates of UCLs and aggregate up to Section of State (SOS). SOSR regions cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#UrbanCentreandLocality">asgs:UrbanCentreAndLocality</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#SectionofState">asgs:SectionOfState</a><sup class="sup-c" title="class">c</sup><br />
### Significant Urban Area <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#SignificantUrbanArea`
Description | Significant Urban Areas (SUAs) represent towns or cities with 10 000 people or more. They are based on Urban Centres and Localities (UCLs) but are defined by the larger Statistical Areas Level 2 (SA2s). A single SUA can represent either a single Urban Centre or a cluster of related Urban Centres. Using SA2s to define SUAs ensures a wider range of more regularly updated data is available for these areas (such as Estimated Resident Population and Building Approvals) compared to UCLs where only Census data is available. The SUA structure does not aggregate to State or Territory (S/T) level as SUAs may cross S/T boundaries. In aggregate SUAs cover Australia without gaps or overlaps as they include a remainder area 'Not in any Significant Urban Area'. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel2">asgs:StatisticalAreaLevel2</a><sup class="sup-c" title="class">c</sup><br />
### State Electoral Division <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StateElectoralDivision`
Description | State Electoral Divisions (SED) are an ABS approximation of State Electoral Districts. A State Electoral District is an area legally prescribed for the purpose of returning one or more members to the State or Territory Lower Houses of Parliament or the relevant equivalent. State Electoral Divisions may change as State or Territory authorities revise their boundaries. Where the Australian Electoral Commission revise their boundaries the SEDs will be updated on an annual basis in July in conjunction with updates of other Non ABS Structures.SEDs are approximated using whole Statistical Areas Level 1 (SA1s). SEDs do not cross State and Territory (S/T) boundaries and they cover the whole of Australia without gaps or overlaps. The Other Territories (OT) of Jervis Bay Norfolk Island Christmas Island and the Cocos (Keeling) Islands are allocated to 'Unclassified (OT)'. The SEDs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br />
### State or Territory <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StateOrTerritory`
Description | State and Territory (S/T) are separate spatial units representing the States and Territories within Australia. Jervis Bay Territory the Territories of Christmas Island; Cocos (Keeling) Islands and Norfolk Island are included as one spatial unit at the State and Territory level under the category of Other Territories. S/T are aggregations of one or more Statistical Area Level 4 (SA4s) in the ASGS Main Structure. S/T boundaries are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel4">asgs:StatisticalAreaLevel4</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#Country">asgs:Country</a><sup class="sup-c" title="class">c</sup><br />
### State Suburb <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StateSuburb`
Description | State Suburbs (SSC) are an ABS approximation of localities gazetted by the Geographical Place Name authority in each State and Territory (S/T). Gazetted Localities are the officially recognised boundaries of suburbs (in cities and larger towns) and localities (outside cities and larger towns). Gazetted Localities cover most of Australia. Presently there remain areas of rural South Australia and rural Australian Capital Territory for which Gazetted Localities remain undefined. Various islands offshore from New South Wales Victoria and Tasmania and some inshore water areas and islands are also undefined. Since 1996 Locality boundaries have been formalised for most areas of Australia through a program coordinated by the Permanent Committee on Place Names (PCPN) under the umbrella of the Intergovernmental Committee On Surveying and Mapping (ISCM). Areas where localities are not gazetted are represented by Remainder SSCs.SSCs are approximated using one or more Mesh Blocks (MBs). SSCs cover the whole of geographic Australia without gaps or overlaps including the Remainder SSCs.The SSCs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br /><a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br />
### Statistical Area Level 1 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StatisticalAreaLevel1`
Description | Statistical Areas Level 1 (SA1s) are designed to maximise the spatial detail available for Census data. Most SA1s have a population of between 200 to 800 persons with an average population of approximately 400 persons. This is to optimise the balance between spatial detail and the ability to cross classify Census variables without the resulting counts becoming too small for use. SA1s aim to separate out areas with different geographic characteristics within Suburb and Locality boundaries. In rural areas they often combine related Locality boundaries. SA1s are aggregations of Mesh Blocks (MBs). Whole SA1s aggregate to form Statistical Areas Level 2 (SA2s) Indigenous Locations (ILOCs) Urban Centres and Localities (UCLs) Remoteness Areas (RAs) Commonwealth Electoral Divisions (CEDs) and State Electoral Divisions (SEDs). SA1s are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#MeshBlock">asgs:MeshBlock</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#UrbanCentreandLocality">asgs:UrbanCentreAndLocality</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#CommonwealthElectoralDivision">asgs:CommonwealthElectoralDivision</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#StateElectoralDivision">asgs:StateElectoralDivision</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#RemotenessArea">asgs:RemotenessArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#IndigenousLocation">asgs:IndigenousLocation</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StatisticalAreaLevel2">asgs:StatisticalAreaLevel2</a><sup class="sup-c" title="class">c</sup><br />
### Statistical Area Level 2 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StatisticalAreaLevel2`
Description | Statistical Areas Level 2 (SA2s) are functional areas that represent a community that interacts together socially and economically. They often align with Suburb and Locality boundaries to improve the geographic coding of data to these areas. In major urban areas SA2s often reflect one or more related suburbs. The SA2 is the smallest area for the release of many ABS statistics including the Estimated Resident Population (ERP) Health & Vitals and Building Approvals data. SA2s generally have a population range of 3 000 to 25 000 persons and have an average population of about 10 000 persons. SA2s are aggregated from whole Statistical Areas Level 1 (SA1s) in the ASGS Main Structure. Whole SA2s aggregate to form Statistical Areas Level 3 (SA3s) Significant Urban Areas (SUAs) and Tourism Regions (TRs). SA2s are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StatisticalAreaLevel3">asgs:StatisticalAreaLevel3</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#TourismRegion">asgs:TourismRegion</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#SignificantUrbanArea">asgs:SignificantUrbanArea</a><sup class="sup-c" title="class">c</sup><br />
### Statistical Area Level 3 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StatisticalAreaLevel3`
Description | Statistical Areas Level 3 (SA3s) are designed for the output of regional data. SA3s create a standard framework for the analysis of ABS data at the regional level. SA3s do this by clustering groups of Statistical Areas Level 2 (SA2s) that have similar regional characteristics administrative boundaries or labour markets. SA3s generally have populations between 30 000 and 130 000 persons. They are often the functional areas of regional towns and cities with a population in excess of 20 000 people. Within urban areas they represent clusters of related suburbs around urban commercial and transport hubs. SA3s are aggregations of whole SA2s in the ASGS Main Structure. Whole SA3s aggregate to form Statistical Areas Level 4 (SA4s). SA3s are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel2">asgs:StatisticalAreaLevel2</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StatisticalAreaLevel4">asgs:StatisticalAreaLevel4</a><sup class="sup-c" title="class">c</sup><br />
### Statistical Area Level 4 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#StatisticalAreaLevel4`
Description | Statistical Areas Level 4 (SA4s) are specifically designed for the output of Labour Force Survey data. SA4s reflect labour markets within each State and Territory within the population limits imposed by the Labour Force Survey sample. Most SA4s have a population above 100 000 persons to provide sufficient sample size for Labour Force estimates. In regional areas SA4s tend to have lower populations (100 000 to 300 000). In metropolitan areas the SA4s tend to have larger populations (300 000 to 500 000). SA4s are aggregations of whole Statistical Areas Level 3 (SA3s) in the ASGS Main Structure. Whole SA4s aggregate to form Greater Capital City Statistical Areas (GCCSAs) and State and Territory (S/T).SA4s are contiguous and in aggregate cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#StateorTerritory">asgs:StateOrTerritory</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">max</span> 1 <a href="#GreaterCapitalCityStatisticalArea">asgs:GreaterCapitalCityStatisticalArea</a><sup class="sup-c" title="class">c</sup><br /><a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel3">asgs:StatisticalAreaLevel3</a><sup class="sup-c" title="class">c</sup><br />
### Tourism Region <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#TourismRegion`
Description | Tourism Regions (TR) are an ABS approximation of Tourism Regions provided by Tourism Research Australia (TRA). They are administrative regions primarily used by Tourism Research Australia for research and policy purposes.TRs are approximated using whole Statistical Areas Level 2 (SA2s). As of 2016 TRs do not cross State and Territory (S/T) boundaries and there are no TRs for the Other Territories (OT). The TRs are Non ABS Structures within the Australian Statistical Geography Standard (ASGS). These are mostly administrative areas which are not defined or maintained by the ABS but for which the ABS is committed to providing a range of statistics. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel2">asgs:StatisticalAreaLevel2</a><sup class="sup-c" title="class">c</sup><br />
### Urban Centre and Locality <sup>c</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#UrbanCentreAndLocality`
Description | Urban Centres and Localities (UCLs) represent areas of concentrated urban development with populations of 200 people or more. These areas of urban development are primarily identified using objective dwelling and population density criteria. This criteria is developed using data from the Census of Population and Housing. Urban Centres are defined separately to Localities. Urban Centres have urban populations of 1 000 people or more while Localities have populations of between 200 and 999 people.The UCLs are designed for the analysis of statistical data in particular data from the Census of Population and Housing. The 200 minimum population size is set to enable users to access cross classified Census data for these areas without the resulting counts becoming too small for use. UCLs are aggregates of Statistical Areas Level 1 (SA1s) they aggregate up to Section of State (SOS). UCLs include a category of Rural Balance which ensures that they cover the whole of Australia without gaps or overlaps. An additional code (Outside Australia) has also been added to represent areas not covered by Geographical Australia.
Super-classes |<a href="#ASGSFeature">asgs:Feature</a><sup class="sup-c" title="class">c</sup><br />
Restrictions |<a href="#iscomposedof">asgs:isComposedOf</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">min</span> 1 <a href="#StatisticalAreaLevel1">asgs:StatisticalAreaLevel1</a><sup class="sup-c" title="class">c</sup><br /><a href="#iswithin">asgs:within</a><sup class="sup-op" title="object property">op</sup> <span class="cardinality">exactly</span> 1 <a href="#SectionofStateRange">asgs:SectionOfStateRange</a><sup class="sup-c" title="class">c</sup><br />
### Organization <sup>c</sup>
Property | Value
--- | ---
IRI | `https://schema.org/Organization`
### Person <sup>c</sup>
Property | Value
--- | ---
IRI | `https://schema.org/Person`

## Object Properties
[is composed of](iscomposedof),
[is within](iswithin),
[type](type),
[](iscomposedof)
### is composed of <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#isComposedOf`
Description | The context resource is composed one or more of the target resources. 
[](iswithin)
### is within <sup>op</sup>
Property | Value
--- | ---
IRI | `http://linked.data.gov.au/def/asgs#within`
Description | The context resource is contained within the target resource, in a logical, ownership, governance, jurisidictional or 'is-part-of' sense. 

This may or may not correspond with a strict geometric relationship (which should be expressed using GeoSPARQL predicates).
[](type)
### type <sup>op</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/type`

## Datatype Properties
[identifier](identifier),
[](identifier)
### identifier <sup>dp</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/identifier`

## Annotation Properties
[created](created),
[creator](creator),
[date](date),
[description](description),
[modified](modified),
[publisher](publisher),
[rights](rights),
[source](source),
[title](title),
[isDefinedBy](isDefinedBy),
[qualifiedCardinality](qualifiedCardinality),
[affiliation](affiliation),
[codeRepository](codeRepository),
[email](email),
[identifier](identifier1),
[name](name),
[url](url),
[](created)
### created <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/created`
[](creator)
### creator <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/creator`
[](date)
### date <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/date`
[](description)
### description <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/description`
[](modified)
### modified <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/modified`
[](publisher)
### publisher <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/publisher`
[](rights)
### rights <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/rights`
[](source)
### source <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/source`
[](title)
### title <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://purl.org/dc/terms/title`
[](isDefinedBy)
### isDefinedBy <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://www.w3.org/2000/01/rdf-schema#isDefinedBy`
[](qualifiedCardinality)
### qualifiedCardinality <sup>ap</sup>
Property | Value
--- | ---
IRI | `http://www.w3.org/2002/07/owl#qualifiedCardinality`
[](affiliation)
### affiliation <sup>ap</sup>
Property | Value
--- | ---
IRI | `https://schema.org/affiliation`
[](codeRepository)
### codeRepository <sup>ap</sup>
Property | Value
--- | ---
IRI | `https://schema.org/codeRepository`
[](email)
### email <sup>ap</sup>
Property | Value
--- | ---
IRI | `https://schema.org/email`
[](identifier1)
### identifier <sup>ap</sup>
Property | Value
--- | ---
IRI | `https://schema.org/identifier`
[](name)
### name <sup>ap</sup>
Property | Value
--- | ---
IRI | `https://schema.org/name`
[](url)
### url <sup>ap</sup>
Property | Value
--- | ---
IRI | `https://schema.org/url`

## Namespaces
* **default (:)**
  * `http://linked.data.gov.au/def/asgs#`
* **asgs**
  * `http://linked.data.gov.au/def/asgs#`
* **cc**
  * `http://creativecommons.org/ns#`
* **dc**
  * `http://purl.org/dc/elements/1.1/`
* **dcterms**
  * `http://purl.org/dc/terms/`
* **doap**
  * `http://usefulinc.com/ns/doap#`
* **geo**
  * `http://www.opengis.net/ont/geosparql#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **schema**
  * `http://schema.org/`
* **sdo**
  * `https://schema.org/`
* **sf**
  * `http://www.opengis.net/ont/sf#`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **void**
  * `http://rdfs.org/ns/void#`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties :op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni