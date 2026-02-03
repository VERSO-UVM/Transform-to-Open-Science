# Module 2: Open Tools and Resources

## Introduction

Open science requires both conceptual understanding and practical tools. This module bridges theory and practice by introducing the tools and resources used across open science workflows. The "Use, Make, Share" framework provides a practical model for applying open science principles throughout research.

## Learning Objectives

After completing this module, you should be able to:
- **Define** foundational open science concepts including research products, the Use-Make-Share framework, and data/software management plans
- **List and explain** resources for discovering, assessing, and reusing research products
- **Develop** a strategy for data management using FAIR principles and data management plans
- **Design** approaches for open software development including version control and documentation
- **Identify** tools and platforms for sharing research outputs and ensuring reproducibility

## Overview of 5 Modules

This module covers essential tools and concepts:
- [Lesson 1: Foundational Open Science Concepts](#lesson-1-foundational-open-science-concepts)
- [Lesson 2: Universal Open Science Tools](#lesson-2-universal-open-science-tools)
- [Lesson 3: Tools for Open Data](#lesson-3-tools-for-open-data)
- [Lesson 4: Tools for Open Code](#lesson-4-tools-for-open-code)
- [Lesson 5: Tools for Sharing Research Results](#lesson-5-tools-for-sharing-research-results)

---

## Lesson 1: Foundational Open Science Concepts

### Overview
In this lesson, you review core concepts that underpin open science practice. You explore research products, understand the Use-Make-Share framework that structures this entire curriculum, learn about management plans, and examine real-world examples of open science in action.

### 1.1 What is Open Science?

**Definition:** Open science is the principle and practice of making the products and processes of research available to all members of an extended, diverse global community while respecting diverse cultures, maintaining security and privacy, fostering collaborations, enabling reproducibility, and advancing equity.

**Core Elements:**
1. **Accessible:** Research freely available without paywalls
2. **Transparent:** Methods, data, and code shared openly
3. **Collaborative:** Researchers work together and build on each other's work
4. **Reproducible:** Others can verify and reproduce findings
5. **Equitable:** Global access regardless of resources or location

**Why Open Science Matters:**
- **Reproducibility:** Science depends on verification
- **Efficiency:** Avoids duplicate effort and accelerates discovery
- **Quality:** Peer scrutiny improves research quality
- **Impact:** Wider dissemination increases citations and influence
- **Equity:** Enables researchers globally to participate

### 1.2 Research Products and Outputs

**What are Research Products?**

Any deliverable from research including:
- **Primary research:** Original studies, experiments
- **Data:** Measurements, observations, datasets
- **Software:** Code, algorithms, tools
- **Publications:** Articles, preprints, books
- **Workflows:** Methods, protocols, procedures
- **Educational materials:** Tutorials, courses, training
- **Supplementary materials:** Figures, tables, analysis code

**Making Products Citable:**
- Assign DOI (Digital Object Identifier)
- Include metadata
- Register in repositories
- Enable clear attribution

### 1.3 The Use, Make, Share Framework

**Overview:** The Use-Make-Share framework provides a practical model for implementing open science.

**USE: Building on Open Research**
- Search and discover existing research
- Assess quality and appropriateness
- Understand licensing and reuse rights
- Build on others' work responsibly

**MAKE: Conducting Open Research**
- Plan research with data/software management plans
- Document methods and procedures
- Design reproducible workflows
- Conduct transparent processes
- Prepare outputs for sharing

**SHARE: Disseminating Research**
- Prepare materials for publication
- Select appropriate venues and platforms
- Deposit in repositories
- Enable discovery through metadata
- Engage with research community

### 1.4 Data and Software Management Plans

**Data Management Plan (DMP):**
- Strategic document for data handling
- Required by most major funders
- Key Components: Data types, standards, storage, access, preservation, budget

**Software Management Plan (SMP):**
- Strategic document for software development
- Describes development approach, testing, documentation, licensing, sharing, maintenance
- Increasingly required by funders

### 1.5 Real-World Example: Open Science Impact

**COVID-19 Research Response:**
- **USE:** Downloaded epidemiological models and datasets
- **MAKE:** Created new analyses with transparent methods
- **SHARE:** Posted preprints, shared code/data, published open access
- **Result:** Vaccine development accelerated, global collaboration enabled, public trust built

### Summary

Foundational concepts guide open science:
- **Open science** is accessible, transparent, reproducible, collaborative, and equitable
- **Research products** include data, software, publications, and methods
- **Use-Make-Share** provides practical framework for implementation
- **Management plans** formalize commitment to open practices
- **Real examples** demonstrate feasibility and impact

---

## Lesson 2: Universal Open Science Tools

### Overview
In this lesson, you explore tools that are essential across all open science domains. These tools enable discoverability, provide persistent access, ensure proper attribution, and support management planning.

### 2.1 Persistent Identifiers: The Foundation

**Why Persistent Identifiers Matter:**

URLs break. Repositories move. Storage locations change. Persistent identifiers ensure that research remains findable and citable indefinitely.

**Common Persistent Identifiers:**

**DOI (Digital Object Identifier)**
- Most common in research
- Format: 10.5281/zenodo.1234567
- Managed by CrossRef, DataCite
- Works across disciplines

**ORCID (Researcher Identifier)**
- Unique identifier for YOU
- Format: 0000-0002-1825-0097
- Connects all your research
- Free to obtain (orcid.org)

### 2.2 Repositories and Discovery

**Types of Repositories:**
- General-purpose (Zenodo, OSF, Figshare)
- Discipline-specific (bioRxiv, arXiv, SSRN)
- Institutional repositories
- Data repositories (DataCite, re3data)

**Discovery Tools:**
- Google Scholar
- OpenAIRE
- SHARE
- Unpaywall

### 2.3 Metadata and Documentation

**Metadata Standards:**
- Dublin Core
- DATACITE
- MIAOU
- MIAOE

**Documentation Importance:**
- Clear descriptions improve discoverability
- Enable proper reuse
- Support reproducibility

### 2.4 Licenses and Attribution

**Common Licenses:**
- Creative Commons (CC BY, CC0, CC BY-SA)
- MIT License
- GPL
- Apache 2.0

**Why Licenses Matter:**
- Clarify reuse rights
- Protect contributors
- Enable clear attribution

### 2.5 Research Impact Metrics

**Citation Metrics:**
- h-index
- Citation counts
- Journal Impact Factor

**Alternative Metrics:**
- Altmetric scores
- Download counts
- Social media mentions
- Policy citations

### Summary

Universal tools enable open science:
- **Persistent identifiers** (DOI, ORCID) ensure permanent access
- **Repositories** provide discoverable storage
- **Metadata standards** enable understanding
- **Licenses** clarify reuse rights
- **Impact metrics** measure contribution

---

## Lesson 3: Tools for Open Data

### Overview
In this lesson, you explore tools and practices for organizing, documenting, and sharing research data using FAIR principles.

### 3.1 FAIR Principles Applied to Tools

**Findable:** 
- Repositories with metadata
- DOI assignment
- Clear descriptions

**Accessible:** 
- Open repositories
- No paywalls
- Free downloads

**Interoperable:** 
- Standard data formats (CSV, JSON, NetCDF)
- Common standards
- Cross-platform compatibility

**Reusable:** 
- Comprehensive documentation
- Clear licenses
- Detailed metadata

### 3.2 Data Formats and Standards

**Tabular Data:**
- CSV (Comma-separated values)
- Excel/XLSX
- Parquet
- JSON

**Scientific Data:**
- NetCDF (Climate, meteorology)
- HDF5 (Large scientific datasets)
- GeoTIFF (Geospatial data)
- FITS (Astronomical data)

**Genomic Data:**
- FASTQ (Sequence reads)
- BAM (Aligned sequences)
- VCF (Variant calls)
- GFF/GTF (Annotations)

### 3.3 Data Management Tools

**Planning Tools:**
- **DMPTool:** Writing and managing DMPs
- **Data Stewardship Wizard:** European DMP support
- **DMPonline:** UK DMP tool

**Organization Tools:**
- **Open Science Framework:** Project management
- **Git/GitHub:** Version control for data
- **Data packages:** Frictionless data standards

**Repository Tools:**
- **Zenodo:** Multidisciplinary
- **Dataverse:** Data repository
- **OSF Storage:** Built-in storage

### 3.4 Data Documentation

**Documentation Essentials:**
- README files
- Data dictionaries
- Metadata records
- Codebooks

**Tools:**
- Jupyter Notebooks
- Markdown files
- Data documentation generators

### 3.5 Data Preservation and Access

**Long-term Preservation:**
- Digital preservation standards
- Format migration planning
- Backup strategies

**Access Control:**
- Open access
- Restricted access with justification
- Embargo periods

### Summary

Data tools enable FAIR sharing:
- **Formats:** Standard formats for discoverability
- **Organization:** DMPTools and version control
- **Documentation:** Metadata and codebooks
- **Repositories:** Discipline-appropriate storage
- **Access:** Free and open for reuse

---

## Lesson 4: Tools for Open Code

### Overview
In this lesson, you explore tools for developing, testing, documenting, and sharing research software.

### 4.1 Version Control Systems

**Git Basics:**
- Distributed version control
- Track changes to files
- Collaborate safely
- Revert to previous versions

**Key Features:**
- Branching and merging
- Commit history
- Collaboration workflows

**Platforms:**
- **GitHub:** Most popular (100M+ repositories)
- **GitLab:** Alternative with self-hosting
- **Bitbucket:** Atlassian ecosystem

### 4.2 Development Environments

**Text Editors:**
- VS Code
- Sublime Text
- Atom
- vim/neovim

**IDEs:**
- PyCharm (Python)
- RStudio (R)
- Jupyter Lab (interactive)
- Visual Studio (C#/.NET)

**Containerization:**
- Docker (containers)
- Singularity (HPC-friendly)
- Conda (environments)

### 4.3 Testing and Quality Assurance

**Testing Frameworks:**
- **Python:** pytest, unittest, nose2
- **R:** testthat, RUnit
- **JavaScript:** Jest, Mocha

**Continuous Integration:**
- GitHub Actions
- Travis CI
- AppVeyor
- CircleCI

**Code Quality Tools:**
- **Python:** Flake8, pylint, Black (formatter)
- **R:** lintr, styler
- **JavaScript:** ESLint, Prettier
- Coverage analysis

### 4.4 Documentation Tools

**Documentation Generators:**
- **Sphinx:** Industry-standard for Python
- **MkDocs:** Markdown-based
- **Quarto:** Multi-language documents

**Hosting:**
- **ReadTheDocs:** Free hosting
- **GitHub Pages:** Built into GitHub
- **GitLab Pages:** Built into GitLab

**Inline Documentation:**
- Docstrings
- Comments
- API documentation
- Jupyter Notebooks

### 4.5 Code Repositories and Registries

**Package Registries:**
- **PyPI:** Python Package Index
- **CRAN:** R packages
- **npm:** JavaScript packages
- **Maven Central:** Java packages

**Code Archival:**
- **Zenodo:** Permanent archival with DOI
- **Figshare:** Easy sharing
- **Software Heritage:** Git repository archival

### 4.6 Code Quality and Performance

**Linting and Formatting:**
- Automated code style checking
- Format enforcement
- Consistency tools

**Performance Profiling:**
- Identify bottlenecks
- Memory profiling
- Optimization tools

### Summary

Code tools enable reproducible software:
- **Version control:** Git and GitHub for collaboration
- **Development:** IDEs and containers for reproducibility
- **Testing:** Frameworks and CI/CD for reliability
- **Documentation:** Generators and notebooks for clarity
- **Quality:** Linters and formatters for consistency

---

## Lesson 5: Tools for Sharing Research Results

### Overview
In this lesson, you explore tools and platforms for sharing, discovering, and evaluating research results.

### 5.1 Project Management and Collaboration

**Collaborative Tools:**
- **Open Science Framework:** OSF.io project management
- **GitHub Projects:** Issue tracking and boards
- **Notion:** All-in-one workspace
- **Slack:** Team communication

**Lab Notebooks:**
- OSF wiki
- GitHub wiki
- Notion databases
- Jupyter Notebooks

### 5.2 Preprint Servers

**Multidisciplinary:**
- **arXiv:** Physics, math, CS (largest)
- **OSF Preprints:** General open science

**Discipline-Specific:**
- **bioRxiv:** Biology (now part of medRxiv)
- **medRxiv:** Medicine and health sciences
- **PsyArXiv:** Psychology
- **EarthArXiv:** Earth sciences
- **SocArXiv:** Social sciences

**Benefits of Preprints:**
- Rapid dissemination (days vs. 6-18 months)
- Establishes priority
- Gets feedback for improvement
- Increases citations

### 5.3 Open Access Publishing

**Finding Open Access Venues:**
- **DOAJ:** Directory of Open Access Journals (20,000+)
- **Open Access Button:** Journal finder
- **Sherpa/RoMEO:** Journal policies
- **Unpaywall:** Free full-text finder

**Publishing Models:**
- **Gold OA:** Immediate open access
- **Green OA:** Self-archive after embargo
- **Diamond/Platinum:** No author fees, no reader fees
- **Hybrid:** Some articles open

### 5.4 Reference Management and Citations

**Reference Management Tools:**
- **Zotero:** Free, open source
- **Mendeley:** Popular with sync
- **Notion:** Database approach
- **Papers:** Modern interface

**Citation Formatters:**
- **Pandoc:** Convert between formats
- **Manubot:** Scholarly writing platform
- **Citation Style Language:** Format standards
- **BibTeX:** LaTeX bibliography system

### 5.5 Reproducibility Support

**Executable Environments:**
- **Jupyter Notebooks:** Python, R, Julia code + narrative
- **RMarkdown:** R + Markdown documents
- **Quarto:** Language-agnostic notebooks

**Containerization:**
- **Docker:** Reproducible environments
- **Singularity:** HPC-friendly containers

**Environment Management:**
- **Conda:** Python/R package management
- **renv/packrat:** R environment isolation
- **Poetry:** Python dependency management

### 5.6 Research Communication

**Social Media:**
- **Twitter/X:** Scholarly communication
- **Mastodon:** Federated alternative
- **Bluesky:** New platform

**Blogs and Websites:**
- Personal blog
- Medium
- GitHub Pages
- Substack

**Video and Multimedia:**
- YouTube
- Podcasts
- Presentation slides
- Infographics

### 5.7 Impact Measurement

**Citation Tools:**
- **Google Scholar:** Citation tracking
- **Altmetric:** Alternative metrics
- **Crossref:** Citation metadata
- **PubMed:** Life sciences focus

**Journal Evaluation:**
- **DOAJ:** OA journal quality
- **COPE:** Publishing ethics
- **ISSN:** Journal identification

### 5.8 Preregistration and Transparency

**Preregistration Platforms:**
- **OSF Registries:** Open science framework
- **AsPredicted:** Quick preregistration
- **ClinicalTrials.gov:** Trial registration

**Benefits:**
- Combat publication bias
- Prevent p-hacking
- Increase trust
- Distinguish confirmatory from exploratory

### Summary

Result-sharing tools maximize impact:
- **Preprints:** Rapid dissemination and priority
- **Open Access:** Permanent free access for all
- **References:** Organize, cite, and manage
- **Communication:** Reach broad audiences
- **Reproducibility:** Enable verification and reuse
- **Impact:** Measure and demonstrate contribution
- **Transparency:** Preregister and document methods

---

## Additional Resources

In addition to the TOPS module training, the community resources below are excellent information sources about open science.

### Data Repositories and Search Tools
- [re3data.org](https://www.re3data.org/) - Registry of data repositories
- [OpenAIRE Find research data sources](https://explore.openaire.eu/search/find/dataproviders)
- [SHARE search tools](https://share.osf.io/sources)
- [DORA - Declaration on Research Assessment](https://sfdora.org/)

### Documentation and Blogs
- [Working efficiently with JupyterLab Notebooks](https://florianwilhelm.info/2018/11/working_efficiently_with_jupyter_lab/) - Florian Wilhelm's blog

### Recommended Papers and Reports
- Candela et al. (2013). Virtual Research Environments: An Overview and a Research Agenda. Data Science Journal. 12, pp.GRDI75–GRDI81.
- [Leiden Manifesto for Research Metrics](http://www.leidenmanifesto.org/)
- Bolick et al. (2017). How open access is crucial to the future of science.
- Clyburne-Sherin (FSCI2017). Advocating for transparency policies - a toolkit for researchers, staff, and librarians.
