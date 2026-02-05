# Module 2 - Open Data

This module focuses on the practice and application of open science for data. It provides a 'how to' process for finding and assessing open data for use, for making open data and for sharing open data. The step-by-step flows are easy to follow and can be used as checklists after you complete the module. Some of the key topics discussed include: data management plans, the process for assessing data for reuse, creating a plan for making data including choosing open formats and adding documentation, and the considerations for sharing data and making your data citable.

## Learning Objectives

After completing this module, you should be able to:
- Describe the meaning and purpose of open data, its benefits, and how FAIR principles are used.
- Recall methods to assess the reusability of data based on its documentation, and cite the data as instructed.
- Implement an open data management plan, select open data formats, add the needed documentation, including metadata, README files and version control, to make the data reusable and findable
- Evaluate whether your data should and can be shared.
- Recall practices to make data more accessible, including the registration of an affiliated DOI and the inclusion of citation instructions in documentation.

### Lesson 1: Introduction to Open Data

#### Overview
This lesson defines open data, its benefits, and the practices that enable data to be open. In addition, the lesson takes a closer look at how FAIR applies to open data as well as at the critical role of metadata. It wraps up with a brief discussion on how to plan for open data in the scientific workflow and tasks guided by the use, make, share framework.

#### 1.1 What Is Open Data?

**Definition:**
Open data is data that is freely available, accessible, and usable by anyone without legal, technical, or financial barriers. Open data can be freely used, modified, and shared by anyone for any purpose.

**Key Characteristics of Open Data:**

1. **Accessible:** Available through public repositories or distribution mechanisms
2. **Machine-readable:** Formatted in standard formats that computers can process
3. **Documented:** Accompanied by metadata explaining what, when, where, why, and how
4. **Licensed:** Released under a clear open license specifying permitted uses
5. **Findable:** Discoverable through repositories and search tools
6. **Reusable:** In formats and with documentation enabling use by others
7. **Non-proprietary:** Not locked in vendor-specific formats
8. **Traceable:** With clear attribution and provenance

**Examples of Open Data:**

**Publicly Available Open Data:**
- Climate data from NOAA, NASA, or ECMWF
- Genomic sequences from GenBank
- Published datasets from Open Data Commons
- Government statistical data (census, economic indicators)
- Environmental monitoring data from agencies

**Research-Generated Open Data:**
- Datasets accompanying published research papers
- Field measurements from ecology studies
- Astronomical observations from surveys
- Medical imaging datasets for research
- Survey responses from social science research

#### 1.2 Benefits of Open Data

**For Individual Researchers:**

- **Reproducibility:** Others can verify your analyses and conclusions
- **Visibility:** Your work is discoverable and citable
- **Collaboration:** Enables collaboration with researchers worldwide
- **Impact:** Increases citations and reach of your research
- **Career Advancement:** Demonstrates commitment to open science

**Example:** A climatologist shares temperature data spanning 30 years. Other researchers use this data for new analyses, discovering that sharing led to 5x more citations of the original dataset.

**For the Research Community:**

- **Acceleration:** Reduces redundant data collection efforts
- **New Discoveries:** Enables meta-analyses and novel combinations of datasets
- **Standardization:** Promotes consistent data collection and formats
- **Knowledge Accumulation:** Builds shared knowledge infrastructure
- **Equity:** Researchers at under-resourced institutions access the same data

**Example:** Open genomic databases enable researchers worldwide to conduct genome-wide association studies without funding for expensive sequencing.

**For Science and Society:**

- **Transparency:** Public funding leads to public data
- **Trust:** Scientific findings can be independently verified
- **Innovation:** Enables new applications beyond original research
- **Education:** Public datasets serve as teaching resources
- **Democracy:** Citizens can access government and research data

**Example:** Open air quality data from EPA enables citizen science projects, environmental justice research, and public awareness of pollution.

**For Funders and Policy Makers:**

- **Return on Investment:** Maximizes value of research funding
- **Compliance:** Meets funder mandates for open science
- **Monitoring:** Enables tracking of research outputs
- **Innovation:** Stimulates new research directions

#### 1.3 Why Open Data Matters: The FAIR Principles

The FAIR principles provide a framework for making data maximally useful for both humans and machines.

**What FAIR Stands For:**

**F - Findable**
- Data are described with sufficient detail that they can be discovered
- Unique persistent identifiers (DOIs) enable citation and tracking
- Metadata are indexed in searchable repositories
- Example: Zenodo DOI allows anyone to cite your dataset

**A - Accessible**
- Data can be retrieved using standard protocols
- Metadata remain accessible even if data are no longer available
- Access may require authentication but rules are clear
- Example: Data available via HTTP download or API

**I - Interoperable**
- Data use standard formats and vocabularies
- Data can be combined with other datasets
- Definitions are shared across disciplines
- Example: Using Darwin Core format for species occurrence data allows combining data from multiple projects

**R - Reusable**
- Data are released under clear licenses
- Sufficient metadata describes methods, limitations, and scope
- Provenance is documented
- Example: CC BY 4.0 license with comprehensive metadata enables reuse in any context with attribution

**FAIR Principles Illustrated:**

```
Data Accessibility Spectrum

Not FAIR                          FAIR
|
Closed → Proprietary → Documented → Standardized → Publicly available
No access   Restricted    Ad-hoc      Following     With metadata
            access        metadata     standards     and DOI
```

**FAIR is NOT the same as OPEN:**

- **FAIR:** Emphasizes how data are managed and documented
- **OPEN:** Emphasizes access and licensing
- **Goal:** Make data BOTH FAIR and OPEN when possible

**Example Comparison:**

| Aspect | Not FAIR | FAIR but Closed | FAIR and Open |
|--------|----------|-----------------|---------------|
| Format | Proprietary Excel | Standard CSV | Standard CSV |
| Documentation | Minimal or none | Comprehensive metadata | Comprehensive metadata |
| Location | Researcher's computer | Institutional repository | Public repository |
| License | None stated | Restricted, clear terms | Open (CC BY), clear terms |
| DOI | No | Yes | Yes |
| Findable | No | Repository search only | Indexed, searchable |

#### 1.4 The Critical Role of Metadata

**Definition:**
Metadata are "data about data" - information that describes the content, quality, condition, and other characteristics of data.

**Why Metadata Are Essential:**

1. **Understanding:** Others understand what the data represent
2. **Reproducibility:** Methods and protocols are documented
3. **Quality Assessment:** Users evaluate appropriateness for their use
4. **Searchability:** Data become discoverable through metadata
5. **Interoperability:** Standardized metadata enable data combination
6. **Preservation:** Ensures data remain interpretable over time

**Types of Metadata:**

**Descriptive Metadata:**
What the data represent - content and context

```yaml
Dataset Title: "Global Temperature Measurements 1980-2023"
Description: "Monthly surface air temperature measurements from 5,000+ meteorological stations worldwide"
Temporal Coverage: "1980-01-01 to 2023-12-31"
Spatial Coverage: "Global, 0.5 degree latitude/longitude grid"
Subject Keywords: "climate, temperature, meteorology, global"
Discipline: "Earth Sciences"
```

**Structural Metadata:**
How data are organized - file formats and organization

```yaml
File Format: "NetCDF"
Variables:
  - temperature (float32)
  - humidity (float32)
  - pressure (float32)
Dimensions:
  - time (87,600 monthly records)
  - latitude (360 values)
  - longitude (720 values)
```

**Administrative Metadata:**
Who, when, and how - access and management

```yaml
Creator: "National Weather Service"
Creation Date: "1980-01-15"
Last Updated: "2024-01-15"
License: "Creative Commons Attribution 4.0"
Repository: "NOAA Earth System Research Laboratories"
DOI: "10.25921/r47p-th54"
```

**Rights Metadata:**
Access and usage restrictions

```yaml
License: "CC BY 4.0"
Access Level: "Public"
Usage Restrictions: "Attribution required"
Confidentiality: "None"
Export Control: "Not restricted"
```

**Quality Metadata:**
Accuracy, completeness, and reliability

```yaml
Accuracy: "±0.5°C measurement error"
Completeness: "98.5% of expected measurements present"
Missing Data: "2.2% gap filling applied from nearby stations"
Validation: "Cross-checked against GISS dataset"
Version: "2.1 (Quality flags updated)"
```

**Minimal Metadata Checklist:**

At minimum, include:
- ✅ Title and description (what is this?)
- ✅ Creator/author (who made this?)
- ✅ Date created and last modified (when?)
- ✅ Temporal coverage (what time period?)
- ✅ Spatial coverage (what geographic area?)
- ✅ Methodology (how was it created?)
- ✅ Variable definitions (what do columns mean?)
- ✅ Units of measurement
- ✅ Missing data handling
- ✅ License/rights (how can it be used?)
- ✅ DOI or permanent identifier (where to cite?)
- ✅ Data quality notes (what are limitations?)

**Metadata Standards by Discipline:**

- **Dublin Core:** Generic, all disciplines
- **MIAPPE:** Minimum Information About a Plant Phenotyping Experiment
- **MIAME:** Minimum Information About a Microarray Experiment
- **EML:** Ecological Metadata Language
- **FGDC:** Federal Geographic Data Committee (GIS)
- **MIAPPE:** Plant phenotyping
- **Darwin Core:** Biodiversity occurrence data

**Creating Good Metadata:**

**Example README for a dataset:**

```markdown
# Global Temperature Dataset 1980-2023

## Overview
This dataset contains monthly surface air temperature measurements from over 5,000 meteorological stations worldwide, compiled from the National Weather Service network.

## Dataset Information
- **File Name:** global_temp_1980_2023_v2.1.nc
- **Format:** NetCDF4
- **Size:** 2.3 GB
- **Temporal Coverage:** January 1, 1980 - December 31, 2023
- **Spatial Coverage:** Global, 0.5°×0.5° latitude/longitude grid
- **Update Frequency:** Monthly, typically by the 15th of following month

## Variables

### temperature (Celsius)
- **Description:** Monthly mean surface air temperature
- **Units:** Degrees Celsius
- **Missing Value Code:** -9999
- **Data Type:** Float32
- **Accuracy:** ±0.5°C measurement error

### humidity (%)
- **Description:** Monthly mean relative humidity
- **Units:** Percent (0-100)
- **Missing Value Code:** -9999
- **Data Type:** Float32

### pressure (hPa)
- **Description:** Monthly mean atmospheric pressure
- **Units:** Hectopascals
- **Missing Value Code:** -9999
- **Data Type:** Float32

## Data Collection Methods
- **Instruments:** Standard thermometers, hygrometers, barometers
- **Station Types:** Climate, synoptic, and cooperative observer networks
- **Quality Control:** Automated range and consistency checks, followed by manual review
- **Calibration:** Instruments calibrated annually against standard reference thermometers

## Data Quality
- **Overall Completeness:** 98.5% of expected measurements present
- **Missing Data:** 2.2% gap-filled using interpolation from neighboring stations
- **Validation:** Cross-validated against GISS and Berkeley Earth datasets (r² > 0.98)
- **Known Issues:** 
  - Station closures: 234 stations closed between 1980-2023
  - Equipment changes: Updated to automated systems in 2010 (no systematic bias detected)
  - Relocations: 45 stations relocated (documented in station_changes.csv)

## Attribution and Citation
**Recommended Citation:**
```
Smith, J., Johnson, A., & Brown, B. (2024). Global Temperature Measurements 1980-2023. 
National Weather Service Data Repository. https://doi.org/10.25921/r47p-th54
```

**BibTeX:**
```bibtex
@dataset{smith2024global,
  author = {Smith, Jane and Johnson, Alice and Brown, Bob},
  title = {Global Temperature Measurements 1980-2023},
  year = {2024},
  publisher = {National Weather Service},
  doi = {10.25921/r47p-th54},
  url = {https://doi.org/10.25921/r47p-th54}
}
```

## License
**Creative Commons Attribution 4.0 International (CC BY 4.0)**

You are free to:
- Share: Copy and redistribute the material
- Adapt: Remix, transform, and build upon the material

Under the condition that you provide proper attribution.

## Contact
- **Data Steward:** Dr. Jane Smith (j.smith@weather.gov)
- **Technical Questions:** Data Support Team (data-support@weather.gov)
- **Issues:** Report at github.com/nws/temp-data/issues

## Version History
- **v1.0** (1980): Initial dataset release
- **v2.0** (2010): Incorporated automated station data
- **v2.1** (2024): Updated quality flags, revalidation against current standards

## Related Datasets
- Precipitation Measurements (same stations and temporal coverage)
- Station Metadata (location, elevation, instrument types)
- Quality Control Flags (detailed quality assessment per measurement)


#### 1.5 Open Data in the Research Workflow

**Where Open Data Fits in the Research Lifecycle:**

```
Research Workflow with Open Data Integration

┌─────────────────────────────────────────────────────────────┐
│ 1. RESEARCH DESIGN & PLANNING                              │
│    - Search open data for similar studies                  │
│    - Plan for data sharing in data management plan         │
│    - Choose open formats and standards                     │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ 2. DATA COLLECTION & GENERATION                            │
│    - Document methods and protocols                        │
│    - Create quality assurance procedures                   │
│    - Use standard formats and metadata schemes             │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ 3. DATA ANALYSIS                                           │
│    - Use and cite open datasets appropriately              │
│    - Document analysis workflows                           │
│    - Generate analysis-ready datasets                      │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ 4. PUBLICATION                                             │
│    - Include data availability statement                   │
│    - Cite datasets used                                    │
│    - Consider data publication concurrently                │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ 5. SHARING & ARCHIVING                                     │
│    - Publish to disciplinary or general repository         │
│    - Obtain DOI for citation                               │
│    - Maintain and update as needed                         │
│    - Archive for long-term preservation                    │
└─────────────────────────────────────────────────────────────┘
```

#### 1.6 The "Use, Make, Share" Framework for Data

**USE Open Data**
- Search for existing data before collecting new data
- Evaluate data quality and suitability
- Properly cite and acknowledge data sources
- Follow data terms and licenses

**MAKE Data Open**
- Plan for openness from the start
- Document thoroughly with metadata
- Choose open, non-proprietary formats
- Ensure data quality and completeness
- Address privacy and security concerns

**SHARE Data**
- Select appropriate repositories
- Create comprehensive documentation
- Obtain persistent identifiers (DOIs)
- Announce and promote access
- Archive for long-term preservation

**Integration Example:**

A researcher studying soil microbial communities:

1. **Uses** existing soil taxonomy datasets and published microbial sequences from NCBI
2. **Makes** new 16S rRNA sequencing data with detailed metadata about soil samples
3. **Shares** raw sequencing data on NCBI and analysis-ready data on Zenodo
4. **Enables** other researchers to reuse the data for meta-analyses

#### Summary

Open data is fundamental to modern research because it:
- **Increases reproducibility** through transparency and verification
- **Accelerates discovery** by enabling reuse and combination
- **Maximizes research impact** through citations and new applications
- **Serves the public good** through accessibility of research funded by taxpayers
- **Ensures data longevity** through archiving and preservation

By understanding FAIR principles, metadata importance, and the "Use, Make, Share" framework, researchers can effectively navigate the open data landscape and contribute to a more transparent, collaborative scientific enterprise.

:::{admonition} Activities for Lesson 1
:class: activity

Complete at least two of the following activities to apply FAIR principles and the Use-Make-Share framework:

**Activity 1.1: Evaluate Data Using FAIR Criteria**
Select a published open dataset in your field. Assess it using the FAIR criteria:
- **Findable:** Is there a DOI? Is it discoverable through repositories?
- **Accessible:** Can you easily download or access the data? Are there clear access instructions?
- **Interoperable:** Is the format standard for your field? Can you import it into common tools?
- **Reusable:** Is there sufficient metadata? Is the license clear? Would you know how to cite it?

Write 200-300 words reflecting on which FAIR criterion was best met and which needs improvement.

**Activity 1.2: Map the Use-Make-Share Framework**
Choose a research project you know well (yours or a published study). For each phase, identify:
- **USE:** What existing open datasets did this project build upon? What publicly available data sources were accessed?
- **MAKE:** What new data did the researchers create? How was it documented?
- **SHARE:** How were the results and data shared? Where can others access them?

Create a visual diagram or written summary showing how Use-Make-Share applied to this project.

**Activity 1.3: Explore a Disciplinary Data Repository**
Visit a major repository in your field (e.g., NCBI, Zenodo, discipline-specific repository). Explore:
- What types of data are stored?
- How is data organized and searchable?
- What metadata standards are used?
- How many datasets are available?
- What policies govern sharing?

Write 150-200 words describing what you learned and how you might use this repository.

**Deliverable:** Your choice of analysis from activities above (1-2 pages total).
:::

### Lesson 2: Using Open Data

#### Overview
In this lesson you learn how to discover, assess, and cite an open data set. You start by exploring repositories and learning about the issues and considerations for searching datasets. You then learn how to determine if the dataset is suitable for your use by learning what to review in documentation, licenses, and file formats. The lesson wraps up with a discussion about the importance of citing the datasets and how to read and follow citation instructions.

#### 2.1 Discovering Open Data

**Step 1: Identify Your Data Needs**

Before searching, clarify what you need:

**Questions to ask:**
- What variables/measurements do I need?
- What geographic area or population?
- What time period?
- What temporal resolution (daily, monthly, annual)?
- What level of quality/processing is needed (raw vs. processed)?

**Step 2: Where to Search for Open Data**

**General Data Repositories:**

- **Zenodo** (zenodo.org)
  - Covers all disciplines
  - 90+ million records
  - Integrates with GitHub
  - Strong preservation commitment

- **Figshare** (figshare.com)
  - All data types
  - User-friendly interface
  - Generous free storage
  - Easy DOI assignment

- **Dataverse** (dataverse.org)
  - Disciplinary or institutional
  - Version control for datasets
  - Supports complex metadata
  - Federated network

- **Open Science Framework (OSF)** (osf.io)
  - Project-based organization
  - Preprints and data
  - File storage and version control
  - Integration with other tools

**Discipline-Specific Repositories:**

- **Ecology/Biology:**
  - Dryad (dryad.org)
  - Knowledge Network for Biocomplexity (KNB)
  - GBIF (Global Biodiversity Information Facility)

- **Climate/Earth Sciences:**
  - NOAA Data Centers
  - NASA Earth Data
  - PANGAEA (oceanography)
  - ECMWF (European Centre for Medium-Range Weather Forecasts)

- **Genomics:**
  - NCBI Sequence Read Archive (SRA)
  - GenBank
  - Ensembl

- **Medical/Health:**
  - GEO (Gene Expression Omnibus)
  - dbGAP (Genetic variants)
  - PhysioBank (Physiological signals)

- **Social Sciences:**
  - ICPSR (Inter-university Consortium for Political and Social Research)
  - Harvard Dataverse
  - UK Data Archive

- **Astronomy:**
  - Mikulski Archive for Space Telescopes (MAST)
  - SDSS (Sloan Digital Sky Survey)
  - ESO (European Southern Observatory)

**Government Data Portals:**

- **data.gov** (US federal data)
- **data.europa.eu** (EU data)
- **data.gc.ca** (Canada)
- **data.gov.uk** (UK)

**Search Strategies:**

**Strategy 1: Keyword Search**

Better: "soil microbial community 16S rRNA sequencing"
Weaker: "microbial data"
Reason: Specific terms find more relevant results

**Strategy 2: Use Filters**
- Filter by date range, file type, license, discipline
- Most repositories allow advanced search

**Strategy 3: Citation Tracking**
- Find papers in your field
- See what datasets they cite
- Often data are reused across studies

**Strategy 4: Community Recommendations**
- Ask colleagues and collaborators
- Check domain-specific forums and mailing lists
- Look at literature reviews for standard datasets

**Example Search Workflow:**

A marine researcher searching for plankton data:

1. Google Scholar: Search "phytoplankton open data 2020-2023"
2. Find relevant papers, note cited datasets
3. Search PANGAEA for "phytoplankton time series"
4. Check NOAA Data Centers for related measurements
5. Filter results by geographic region of interest
6. Evaluate top 5 results for suitability

#### 2.2 Assessing Data Quality and Suitability

**Step 1: Review Documentation**

**Critical Elements to Check:**

**1. Data Description**
- What exactly does this dataset contain?
- What are the variables/measurements?
- What methods were used?
- What is the time period and geographic coverage?

**2. Completeness**
- What percentage of data is present?
- Are there known gaps?
- How were missing values handled?
- Is this acceptable for your use?

**3. Quality Information**
- What is the measurement accuracy/uncertainty?
- What quality control procedures were used?
- Are there known biases or limitations?
- Have results been validated against other sources?

**4. Methodology**
- How was data collected/generated?
- What instruments or methods were used?
- What are the processing steps?
- Are methods appropriate for your use case?

**5. Variable Definitions**
- What does each variable represent?
- What are the units?
- What are the data ranges?
- Are there special codes (e.g., -999 for missing)?

**Assessment Checklist:**

| Question | Yes | No | Notes |
|----------|-----|-----|--------|
| Do I understand what this data represents? | | | |
| Does it have geographic coverage I need? | | | |
| Does it have temporal coverage I need? | | | |
| Is data quality described and acceptable? | | | |
| Is methodology clearly documented? | | | |
| Are variable definitions provided? | | | |
| Is completeness/missing data addressed? | | | |
| Can I access the data format? | | | |
| Is the license permissive for my use? | | | |
| Can I get a persistent identifier (DOI)? | | | |
| Is version/update frequency appropriate? | | | |

**Step 2: Check the License**

**Common Data Licenses:**

**Creative Commons Licenses:**

- **CC0 (Public Domain):** No restrictions, use however you want
- **CC BY (Attribution):** Use freely, must cite creator
- **CC BY-SA (Attribution-ShareAlike):** Use freely, must cite, derivatives under same license
- **CC BY-NC (Attribution-Non-Commercial):** Use for non-commercial only, must cite
- **CC BY-ND (Attribution-No Derivatives):** Use as-is only, must cite, no modifications

**Open Data Commons Licenses:**

- **PDDL (Public Domain Dedication):** Full public domain
- **ODC-BY (Attribution):** Like CC-BY
- **ODC-ODbL (ODbL):** Database-specific, very permissive with share-alike

**Government Data:**
- Often in public domain (no restrictions)
- Check specific agency policies

**Proprietary/Restricted:**
- May require institutional access
- May have usage restrictions
- May require registration or fees

**Compatibility Assessment:**

**If you're publishing your work commercially:**
✅ Use CC0, CC BY, CC BY-SA, PDDL, ODC-BY
❌ Avoid CC BY-NC (no commercial use restriction)

**If you're publishing open source research:**
✅ Any CC or OD license works
✅ CC BY-SA and ODbL for derivative works sharing

**If you're creating proprietary derivative work:**
⚠️ Check carefully, most CC licenses require attribution even in commercial use

**Step 3: Evaluate File Formats**

**Open vs. Proprietary Formats:**

**Excellent (Open, Standard):**
- CSV (comma-separated values) - universal
- NetCDF - standard in Earth sciences
- HDF5 - standard for large scientific data
- JSON - modern, machine-readable
- Plain text with documentation

**Good (Open, Widely Used):**
- Excel (.xlsx) - ubiquitous, but proprietary format
- GeoTIFF - geospatial standard
- Shapefile - GIS standard (actually multiple files)
- ASCII/text data with metadata

**Problematic (Proprietary, Less Accessible):**
- SPSS .sav files
- SAS .sas7bdat files
- Stata .dta files
- Proprietary database formats
- Uncommon or custom formats

**Considerations:**
- Can I open the format with free/open software?
- Will the format be readable in 10 years?
- Is there documentation of the format?
- Do I have the specialized software needed?

**Conversion:**
If data are in a problematic format:
- Convert to open format (CSV, HDF5, NetCDF) if possible
- Document the conversion process
- Retain original file for reference

#### 2.3 Downloading and Accessing Data

**Download Methods:**

**Direct Download:**
- Simple for small files
- May have file size limits
- Good for one-time access

**FTP/SFTP:**
- For large files
- May require client software
- Faster for bulk downloads

**API (Application Programming Interface):**
- Programmatic access
- Ideal for automated workflows
- Example: NOAA Climate Data

**Database Queries:**
- Search and download specific subsets
- Common for large repositories
- Example: NCBI BLAST, GBIF web interface

**Bulk Data Transfer:**
- Amazon AWS, Google Cloud, etc.
- For very large datasets
- Often faster and cheaper than internet downloads

**Example Access Workflow:**

```python
# Programmatic access to NOAA climate data
import requests

# Search NOAA for temperature data
url = "https://www.ncei.noaa.gov/api/v1/data"
params = {
    'datasetid': 'GHCND',  # Global Historical Climatology Network Daily
    'stationid': 'GHCND:USW00013874',  # New York Central Park
    'startDate': '2020-01-01',
    'endDate': '2020-12-31',
    'limit': '1000'
}

response = requests.get(url, params=params)
data = response.json()

# Process and save data
import pandas as pd
df = pd.DataFrame(data['results'])
df.to_csv('temperature_data.csv', index=False)
```

#### 2.4 Citing Open Data

**Why Citation Matters:**

- **Gives Credit:** Acknowledges dataset creators and contributors
- **Enables Verification:** Others can access the exact data you used
- **Supports Data Infrastructure:** Citations justify continued funding for repositories
- **Enables Tracking:** Shows impact and reach of data
- **Required by Funders:** Most funding agencies require data citations

**Where to Find Citation Instructions:**

**1. Repository/Dataset Landing Page**
Most repositories have "Cite this dataset" buttons

**2. README or Documentation**
Dataset creators often provide recommended citation

**3. CITATION.cff File**
Machine-readable citation format

**4. Dataset Metadata**
Author, date, version information

**Citation Format Elements:**

**Required:**
- Author/creator names
- Publication year
- Dataset title
- Repository name
- Persistent identifier (DOI, URL, or accession number)

**Recommended:**
- Version number
- Access date (if no version)
- URL/location

**Example Citations:**

**Harvard Style:**
```
Smith, J., Johnson, A., & Brown, B., 2024. Global Temperature 
Measurements 1980-2023. National Weather Service Data Repository. 
https://doi.org/10.25921/r47p-th54. Accessed: 15 January 2024.
```

**APA Style:**
```
Smith, J., Johnson, A., & Brown, B. (2024). Global temperature 
measurements 1980-2023 [Data set]. National Weather Service Data Repository. 
https://doi.org/10.25921/r47p-th54
```

**Chicago Style:**
```
Smith, Jane, Alice Johnson, and Bob Brown. "Global Temperature 
Measurements 1980-2023." Dataset. National Weather Service Data 
Repository. https://doi.org/10.25921/r47p-th54. Accessed January 15, 2024.
```

**BibTeX:**
```bibtex
@dataset{smith2024global,
  author = {Smith, Jane and Johnson, Alice and Brown, Bob},
  title = {Global temperature measurements 1980-2023},
  year = {2024},
  publisher = {National Weather Service Data Repository},
  doi = {10.25921/r47p-th54}
}
```

**In Text:**
```
Temperature data were obtained from the National Weather Service 
global dataset (Smith et al., 2024).

We analyzed 44 years of temperature observations (Smith et al., 2024) 
to identify trends.
```

**Data Availability Statement (for papers):**

```markdown
## Data Availability

The temperature dataset used in this analysis is publicly available 
at the National Weather Service Data Repository (https://doi.org/10.25921/r47p-th54). 
The dataset is distributed under a Creative Commons Attribution 4.0 
International License. Code for reproducing the analyses is available 
at https://github.com/jsmith/temperature-analysis.
```

**Version-Specific Citations:**

If data have versions, cite the specific version used:

```
Smith, J., Johnson, A., & Brown, B., 2024. Global Temperature 
Measurements 1980-2023 (v2.1). National Weather Service Data Repository. 
https://doi.org/10.25921/r47p-th54.v2.1
```

#### 2.5 Data Integration and Reuse

**Combining Multiple Datasets:**

**Challenges:**
- Different formats and structures
- Different temporal or spatial resolution
- Different quality standards
- Inconsistent variable definitions

**Best Practices:**

1. **Document the integration process**
   - Keep track of data transformations
   - Note any quality differences
   - Record merge keys and logic

2. **Verify compatibility**
   - Check temporal and spatial overlap
   - Verify unit consistency
   - Test on subset before full merge

3. **Maintain traceability**
   - Keep original files
   - Document all processing steps
   - Version the integrated dataset

**Example Integration Workflow:**

```python
# Combining climate and biological datasets
import pandas as pd

# Load datasets
temp_data = pd.read_csv('temperature_1980_2023.csv')
biology_data = pd.read_csv('plant_phenology_observations.csv')

# Check temporal overlap
print(f"Temperature: {temp_data['date'].min()} to {temp_data['date'].max()}")
print(f"Biology: {biology_data['date'].min()} to {biology_data['date'].max()}")

# Merge on date and location
merged = pd.merge(
    temp_data,
    biology_data,
    on=['date', 'latitude', 'longitude'],
    how='inner'  # Keep only matching records
)

# Document the merge
print(f"Original temperature records: {len(temp_data)}")
print(f"Original biology records: {len(biology_data)}")
print(f"Merged records: {len(merged)}")

# Save with documentation
merged.to_csv('integrated_climate_biology.csv', index=False)

# Create README documenting the merge
readme = """
# Integrated Climate-Biology Dataset

Created: 2024-01-15

## Source Datasets
1. Global Temperature Measurements (doi:10.25921/r47p-th54)
2. Plant Phenology Observations (doi:10.1234/example)

## Integration Method
- Merged on date, latitude, longitude
- Temperature data at 0.5° resolution, resampled to match biology observations
- 10,234 matching records across both datasets

## Temporal Coverage
- 1980-2023

## Citations
... [cite both original datasets]
"""

with open('README.md', 'w') as f:
    f.write(readme)
```

#### Summary

Effectively using open data requires:
1. **Discovery:** Knowing where to search and how to find relevant datasets
2. **Assessment:** Evaluating data quality, licensing, and suitability for your work
3. **Access:** Understanding download options and data formats
4. **Citation:** Properly crediting dataset creators and enabling reproducibility
5. **Integration:** Combining datasets while maintaining quality and traceability

By developing these skills, you maximize the value of open data and contribute to reproducible, trustworthy science.

:::{admonition} Activities for Lesson 2
:class: activity

Complete at least two of the following activities to practice finding, assessing, and citing open data:

**Activity 2.1: Conduct a Data Discovery Search**
Search for an open dataset relevant to your research interests using at least two different approaches:
- Method 1: Search a general repository (Zenodo, Figshare, or data.gov)
- Method 2: Search a discipline-specific repository

For each dataset found, document:
- Title and creators
- Brief description
- How you discovered it
- Why it might be useful for your work

Write a brief summary (150-200 words) comparing the search experience across repositories.

**Activity 2.2: Assess Data Quality and Suitability**
Select one open dataset you found in Activity 2.1 (or choose a different dataset). Complete the assessment checklist:
- Is the purpose and methodology clear?
- Is the time period and geographic coverage appropriate for your use?
- Is completeness/missing data documented?
- Is quality described and acceptable?
- Can you understand all variables and units?
- Is the license permissive for your intended use?

Write 200-300 words explaining whether this dataset would be suitable for your research and any limitations you identified.

**Activity 2.3: Practice Data Citation**
Find a published dataset with a DOI. Locate the recommended citation format (usually on the repository page or in documentation). Create citations in at least two formats:
- APA format
- BibTeX format

Document the citation and reflect on why proper data citation matters for reproducibility.

**Deliverable:** Your choice of output from activities above (1-2 pages total).
:::

### Lesson 3: Making Open Data

#### Overview
In this lesson, you learn the criteria and tasks needed to ensure that the datasets you make are open and reusable. The lesson starts with a discussion on creating a data management plan and then continues with topics on selecting open data formats and how to include metadata, readme files, and version control for your data. It wraps up with a discussion on open licenses for data.

#### 3.1 Creating a Data Management Plan (DMP)

**What is a Data Management Plan?**

A Data Management Plan (DMP) is a document describing how data will be created, documented, preserved, and shared throughout and after a research project.

**Why Create a DMP?**

- **Funder Requirements:** Most funding agencies require DMPs
- **Planning Tool:** Ensures data is managed well from the start
- **Best Practices:** Guides proper documentation and archiving
- **Compliance:** Demonstrates commitment to open science
- **Sustainability:** Plans for long-term preservation

**When to Create:**
- **Ideal:** Before research begins, as part of proposal
- **Acceptable:** Early in project during planning
- **Update:** Revise as project evolves

**3.1.1 DMP Components**

**1. Data Collection and Generation**

```markdown
## Data Collection

### What Data Will Be Generated?
- Type: 16S rRNA amplicon sequencing reads
- Format: FASTQ format
- Volume: ~5 TB (50,000 samples × 100 MB each)
- Resolution: 50,000 samples from global soils

### How Will Data Be Generated?
- Method: Illumina MiSeq sequencing
- Protocol: Earth Microbiome Project standard protocol
- Quality control: Sequencing quality flags, taxonomy validation
- Standards: Data will follow EMP standards for microbial genomics

### Timeline
- Months 1-24: Active sampling and sequencing
- Months 25-30: Final processing and quality control
```

**2. Data and Metadata Standards**

```markdown
## Standards and Formats

### Metadata
- Standard: MIAPPE (Minimum Information About a Plant Phenotyping Experiment)
- Also capture: Sample location, collection date, storage conditions
- Format: JSON metadata files accompanying each dataset

### File Formats
- Raw sequences: FASTQ format
- Processed sequences: FASTA format
- Taxonomy tables: CSV format
- Quality scores: SAM/BAM format

### Data Dictionary
- Column definitions provided for all CSV files
- Variable definitions included in metadata
- Units of measurement specified
```

**3. Data Storage and Backup**

```markdown
## Storage

### Primary Storage (During Project)
- Location: University computing cluster
- Capacity: 10 TB raw + 10 TB backup
- Backup: Daily automated backups to university storage
- Access: Lab members via secure SSH access
- Redundancy: RAID 6 storage with 2-disk failure tolerance

### Archival Storage (Post-Project)
- Primary: Zenodo repository
- Backup: University institutional repository
- Format: FAIR-compliant with comprehensive metadata
```

**4. Data Quality and Organization**

```markdown
## Quality Control

### During Collection
- Field replicates: 5% of samples
- Positive/negative controls in every sequencing run
- Regular quality metrics reported

### During Processing
- Sequence quality filtering (Q > 20)
- Contamination screening
- Duplicate removal
- Cross-contamination assessment

### Data Organization
```
project_data/
├── raw_sequences/
│   ├── run_2024_01/
│   ├── run_2024_02/
│   └── run_2024_03/
├── processed/
│   ├── qc_filtered/
│   ├── taxonomic_assignments/
│   └── abundance_tables/
├── metadata/
│   ├── sample_metadata.csv
│   ├── collection_protocol.md
│   └── processing_log.txt
└── documentation/
    ├── README.md
    ├── METADATA.md
    └── DATA_DICTIONARY.csv
```

**5. Data Access and Sharing**

```markdown
## Sharing Plan

### Timeline
- Months 1-24: Data embargoed (private to lab)
- Month 25 (at publication): Raw sequences released
- Month 26: Processed data and analysis code released

### Repository
- NCBI Sequence Read Archive (SRA) for raw sequences
- Zenodo for processed data and analysis
- GitHub for analysis code

### License
- Raw sequences: CC0 (public domain)
- Processed data: CC BY 4.0 (requires attribution)
- Code: MIT License

### Access Control
- No authentication required for published data
- Metadata will be searchable in repository
```

**6. Data Retention and Preservation**

```markdown
## Long-Term Preservation

### Retention Period
- Raw data: 7 years minimum (per funding agency)
- Processed data: Permanent in Zenodo
- Metadata: Permanent

### Maintenance Responsibilities
- Years 1-5: PI responsible for data stewardship
- Years 5+: Zenodo and NCBI provide archival preservation
- Plan for transition of access if PI moves institutions

### Disaster Recovery
- Regular verification of archival integrity
- Documentation preserved on university servers
- Code and analysis preserved on GitHub
```

**3.1.2 DMP Templates**

Templates available from:
- **DMPTool** (dmptool.org) - Free, funder-specific templates
- **Data Stewardship Wizard** (ds-wizard.org) - Interactive guidance
- **University Library:** Ask your data librarian
- **Funder Guidelines:** NIH, NSF, EU, etc. provide examples

#### 3.2 Selecting Open Data Formats

**Why Format Matters:**

- **Longevity:** Some formats become obsolete
- **Accessibility:** Standard formats are universally readable
- **Interoperability:** Open formats enable data combination
- **Reproducibility:** Standard formats ensure consistent interpretation

**Best Practices for Data Formats:**

**Text-Based Formats (Excellent):**

**CSV (Comma-Separated Values)**
- ✅ Universal, readable by any software
- ✅ Preserves data integrity
- ✅ Human-readable
- ✅ Version control friendly
- ❌ Limited for complex data structures
- **Use for:** Tabular data, spreadsheets

**Example CSV:**
```csv
date,location,temperature,humidity,pressure
2024-01-01,Station_A,5.2,65,1013.25
2024-01-02,Station_A,6.1,68,1013.50
2024-01-03,Station_A,4.8,72,1012.80
```

**JSON (JavaScript Object Notation)**
- ✅ Flexible, handles complex structures
- ✅ Human-readable
- ✅ Machine-parseable
- ✅ Widely supported
- **Use for:** Hierarchical data, metadata

**Example JSON:**
```json
{
  "dataset": {
    "title": "Temperature measurements",
    "date_created": "2024-01-01",
    "measurements": [
      {
        "date": "2024-01-01",
        "location": "Station_A",
        "temperature": 5.2,
        "humidity": 65
      }
    ]
  }
}
```

**Scientific Formats (Excellent for Domain):**

**NetCDF (Network Common Data Form)**
- ✅ Standard for Earth sciences, climate, oceanography
- ✅ Efficient for large multidimensional arrays
- ✅ Includes metadata
- ❌ Requires specialized software to read
- **Use for:** Climate, oceanography, atmospheric data

**HDF5 (Hierarchical Data Format)**
- ✅ Excellent for very large datasets
- ✅ Efficient compression
- ✅ Hierarchical organization
- ❌ Specialized software required
- **Use for:** Large scientific datasets, image data

**Binary Formats (Generally Good):**

**GeoTIFF (Geospatial Tagged Image File Format)**
- ✅ Standard for geospatial raster data
- ✅ Self-describing (includes coordinate system)
- ✅ Readable by many GIS tools
- **Use for:** Satellite imagery, raster maps

**Shapefile**
- ✅ Standard for GIS vector data
- ⚠️ Actually multiple related files
- **Use for:** Maps, geographic features

**Formats to Avoid:**

**Proprietary Formats (Problematic):**
- ❌ SPSS (.sav), SAS (.sas7bdat), Stata (.dta)
- ❌ Require paid software
- ❌ May not be readable in future
- **If necessary:** Provide conversion to open format or detailed format documentation

**Obsolete Formats:**
- ❌ floppy disk formats
- ❌ Ancient proprietary database formats
- ❌ Formats no longer supported

**Recommendations by Data Type:**

| Data Type | Recommended Format | Alternative | Avoid |
|-----------|-------------------|-------------|-------|
| Tabular | CSV | Excel (.xlsx) | SPSS, Stata, SAS |
| Large array | NetCDF/HDF5 | Binary with docs | Proprietary |
| Geospatial raster | GeoTIFF | NetCDF | Proprietary GIS |
| Geospatial vector | Shapefile | GeoJSON | Proprietary GIS |
| Sequences | FASTA/FASTQ | Plain text | Proprietary |
| Images | TIFF/PNG | JPEG (lossy) | Proprietary formats |
| Time series | NetCDF/CSV | HDF5 | Binary, no docs |
| Metadata | JSON/YAML | XML | Proprietary |

#### 3.3 Creating Comprehensive Metadata

**Metadata Documentation Requirements:**

**1. Variable Definitions**

For each column/variable in your dataset:

```markdown
## Variable Dictionary

### temperature
- **Description:** Hourly mean surface air temperature
- **Units:** Degrees Celsius
- **Data Type:** Float (4 bytes)
- **Missing Value Code:** -9999
- **Accuracy:** ±0.5°C
- **Measurement Instrument:** Thermometer model XYZ
- **Precision:** 0.1°C
- **Valid Range:** -40 to +60°C

### humidity
- **Description:** Hourly mean relative humidity
- **Units:** Percent (0-100)
- **Data Type:** Float (4 bytes)
- **Missing Value Code:** -9999
- **Accuracy:** ±2%
- **Measurement Instrument:** Hygrometer model ABC
```

**2. Collection Methods**

```markdown
## Methodology

### Data Collection
- **Protocol:** Standard meteorological measurement protocols (WMO guidelines)
- **Frequency:** Hourly measurements
- **Start Date:** 1980-01-01
- **End Date:** 2023-12-31
- **Number of Stations:** 5,000 worldwide
- **Instruments:** Calibrated thermometers, hygrometers, barometers
- **Calibration:** Annual calibration against standard references
- **Quality Control:** Real-time automated checks, manual review of anomalies

### Data Processing
- **Raw Data:** Original hourly measurements from instruments
- **Step 1:** Data validation and error checking
- **Step 2:** Interpolation for missing values (2.2% of data)
- **Step 3:** Aggregation to monthly means
- **Step 4:** Quality flag assignment
```

**3. Data Provenance and Version History**

```markdown
## Provenance

### Original Data Source
- National Weather Service
- Collection began: 1980-01-01
- Collectors: NWS cooperative observer network

### Processing History
- Version 1.0 (1980): Initial dataset compilation
- Version 1.5 (2000): Added automated station data
- Version 2.0 (2010): Reprocessed with updated QC procedures
- Version 2.1 (2024): Quality flag updates, new validation against GISS

### Current Version
- Version: 2.1
- Released: 2024-01-15
- Modifications: Quality flag improvements
```

**4. Quality Assessment**

```markdown
## Data Quality

### Completeness
- Target: 100% of expected measurements
- Achieved: 98.5%
- Missing: 2.2% gap-filled using interpolation from neighbors
- Explanation: 234 station closures account for most gaps

### Accuracy
- Measurement error: ±0.5°C
- Calibration: Annual calibration against standards
- Validation: Cross-checked against GISS (r² = 0.98)

### Consistency
- Equipment changes: Documented (2010 transition to automated systems)
- No systematic bias detected post-equipment change
- Station relocations: 45 stations, documented in station_changes.csv

### Known Issues
- Urban heat island effect: Present in some urban stations
- Documented in station metadata
- Recommend caution for urban trend analysis
```

**5. Access and Use Restrictions**

```markdown
## Access and Use Information

### License
- CC BY 4.0 (Creative Commons Attribution 4.0 International)
- Full license text: https://creativecommons.org/licenses/by/4.0/

### Attribution Required
When using this data, cite as:
Smith et al. (2024). Global Temperature Measurements 1980-2023. 
https://doi.org/10.25921/r47p-th54

### No Restrictions On
- Redistribution
- Modification
- Commercial use
- Creating derivatives

### Restrictions
- Must provide attribution
- Cannot hold licensor liable
- Cannot imply endorsement of your use

### Recommended Restrictions on Users
- None

### Data Sensitivity
- Public data, no sensitive information
- Contains no personal information
- No export controls apply
```

**Creating Machine-Readable Metadata (YAML):**

```yaml
# METADATA.yaml
Dataset:
  Title: "Global Temperature Measurements 1980-2023"
  Description: "Monthly surface air temperature from 5000+ stations worldwide"
  Creator:
    Name: "National Weather Service"
    Email: "data@weather.gov"
  DateCreated: 2024-01-15
  DateModified: 2024-01-15
  TemporalCoverage:
    StartDate: 1980-01-01
    EndDate: 2023-12-31
  SpatialCoverage:
    BoundingBox:
      North: 90
      South: -90
      East: 180
      West: -180
  Variables:
    - Name: "temperature"
      Description: "Monthly mean surface air temperature"
      Units: "Celsius"
      DataType: "float32"
    - Name: "humidity"
      Description: "Monthly mean relative humidity"
      Units: "percent"
      DataType: "float32"
  License:
    Type: "Creative Commons Attribution 4.0"
    URL: "https://creativecommons.org/licenses/by/4.0/"
  Doi: "10.25921/r47p-th54"
  Keywords:
    - "climate"
    - "temperature"
    - "meteorology"
    - "global"
```

#### 3.4 Documentation Files

**Essential Documentation:**

**README.md** (We covered this in Lesson 1)
- Overview and description
- Variable definitions
- Methods
- Limitations and known issues
- Citation instructions
- Contact information

**DATA_DICTIONARY.csv**

For tabular data, provide a CSV file defining every column:

```csv
Column_Name,Description,Data_Type,Units,Valid_Range,Missing_Value,Source
date,Observation date,Date (YYYY-MM-DD),NA,1980-01-01 to 2023-12-31,NA,Original records
station_id,Unique station identifier,Text,NA,10001-99999,NA,NWS station network
latitude,Station latitude,Float,Degrees,-90 to 90,NA,GPS/map coordinates
longitude,Station longitude,Float,Degrees,-180 to 180,NA,GPS/map coordinates
temperature,Mean hourly temperature,Float,Celsius,-40 to 60,-9999,Thermometer readings
humidity,Mean relative humidity,Float,Percent,0 to 100,-9999,Hygrometer readings
quality_flag,Data quality assessment,Integer,Code,0-5,-9999,QC procedures
```

**METHODS.md**

Detailed description of data collection and processing:

```markdown
# Methodology

## Data Collection

### Sampling Design
- 5,000 meteorological stations across 180 countries
- Stratified sampling: 10% urban, 30% suburban, 60% rural
- Random site selection within each stratum

### Measurement Protocols
- Follow World Meteorological Organization (WMO) guidelines
- Instruments: Mercury thermometers ≤2010, electronic ≥2010
- Measurement frequency: Hourly
- Recording precision: 0.1°C

### Quality Assurance
- Daily automated checks for:
  - Out-of-range values
  - Temporal consistency
  - Spatial continuity
- Monthly manual review of flagged data
- Annual audits of random sample (2% of stations)

## Data Processing

### Step 1: Quality Control
- Remove obviously erroneous values
- Flag suspicious values (e.g., >2 SD from local mean)
- Maintain original values while flagging

### Step 2: Missing Data
- Interpolate missing values using neighboring stations
- Weights based on distance and elevation
- Flag interpolated values

### Step 3: Aggregation
- Calculate monthly means from hourly data
- Discard months <80% complete
- Report number of contributing observations

### Step 4: Validation
- Compare against satellite data (MODIS)
- Compare against other station networks (GISS)
- Cross-correlation: r² > 0.95 required
```

**VERSION.txt** or **CHANGELOG.md**

```markdown
# Version History

## Version 2.1 (2024-01-15)
- Updated quality control procedures
- Added enhanced validation against GISS dataset
- Fixed 3 data points with known instrument errors
- Improved missing data documentation

## Version 2.0 (2010-06-30)
- Incorporated automated station network
- Reprocessed all historical data with new QC
- Extended to include humidity and pressure
- Changed format from ASCII to NetCDF

## Version 1.5 (2000-12-31)
- Extended coverage to 180 countries
- Added automated data entry validation

## Version 1.0 (1980-01-01)
- Initial compilation from NWS archives
```

#### 3.5 Version Control for Data

**Why Version Control Matters for Data:**

- Tracks changes and who made them
- Enables reverting to previous versions
- Documents why changes were made
- Enables collaboration on data updates

**Options for Data Version Control:**

**Git (with care):**
- ✅ Works well for small-medium datasets
- ✅ Good for tabular CSV data
- ❌ Poor for large binary files (>100MB)
- ❌ Not ideal for frequently changing data

**Zenodo Versions:**
- ✅ Designed for data versioning
- ✅ Each version gets its own DOI
- ✅ Automatic version tracking
- ✅ Good for release versions

**Dataverse Versions:**
- ✅ Similar to Zenodo
- ✅ Good for academic institutional use
- ✅ Version control built-in

**Version Numbering Scheme:**

Use semantic versioning: MAJOR.MINOR.PATCH

- **MAJOR:** Incompatible changes (new structure, removed fields)
- **MINOR:** Added data or features (new time period, new stations)
- **PATCH:** Bug fixes, quality improvements

**Example:**
- v1.0 - First release
- v1.1 - Added 100 new stations
- v1.2 - Fixed 5 data quality issues
- v2.0 - Restructured file format (incompatible)

**Documenting Data Changes:**

```markdown
# Change Log

## v2.1 (2024-01-15)
### Changed
- Updated quality control procedures
- Enhanced validation against GISS dataset

### Fixed
- 3 temperature measurements with instrument drift issues
- Station coordinates for 12 relocated stations

### Added
- New field: quality_score (0-100)
- Documentation of station equipment changes

## v2.0 (2010-06-30)
### Breaking Changes
- Format changed from ASCII to NetCDF
- Data structure reorganized

### Added
- Humidity measurements
- Pressure measurements
```

#### 3.6 Open Data Licensing

**License Selection for Data:**

The same principles apply as for code, but some differences exist.

**Recommended: Creative Commons Licenses**

**CC0 (Public Domain)**
- ✅ Maximum freedom
- ✅ No attribution required
- ✅ Best for data shared as global resource
- ❌ No recognition for creators
- **Use for:** Public datasets, foundational data

**CC BY (Attribution)**
- ✅ Very permissive
- ✅ Clear attribution requirement
- ✅ Widely accepted in academia
- ✅ Good balance
- **Use for:** Most research datasets
- **Example:** Global Temperature Measurements

**CC BY-SA (Attribution-ShareAlike)**
- ✅ Derivatives must use same license
- ✅ Ensures openness propagates
- ❌ More restrictive
- **Use for:** Data meant to remain open

**Not Recommended: Restrictive Licenses**

❌ **CC BY-NC:** No commercial use restriction
- Limits use in industry and applied research
- Difficult to enforce
- Reduces data utility

❌ **CC BY-ND:** No derivatives allowed
- Prevents data reuse and improvement
- Defeats purpose of open data
- Very restrictive

**Open Data Commons Licenses** (for databases specifically):

- **PDDL** (Public Domain Dedication and License): Like CC0
- **ODC-BY** (Attribution): Like CC BY
- **ODbL** (Open Data Commons Open Database License): Like CC BY-SA, with database-specific legal framework

**License Compatibility Matrix:**

| Your License | Can Use CC BY | Can Use CC BY-SA | Can Use ODbL | Can Use CC0 |
|------|------|------|------|------|
| CC BY | ✅ | ✅ | ✅ | ✅ |
| CC BY-SA | ⚠️ Must use SA | ✅ | ⚠️ Database specific | ✅ |
| ODbL | ⚠️ Database only | ⚠️ Database only | ✅ | ✅ |
| CC0 | ✅ | ✅ | ✅ | ✅ |

**Applying a License to Your Data:**

1. **Choose license** - Use CC BY for most research data
2. **Add LICENSE file** to your data directory
3. **Include in README** - State license clearly
4. **Add to metadata** - Include license information
5. **Communicate clearly** - Make licensing obvious

**Example License Statement:**

```markdown
## License

This dataset is released under the Creative Commons Attribution 4.0 
International License (CC BY 4.0).

You are free to:
- Share: Copy and redistribute the material in any medium or format
- Adapt: Remix, transform, and build upon the material

Under the condition that you provide proper attribution.

Full license: https://creativecommons.org/licenses/by/4.0/

### How to Cite
Smith et al. (2024). Global Temperature Measurements 1980-2023. 
National Weather Service Data Repository. https://doi.org/10.25921/r47p-th54
```

#### Summary

Making open data requires:
1. **Planning:** DMPs guide data management from start
2. **Format Selection:** Choose open, standard formats
3. **Documentation:** Comprehensive metadata and README files
4. **Organization:** Clear file structure and naming
5. **Version Control:** Track changes and releases
6. **Licensing:** Apply clear, permissive licenses

By following these practices, you ensure your data is reusable, discoverable, and valuable to the research community for years to come.

:::{admonition} Activities for Lesson 3
:class: activity

Complete at least two of the following activities to practice preparing data for sharing:

**Activity 3.1: Create a Data Management Plan (DMP) Section**
Write the data management section of a DMP for a real or hypothetical research project. Include:
- Description of data to be created (type, volume, time period)
- Data and file standards/formats you will use and why
- Approaches to data and metadata documentation
- Policies for data and metadata access and sharing
- Plan for archiving and preservation

Follow the template from a major funder (NSF, NIH, or NSF.gov/bfa/dias/policy/dmp.jsp). Aim for 500-750 words.

**Activity 3.2: Design Metadata and README Documentation**
Select a real or hypothetical dataset. Create comprehensive documentation:
- **Metadata record:** Title, creators, description, keywords, discipline, temporal/geographic coverage, license
- **README file:** Overview of dataset, variable definitions, methodology, data quality, usage notes, citation format
- **Data dictionary:** Table listing each variable/column with units, data type, and description

Ensure documentation is clear enough that someone unfamiliar with your project could use the data.

**Activity 3.3: Choose Appropriate Licenses and Formats**
For a dataset you work with (or a hypothetical one), document:
- Your choice of open license (CC0, CC BY, CC BY-SA) and justification
- File format selection—what formats will you use and why?
- How formats ensure interoperability and long-term accessibility
- Any format conversions needed for different use cases

Write a brief summary (150-200 words) explaining these choices.

**Deliverable:** Your choice of output from activities above (2-3 pages total).
:::

### Lesson 4: Sharing Open Data

#### Overview
In this lesson, you learn about the practice of sharing your data. The discussion starts with a review of the sharing process and how to evaluate if your data are sharable. Next, you take a look at ensuring your data is accessible with a closer look at repositories and the lifecycle of data accessibility from the selecting a repository to maintaining and archiving your data. The lesson then discusses some steps to make the data as reusable as possible, and concludes with a section about considering who will help with the data sharing process.

#### 4.1 Evaluating Data Shareability

**Can Your Data Be Shared?**

**✅ Data That Should Be Shared:**

1. **Research datasets supporting publications**
   - Essential for reproducibility
   - Often required by journals and funders
   - Enables meta-analyses and follow-up research

2. **Public interest data**
   - Environmental monitoring
   - Health/epidemiology data (de-identified)
   - Climate and weather data
   - Economic and social data

3. **Data without sensitive information**
   - Derived or processed data (not raw sensitive data)
   - Already in public domain
   - De-identified or aggregated

4. **Foundational datasets**
   - Reference genomes
   - Climate normals
   - Geographic basemaps
   - Standard reference materials

**⚠️ Data That May Have Restrictions:**

1. **Personally Identifiable Information (PII)**
   - Names, addresses, phone numbers
   - Medical records (unless de-identified)
   - Financial information
   - Biometric data
   
   **Solutions:**
   - De-identify: Remove or encrypt personal identifiers
   - Aggregate: Combine individuals into groups
   - Synthesize: Create synthetic data with same statistical properties
   - Secure access: Restrict to authorized researchers

2. **Protected Health Information (PHI)**
   - Medical diagnoses
   - Treatment records
   - Health insurance information
   
   **Solutions:**
   - De-identify per HIPAA Safe Harbor method
   - Get IRB approval for sharing
   - Use secure limited datasets
   - Implement Data Use Agreements

3. **Human Subject Data**
   - Genetic information
   - Behavioral data
   - Survey responses
   
   **Solutions:**
   - Obtain informed consent for sharing
   - Verify IRB approval allows sharing
   - Use controlled access repositories
   - Implement data sharing agreements

4. **Proprietary or Licensed Data**
   - Data from commercial sources
   - Licensed databases
   - Data with use restrictions
   
   **Solutions:**
   - Check licensing terms
   - Request permission from licensor
   - Share processed derivatives if allowed
   - Reference original source

5. **Sensitive Location or Species Data**
   - Endangered species locations
   - Sacred or culturally sensitive sites
   - Critical infrastructure locations
   
   **Solutions:**
   - Aggregate to coarser resolution
   - Remove exact coordinates
   - Request restricted access
   - Consult with affected communities

6. **Export-Controlled or Restricted Data**
   - Dual-use research of concern
   - Strategic or national security data
   - Some cryptographic or biosecurity information
   
   **Solutions:**
   - Consult institutional export control officer
   - Obtain necessary approvals
   - Redact or remove restricted portions
   - Consider international collaboration agreements

**Sharing Decision Framework:**

```
Start: Should I share this data?
       |
       ├─→ Does it contain PII or PHI?
       │    YES → De-identify or restrict access
       │    NO → Continue
       ├─→ Is it licensed/proprietary?
       │    YES → Get permission or share derivatives
       │    NO → Continue
       ├─→ Is there export control concern?
       │    YES → Consult compliance office
       │    NO → Continue
       ├─→ Would sharing violate privacy/consent?
       │    YES → Modify consent or data
       │    NO → Continue
       └─→ No blockers → SHARE IT!
```

#### 4.2 Selecting Data Repositories

**What Makes a Good Data Repository?**

**Essential Features:**
1. **Persistence:** Will it be maintained long-term?
2. **Preservation:** Does it archive data permanently?
3. **Discoverability:** Is it searchable and indexed?
4. **Access:** Is data freely available?
5. **DOI:** Do you get a persistent identifier?
6. **Metadata:** Does it capture comprehensive metadata?

**General-Purpose Repositories:**

**Zenodo** (zenodo.org)
- **Pros:**
  - Free unlimited storage
  - DOI automatically assigned
  - Strong preservation (CERN backing)
  - All disciplines
  - GitHub integration
  - Excellent search interface
- **Cons:**
  - Less discipline-specific than some alternatives
- **Cost:** Free
- **Best for:** Datasets for papers, multi-disciplinary data

**Figshare** (figshare.com)
- **Pros:**
  - User-friendly interface
  - 20 GB free storage per user
  - DOI automatically assigned
  - Good for figures, datasets, code
  - Beautiful data visualizations
- **Cons:**
  - Free storage limits (larger datasets require payment)
- **Cost:** Free up to 20GB
- **Best for:** Individual datasets, figures, multi-media

**Dataverse** (dataverse.org)
- **Pros:**
  - Federated network of institutional repositories
  - Built-in version control
  - Advanced metadata support
  - Academic-friendly
- **Cons:**
  - Varies by institution
- **Cost:** Usually free through institution
- **Best for:** Academic institutions, longitudinal studies

**Open Science Framework (OSF)** (osf.io)
- **Pros:**
  - Good for organizing whole projects
  - Version control and documentation
  - Integrates with other tools
- **Cons:**
  - Less specialized for data preservation
- **Cost:** Free
- **Best for:** Open science workflows, project organization

**Discipline-Specific Repositories:**

**Life Sciences:**
- **NCBI Sequence Read Archive (SRA):** Raw sequencing data
- **Gene Expression Omnibus (GEO):** Microarray and sequencing expression data
- **Dryad:** Life sciences datasets from publications
- **GBIF:** Biodiversity occurrence data
- **PhysioBank:** Physiological signals and time series

**Earth & Environmental Sciences:**
- **NOAA Data Centers:** Climate, oceanography, meteorology
- **NASA Earth Data:** Satellite imagery, environmental data
- **PANGAEA:** Oceanography, paleoceanography, marine data
- **ESA CCI:** Climate data records from ESA satellites
- **SEDAC:** Socioeconomic data for Earth sciences

**Astronomy & Astrophysics:**
- **MAST:** Multi-mission archive (HST, Kepler, etc.)
- **SDSS:** Sloan Digital Sky Survey data
- **ESO Archive:** European Southern Observatory
- **Gaia Archive:** ESA Gaia spacecraft data

**Social Sciences:**
- **ICPSR:** Inter-university Consortium for Political and Social Research
- **UK Data Archive:** Social and economic data
- **GESIS:** German social science data
- **DANS:** Netherlands data repository

**Cross-Cutting:**
- **Mendeley Data:** All disciplines
- **Harvard Dataverse:** Institutional focus
- **UK Research Data Catalogue:** UK research data across disciplines

**Repository Selection Checklist:**

| Criterion | Zenodo | Figshare | Dataverse | Discipline Repo |
|-----------|--------|----------|-----------|------------------|
| Free | ✅ | ✅ limited | ✅ | Usually ✅ |
| DOI | ✅ | ✅ | ✅ | ✅ |
| Preservation | ✅✅ | ✅ | ✅ | ✅✅ |
| Metadata support | ✅ | ✅ | ✅✅ | ✅✅ |
| Discipline-specific | ~Limited | ~Limited | ~Limited | ✅✅ |
| Version control | ✅ | Limited | ✅✅ | Limited |
| Easy to use | ✅ | ✅✅ | ✅ | Varies |

**Multi-Repository Strategy:**

**Recommended approach:**
1. **Primary:** Discipline-specific repository if available
2. **Secondary:** General repository (Zenodo or Figshare) as backup
3. **Institutional:** Deposit in institutional repository
4. **Archive:** Software Heritage or Zenodo for permanent preservation

**Example Strategy:**

A genomics researcher with transcriptomics data:
1. **Primary:** Gene Expression Omnibus (GEO)
2. **Secondary:** Zenodo backup
3. **Institutional:** University data repository
4. **Archive:** Software Heritage for code

#### 4.3 Data Accessibility Lifecycle

**Phase 1: Preparation (Before Submission)**

**Tasks:**
- Finalize data cleaning and QC
- Create comprehensive documentation
- Add metadata
- Select license
- Choose repository
- De-identify if needed
- Test access workflows

**Timeline:** 2-4 weeks

**Phase 2: Submission**

**Step-by-step:**

1. **Create account** in chosen repository
2. **Prepare upload**
   - Organize files in logical structure
   - Include all documentation
   - Check file formats
3. **Upload dataset**
   - Follows repository's upload process
   - May be immediate or queued for review
4. **Add metadata**
   - Title, description, creators
   - Keywords, subject classifications
   - Method description
   - Funding information
5. **Set access level**
   - Public (immediate or embargoed)
   - Restricted (requires approval)
   - Private (for now)
6. **Assign license**
   - CC0, CC BY, or other
   - Clear rights statement
7. **Review and submit**
   - Verify all information correct
   - Preview public page
   - Submit for publication

**Phase 3: Publication**

**After submission:**
- Repository assigns DOI
- Creates public landing page
- Indexes in search engines
- Makes available for discovery
- May include mandatory embargo period

**Timeline:** Immediate to 24 hours usually

**Phase 4: Maintenance (Post-Publication)**

**Ongoing responsibilities:**

**Monitoring:**
- Track downloads and citations
- Monitor for reported issues
- Check for broken links
- Verify file integrity

**Updates:**
- Bug fixes: Resubmit corrected version
- New data: Upload as new dataset or new version
- Documentation updates: Revise metadata

**User Support:**
- Respond to questions about data
- Provide clarifications
- Fix metadata errors

**Phase 5: Archival and Preservation**

**Long-term stewardship:**

**Repository responsibilities:**
- Maintain digital integrity
- Monitor for technological obsolescence
- Migrate formats as needed
- Ensure availability
- Handle institution changes

**Your responsibilities (PI):**
- Keep contact information current
- Update when you move institutions
- Maintain institutional relationships
- Support continued access

**Lifecycle Diagram:**

```
Data Sharing Lifecycle

PREPARATION    SUBMISSION    PUBLICATION    MAINTENANCE    ARCHIVAL
(2-4 weeks)    (2-4 weeks)   (days)         (ongoing)      (years+)

├─ Clean data   ├─ Create      ├─ Assign DOI  ├─ Answer       ├─ Verify
├─ Document     │   account    ├─ Index in    │   questions    │   integrity
├─ Add          ├─ Upload      │   search     ├─ Monitor      ├─ Monitor
│  metadata     ├─ Add         ├─ Public      │   usage        │   format
├─ Select       │  metadata    │   page       ├─ Fix issues   │   obsolescence
│  license      ├─ Set access  │   created    └─ Update if    └─ Ensure
├─ Choose       ├─ Choose      └─ Available     needed        longevity
│  repository   │  license        for
├─ De-identify  └─ Submit      discovery
└─ Test access
```

#### 4.4 Making Data Reusable

**Beyond Just Uploading: Enabling Reuse**

**Essential Elements:**

**1. Comprehensive README**

Data need context to be useful:

```markdown
# Dataset Title: Global Tree Species Distribution 1900-2023

## Quick Description
This dataset contains observations of tree species occurrence and abundance 
from forest surveys across 85 countries over 123 years, containing 2.3 million 
occurrence records.

## How Was This Data Created?
- Method: Forest surveys by trained field crews
- Frequency: Annual surveys in most locations
- Protocol: ISO/IEC standardized protocol
- Quality: Field verification, laboratory confirmation of identification

## What Can I Do With This Data?
- Analyze trends in biodiversity
- Validate climate-vegetation models
- Assess impacts of climate change on forest composition
- Train distribution models
- Calculate diversity indices

## Important Limitations
- Sampling bias toward accessible areas
- Some regions sparsely sampled
- Species identification evolving (taxonomy changed in 1995)
- Earlier records may have lower accuracy

## Citing This Dataset
Please cite as: Brown et al. (2024). Global Tree Species Distribution. 
Zenodo. https://doi.org/10.5281/zenodo.XXXXX
```

**2. Data Dictionary / Codebook**

Complete description of every field:

```markdown
# Data Dictionary

## File: tree_observations.csv

### occurrence_id (TEXT, Unique identifier)
- Format: ISO 3166-1 alpha-2 country code + year + record number
- Example: "US_1995_000001"
- Use: Primary key, unique identifier for each observation

### scientific_name (TEXT, Species identifier)
- Format: Binomial nomenclature (Genus species)
- Example: "Quercus robur"
- Validation: Cross-checked against Tropicos and IPNI
- Unknown: "NA" for unidentified specimens

### survey_date (DATE, Observation date)
- Format: YYYY-MM-DD
- Range: 1900-01-01 to 2023-12-31
- Precision: Daily
- Missing: 0.3% pre-1950 records lack exact dates (recorded as 1950-06-15)

### latitude (NUMERIC, Location latitude)
- Format: Decimal degrees, WGS84
- Range: -90 to 90
- Precision: 0.001 degrees (~100m)
- Missing: -9999
- Accuracy: ±100m typical

### longitude (NUMERIC, Location longitude)
- Format: Decimal degrees, WGS84
- Range: -180 to 180
- Precision: 0.001 degrees (~100m)
- Missing: -9999
- Accuracy: ±100m typical

### abundance (INTEGER, Number of individuals)
- Format: Count of individuals
- Range: 1 to 100,000
- Units: Individual trees
- Missing: -9999 (when not quantified)
- Notes: Pre-1980 may be categorical (rare, common, abundant)
```

**3. Methodology Documentation**

```markdown
# Data Collection Methods

## Survey Design
- Stratified random sampling
- 50m × 50m plots in ~1.6 hectare area
- 10 plots per site minimum

## Identification
- Field identification by trained botanists
- Specimen collection for uncertain identifications
- Laboratory confirmation using:
  - Morphological characteristics
  - DNA barcoding (ITS2) since 2010

## Quality Control
- Double-blind verification of 5% of records
- Cross-checking species names against Tropicos
- Outlier detection for abundance values
- Consistency checks across visits to same location

## Data Processing
1. Field data entered into mobile app
2. Automated validation checks
3. Manual review of flagged records
4. Standardization of species names
5. Removal of duplicates
6. Assignment of quality scores (1-5)
```

**4. Analysis Examples**

Provide code showing common analyses:

```python
# Example: Load and visualize tree data
import pandas as pd
import matplotlib.pyplot as plt

# Load data
df = pd.read_csv('tree_observations.csv')

# Filter to recent observations
recent = df[df['survey_date'] >= '2010-01-01']

# Count species richness per location
species_richness = recent.groupby(['latitude', 'longitude'])['scientific_name'].nunique()

# Plot
scatter = plt.scatter(df['longitude'], df['latitude'], 
                     c=species_richness, cmap='viridis')
plt.colorbar(scatter, label='Species Richness')
plt.xlabel('Longitude')
plt.ylabel('Latitude')
plt.title('Tree Species Richness by Location (2010-2023)')
plt.show()
```

**5. Quality/Limitations Documentation**

```markdown
# Data Quality and Limitations

## Completeness
- Overall: 99.7% of expected fields present
- Geographic coverage: 98% of terrestrial surface
- Temporal coverage: 1900-2023, complete

## Accuracy
- Species identification:
  - Post-1980 with DNA confirmation: >99% accuracy
  - 1950-1980 field identification: ~95% accuracy
  - Pre-1950: ~85% accuracy (morphological only)
- Location: ±100m typical (±500m pre-1950)
- Abundance: ±10% for quantified plots

## Known Biases
- Geographic: More sampling in developed countries
- Temporal: Increased sampling in recent decades
- Species: Larger trees more likely to be identified
- Seasonal: Most sampling June-September

## Recommendations for Use
- Weight by quality score for meta-analyses
- Account for uneven sampling when comparing regions
- For pre-1950 data, consider sensitivity analyses
- Verify species identification for critical analyses
```

#### 4.5 Roles in Data Sharing

**Who Needs to Be Involved:**

**Principal Investigator (PI) / Research Lead**
- Makes final decision on sharing
- Ensures compliance with funder requirements
- Signs off on data management plan
- Takes responsibility for data quality

**Data Manager / Data Steward**
- Implements data management plan
- Ensures quality and standards
- Prepares data for sharing
- Manages repository interactions

**Institutional Data Support**
- Data librarian: Advises on repositories and best practices
- IT department: Ensures security and storage
- Legal/compliance: Reviews licensing and restrictions
- Grant administrator: Ensures funder requirements met

**Repository Staff**
- Curators: Review and approve submissions
- Archivists: Ensure long-term preservation
- Technical staff: Maintain systems and access

**Collaborators/Team Members**
- Contribute to metadata documentation
- Test data accessibility
- Provide feedback on reusability

#### Summary

Successfully sharing data requires:
1. **Evaluation:** Determining if and how data can be shared
2. **Repository Selection:** Choosing appropriate platform(s)
3. **Preparation:** Comprehensive documentation and organization
4. **Publication:** Formal submission with metadata
5. **Maintenance:** Ongoing support and updates
6. **Archival:** Long-term preservation
7. **Collaboration:** Involving necessary stakeholders

Well-shared data maximizes research impact and enables discoveries by enabling others to reuse, validate, and build upon your work.

:::{admonition} Activities for Lesson 4
:class: activity

Complete at least two of the following activities to practice sharing data:

**Activity 4.1: Evaluate Data Shareability**
For a dataset you work with (or hypothetical), create a shareability assessment:
- Is this sensitive data (health, location, personal)?
- What is the consent/IRB status for sharing?
- Are there intellectual property or patent considerations?
- Are there security or safety concerns?
- Could de-identification maintain research utility?

Develop a sharing plan addressing:
- What data components can be openly shared?
- What components require restricted access?
- What timeline for releasing each component?
- How will restricted access be managed?

Write a 300-400 word assessment and plan.

**Activity 4.2: Select Repositories and Create Submission Plan**
For your dataset, identify 2-3 appropriate repositories. For each, document:
- Repository name and discipline/scope
- Storage capacity and requirements
- Metadata standards used
- DOI/persistent identifier support
- Long-term preservation commitment
- Associated costs (if any)

Create a table comparing repositories and explain which you would choose and why.

**Activity 4.3: Plan Data Lifecycle and Maintenance**
Create a timeline and plan for your shared dataset:
- **Short-term (first year):** Maintenance, error corrections, documentation updates
- **Medium-term (2-5 years):** Version updates, additional analyses, derived datasets
- **Long-term (5+ years):** Archival strategy, format preservation, access maintenance

Identify who will maintain the dataset, how long it will be actively maintained, and archival plans.

**Deliverable:** Your choice of output from activities above (2-3 pages total).
:::

### Lesson 5: From Theory to Practice

#### Overview
In this lesson, you will get some practice writing a data management plan. You will then learn how you can get involved in open data communities. You will also learn about resources you can start to use and training you can take to start your journey with open data.

#### 5.1 Writing an Effective Data Management Plan

**Steps to Write a Strong DMP:**

**Step 1: Gather Information**

Before writing, collect details about your project:
- What data will you generate/use?
- How much data (size and number of files)?
- What are the variables and measurements?
- Who will generate/collect the data?
- When will data be generated?
- Where will data be stored?
- Who needs access?
- What are the funder requirements?

**Step 2: Use a Template**

**Template Sources:**

**DMPTool** (dmptool.org)
- Free, institution-specific templates
- NSF, NIH, IMLS, DOE templates included
- Guidance for each section
- Public DMPs you can view for examples

**Data Stewardship Wizard** (ds-wizard.org)
- Interactive question-based approach
- Generates compliant DMPs
- Knowledge base guidance

**Funder-Specific Templates:**
- **NSF:** Section on "Data Management and Sharing Plan"
- **NIH:** Data Management and Sharing Plan requirement
- **EU:** FAIR data management plans
- **UK Funding Councils:** Data management plan guidance

**Step 3: Write Each Section**

Using our Lesson 3 example template, write:

1. **Data Collection and Generation**
   - What data will be collected?
   - By what methods?
   - How much data?
   - Timeline?

2. **Data and Metadata Standards**
   - Which standards apply?
   - What metadata will be captured?
   - Format standards?

3. **Data Storage and Security**
   - Where will data be stored?
   - Who has access?
   - How is it backed up?
   - How is security ensured?

4. **Access and Sharing**
   - Who can access data?
   - When will data be made available?
   - Where will data be shared (repository)?
   - Are there restrictions?

5. **Long-term Preservation**
   - How long will data be retained?
   - Who is responsible for archiving?
   - How will format changes be handled?
   - Budget for preservation?

**Step 4: Get Feedback**

- Share with advisor/PI
- Get departmental review
- Consult data librarian
- Check institutional compliance

**Step 5: Revise and Finalize**

- Address feedback
- Ensure clarity
- Verify compliance with funder
- Submit with proposal

**Step 6: Implement**

- Follow your own DMP
- Update as project evolves
- Share with team
- Train team on procedures

**Common DMP Mistakes to Avoid:**

❌ **"We will follow best practices"**
- Too vague
- Specify WHICH practices

❌ **"All data will be shared immediately"**
- May conflict with publication timeline
- Specify when (e.g., "upon publication")

❌ **"Data will be archived in a repository"**
- Which repository?
- Zenodo? Dataverse? Discipline-specific?

❌ **Ignoring metadata requirements**
- Be specific: What metadata will be captured?
- What standards will be used?

❌ **No mention of budget**
- Data management costs money
- Include costs for storage, archiving, support

**Example DMP Excerpt (Filled In):**

```markdown
# Data Management Plan: Global Microbiome Survey

## Data Collection
We will generate 16S rRNA amplicon sequencing data from 50,000 soil samples 
collected globally. Each sample will produce ~100MB of raw sequencing data 
(FASTQ format), plus processed data (FASTA sequences, abundance tables). 
Total volume: ~5TB raw + 500GB processed.

## Standards
Data will follow Earth Microbiome Project (EMP) standards:
- Metadata: MIAPPE standard in JSON format
- File formats: FASTQ (raw), FASTA (processed), CSV (abundance tables)
- Taxonomy: Silva database v138

## Storage
- Primary: Lab server (replicated, backed up daily)
- Timeline: During project + 3 years post-completion
- Archives: NCBI SRA (raw sequences), Zenodo (processed data)

## Access and Sharing
- Timeline: Raw sequences released upon publication (Month 24)
- Processed data: Released same time
- Repository: NCBI SRA + Zenodo
- DOI: Will obtain DOI for citable release
- License: CC0 (public domain, no restrictions)

## Long-term
- NCBI SRA and Zenodo provide long-term archival
- No active maintenance required after archival
- 7-year minimum retention per NIH
```

#### 5.2 Open Data Communities and Engagement

**Why Join Communities?**

- **Learn:** Best practices, tools, workflows
- **Connect:** Meet others working on similar data
- **Support:** Get help with challenges
- **Contribute:** Help others, improve field standards
- **Advocate:** Advance open data principles

**Types of Open Data Communities:**

**1. Disciplinary Communities**

These focus on data sharing within specific scientific fields:

**Life Sciences:**
- **Global Biodiversity Information Facility (GBIF):** Biodiversity occurrence data
- **Dryad:** Data repository for life sciences publications
- **Bioconductor:** Computational biology data and tools
- **Microbiome Forums:** Open microbiome data discussion

**Earth & Environmental Sciences:**
- **DataOne:** Distributed data repository network
- **Pangaea:** Oceanography and paleoceanography data
- **FAIR Climate:** Fair data in climate science
- **ESIP (Earth Science Information Partners):** Earth science data standards

**Social Sciences:**
- **ICPSR:** Hosts social science data discussions
- **CESSDA:** European Social Science Data Archive
- **RECODE:** Research Ethics and Compliance in Data Exchange

**2. Infrastructure Communities**

These support data management tools and systems:

- **DataCite:** DOI assignment and citation for data
- **FORCE11:** Scholarly communication innovation
- **CODATA:** Committee on Data for Science and Technology
- **RDA (Research Data Alliance):** Cross-disciplinary data standards

**3. Open Science Communities**

- **The Carpentries:** Teaching data management and computing skills
- **Center for Open Science:** Open science practices and tools
- **Software/Data Carpentry:** Community teaching labs
- **Open Science Foundation:** Supporting open science initiatives

**4. Domain-Specific Organizations**

- **DataONE:** Environmental data network
- **ELIXIR:** Life sciences data infrastructure
- **XSEDE:** High-performance computing and data resources
- **EUDAT:** European data infrastructure

**How to Get Involved:**

**Level 1: Participant (Minimal Commitment)**
- Attend webinars and workshops
- Join mailing lists
- Participate in forums (read and occasionally post)
- Follow social media accounts
- Use community tools and standards

**Level 2: Active Member (Regular Engagement)**
- Attend regular meetings or conferences
- Answer others' questions in forums
- Contribute to working groups
- Submit data to community repositories
- Provide feedback on standards

**Level 3: Leader (High Commitment)**
- Serve on committees
- Lead working groups
- Organize local meetings or workshops
- Contribute to standards development
- Mentor new members

**Example Community Engagement:**

A researcher gets involved in open data communities:

**Month 1-2: Discovery**
- Finds GBIF (biodiversity) and Dryad (data sharing)
- Joins mailing lists
- Watches introductory webinars

**Month 3-6: Participation**
- Shares first dataset on Dryad
- Participates in online Q&A forum
- Attends virtual workshops

**Month 6-12: Contribution**
- Helps other researchers upload data
- Comments on proposed standards
- Presents at local data management seminar

**Year 2+: Leadership**
- Serves on Dryad advisory committee
- Mentors junior researchers on data sharing
- Co-leads workshop on biodiversity data standards

#### 5.3 Resources for Learning More

**Books and Guides:**

1. **"The Turing Way"** (the-turing-way.netlify.app)
   - Free, open-source handbook
   - Covers reproducible research, open science, collaboration
   - Community-driven, continuously updated

2. **"The Data Book: A Guide to Understanding the Digital Transformation of Everything"** by Andy Crestodina
   - Practical guide to data collection and use

3. **"Data Mesh"** by Zhamak Dehghani
   - Architecture for data infrastructure
   - Relevant for large research institutions

4. **"Good Enough Practices in Scientific Computing"**
   - Carpentries guide to practical data management

**Online Courses:**

1. **Data Carpentry** (datacarpentry.org)
   - Free, open-source lessons
   - Data organization, cleaning, analysis
   - Self-paced or instructor-led workshops

2. **Coursera: Data Management and Sharing** (various institutions)
   - Johns Hopkins University offerings
   - Data science specialization
   - Free to audit

3. **Udemy: Data Management Courses**
   - Various topics and levels
   - Often affordable

4. **FASTERDATA (NERSC)**: fasterdata.lbl.gov
   - HPC data transfer tutorials
   - Free online training

5. **MANTRA (University of Edinburgh):** mantra.edina.ac.uk
   - Research Data Management Training
   - Open online course

**Interactive Tools & Platforms:**

1. **DMPTool** (dmptool.org)
   - Create DMPs with institutional templates
   - View public examples
   - Integrate with institutional systems

2. **Data Stewardship Wizard** (ds-wizard.org)
   - Interactive DMP creation
   - Question-guided approach

3. **FAIRsharing** (fairsharing.org)
   - Standards, databases, policies
   - Search by discipline
   - Compare repositories

4. **Zenodo** (zenodo.org)
   - Create free account and explore
   - Practice uploading a small dataset
   - Learn by doing

5. **Figshare** (figshare.com)
   - User-friendly data sharing
   - No specialized knowledge required
   - Good for learning

**Research Articles & Papers:**

1. **FAIR Data Principles**
   - Wilkinson et al. (2016). "The FAIR Guiding Principles for scientific data management and stewardship." Scientific Data, 3, 160018.

2. **Data Management for Open Science**
   - Various papers in Science, Nature, PLOS ONE
   - Search: "open data management" or "FAIR principles"

3. **Journal: Scientific Data**
   - Publishes data papers
   - Good examples of data documentation

**Websites and Organizations:**

1. **The Open Data Handbook** (opendatahandbook.org)
   - Comprehensive guide to open data
   - Multiple language translations
   - Practical guidance

2. **Open Access Button** (openaccessbutton.org)
   - Search for open data and papers
   - See what's available

3. **Registry of Open Access Repositories (ROAR)**
   - Find appropriate repositories
   - Quality assessment information

4. **DataCite Blog** (datacite.org/blog)
   - Latest on data citation and DOIs
   - Case studies and best practices

5. **Force11 Scholarly Kitchen** (scholarlykitchen.sspnet.org)
   - Commentary on scholarly communication
   - Data publishing discussions

**Institutional Resources:**

- **University Data Librarian**
  - Often free consultation available
  - Tailored to your institution
  - Knows funder requirements

- **Library Research Support Services**
  - Workshops on data management
  - Help with repositories and archiving
  - Often free

- **IT Data Services**
  - Storage and backup solutions
  - Large data handling advice

- **Graduate Student Training**
  - Data management workshops
  - Often included in graduate programs
  - May be available for postdocs

**Community Events:**

1. **Research Data Management Forum** (various locations)
   - Local and regional meetings
   - Networking opportunities

2. **Conferences with Data Tracks**
   - Most scientific conferences now include data sessions
   - Look for data-specific workshops

3. **FORCE11 Annual Conference**
   - Scholarly communication innovation
   - Includes data management sessions

4. **RDA Plenary Meetings**
   - Twice yearly, online and in-person
   - Working groups and community meetings
   - Free to attend

5. **DataCite Member Events**
   - DOI implementation and data citation
   - Training sessions

**Professional Development:**

1. **Research Data Management Certification**
   - University of Edinburgh
   - Self-paced online course
   - Recognized credential

2. **Data Stewardship Certification**
   - Various institutions offering
   - Increasingly important credential

3. **Software/Data Carpentry Instructor Training**
   - Train-the-trainer program
   - Become certified to teach data skills
   - Community of instructors

#### 5.4 Practical Exercises

**Exercise 1: Write Your First DMP**

For a real or hypothetical project:

1. Use DMPTool (dmptool.org)
2. Select your institution and funder
3. Answer all sections
4. Aim for 2-3 pages
5. Have advisor review

**Deliverable:** Completed DMP document

**Exercise 2: Explore Repositories**

1. Visit Zenodo, Figshare, and one discipline-specific repository
2. Search for datasets in your field
3. Read READMEs and documentation
4. Note: What information was helpful? What was missing?
5. Write a 1-page reflection

**Deliverable:** Reflection on repository quality

**Exercise 3: Assess a Dataset**

Find a published dataset:

1. Check: Is it FAIR?
   - Findable: Can you find it? Is there metadata?
   - Accessible: Can you download/access it?
   - Interoperable: Is the format standard? Well documented?
   - Reusable: Is there a license? Is it documented?

2. Write up assessment (1-2 pages)
3. Suggest improvements

**Deliverable:** Dataset assessment

**Exercise 4: Create a Data Dictionary**

For a dataset you have access to:

1. Choose a CSV or spreadsheet file
2. Document every column
   - Name, description, type, units, range, missing codes
3. Create DATA_DICTIONARY.csv
4. Include examples

**Deliverable:** Complete data dictionary

**Exercise 5: Prepare Data for Sharing**

Take a dataset and:

1. Clean it thoroughly
2. Create README.md
3. Write DATA_DICTIONARY.csv
4. Add METHODS.md
5. Choose and add LICENSE file
6. Organize in folder with all documentation
7. Share folder link with colleague for feedback

**Deliverable:** Complete shareable dataset package

**Exercise 6: Share Data Online**

1. Choose a small dataset
2. Create free Zenodo account
3. Upload dataset
4. Add all metadata
5. Get DOI
6. Share link with others
7. Track downloads

**Deliverable:** Published dataset with DOI

#### 5.5 Implementation Roadmap

**For the Next 3 Months:**

**Week 1-2: Learn**
- Complete one Data Carpentry lesson
- Watch 2-3 webinars on data management
- Read your funder's data sharing requirements

**Week 3-4: Assess**
- Evaluate your current data practices
- Identify gaps
- Review your institution's data services

**Week 5-8: Plan**
- Write DMP for current/next project
- Get feedback from advisor/librarian
- Identify repository for your data

**Week 9-12: Implement**
- Create README and documentation
- Organize files
- Prepare first dataset for sharing

**For the Next Year:**

**Quarters 1-2:** Foundation
- Implement DMP in current project
- Share first dataset
- Get DOI

**Quarters 3-4:** Advanced
- Automate data management workflows
- Contribute to community discussions
- Mentor others on data sharing
- Attend conference or workshop

**For Long-Term Success:**

- Make open data practices standard in your lab
- Integrate data management training into grad student onboarding
- Advocate for institutional data support
- Participate in professional communities
- Keep learning about evolving standards

#### Summary

Moving from theory to practice involves:

1. **Planning:** Writing effective data management plans
2. **Learning:** Using available resources and training
3. **Engaging:** Connecting with open data communities
4. **Implementing:** Putting practices into action
5. **Evolving:** Continuously improving as practices change

Open data is not just about compliance with funder requirements—it's about advancing science by making data available, discoverable, and reusable. By developing strong data management practices and engaging with communities, you contribute to a more transparent, reproducible, and collaborative scientific enterprise.

Remember: You don't need to do everything at once. Start small, learn as you go, and build sustainable practices that work for your research. The open data community is welcoming and supportive—don't hesitate to ask for help or share your experiences with others.

:::{admonition} Activities for Lesson 5
:class: activity

Complete at least one of the following activities to implement open data practices:

**Activity 5.1: Write a Complete Data Management Plan**
Using insights from previous activities, write a comprehensive DMP for a real or planned research project. Include:
- Executive summary
- Data description (types, volume, time period, geographic scope)
- FAIR principles implementation strategy
- Data management practices (formats, documentation, version control)
- Repository and archival strategy
- Access and sharing policies (with justification)
- Budget and resources needed
- Timeline for key milestones

Aim for 1500-2000 words. Use a template from your funder or discipline.

**Activity 5.2: Connect with Open Data Communities**
Identify and engage with open data communities relevant to your field:
- Join a disciplinary data community or working group
- Attend (or watch recordings of) a webinar on open data in your field
- Follow an open data organization on social media or subscribe to their newsletter
- Contribute to a community discussion about open data challenges

Document what you learned and how it will inform your open data practice. Write 200-300 words reflecting on the value of community engagement.

**Activity 5.3: Create Your 12-Month Open Data Action Plan**
Develop a concrete implementation plan:
- **Month 1-2:** Assess current practices, identify gaps, choose first project
- **Month 3-5:** Implement foundational practices (DMPs, metadata documentation)
- **Month 6-8:** Prepare first dataset for sharing (licensing, format conversion)
- **Month 9-10:** Submit to repository and obtain DOI
- **Month 11-12:** Document lessons learned, identify improvements for next phase

Include specific actions, timelines, resources needed, and success metrics. Aim for 1-2 pages.

**Deliverable:** Your choice of output from activities above (2-3 pages total).
:::

## Additional Resources

In addition to the TOPS module training, the community resources below are excellent information sources about Open Data.
- [NASA's Transform to Open Science](https://nasa.github.io/Open-Science-101-Book/) github landing page for TOPS
- [NASA SMD's Open-Source Science Guidance](https://science.nasa.gov/science-red/s3fs-public/atoms/files/SMD%20Open-Source%20Science%20Guidance%20v1%2020221208.pdf)
- [Repository of Federal Enterprise Data Resources](https://resources.data.gov/)
- [The Open Data Handbook](http://opendatahandbook.org/guide/en/)
- GODAN [MOOC](https://aims.gitbook.io/open-data-mooc/) on Open Data Management in Agriculture and Nutrition
- [Carpentries Data Management](https://carpentries-incubator.github.io/good-enough-practices/02-data_management/index.html) for Scientific Computing
- Great open data in Africa farming [MOOC](https://aims.gitbook.io/farm-data-mooc/)
- FAIRsharing.org; [The FAIR Principles](https://fairsharing.org/FAIRsharing.WWI10U) 
- Reproducible Research and Data Analysis. [FOSTER](https://github.com/Open-Science-Training-Handbook/Open-Science-Training-Handbook_EN/blob/master/02OpenScienceBasics/04ReproducibleResearchAndDataAnalysis.md) 
- Some guides on publishing data are available [here](https://www.cessda.eu/Training/Training-Resources/Library/Data-Management-Expert-Guide/6.-Archive-Publish/Data-publishing-routes) and [here](https://www.openaire.eu/opendatapilot-repository-guide)
- An example of tagging and sharing data from Harvard University, [DataTags](https://privacytools.seas.harvard.edu/datatags)
