# Open Science Tools and Software

## Introduction

Open science tools are digital resources and instruments that support research through data storage, code collaboration, persistent identification, documentation, and community engagement. These tools are essential for implementing open science practices, enabling reproducibility, and facilitating collaboration.

## Module Overview

This module covers the essential tools and platforms used in open science research:
- Lesson 1: Repositories and Data Storage
- Lesson 2: Version Control and Collaboration
- Lesson 3: Persistent Identifiers and Citation
- Lesson 4: Open Science Software Ecosystems
- Lesson 5: Building Your Open Science Toolkit

---

## Lesson 1: Repositories and Data Storage

### Overview
In this lesson, you explore the different types of repositories used to store and preserve research data and software, understand the differences between development repositories and archives, and learn how to select appropriate platforms for your research outputs.

### 1.1 What is a Repository?

A repository is a digital storage system that:
- **Stores** research data, code, or documentation
- **Provides access** to your research outputs
- **Ensures preservation** for long-term access
- **Enables discovery** through search and indexing
- **Manages versions** of files and records

**Core Functions:**
1. **Storage:** Secure, reliable hosting
2. **Access:** Public, restricted, or tiered access
3. **Preservation:** Long-term maintenance and format migration
4. **Metadata:** Description enabling discovery
5. **Persistence:** Assigned identifiers (DOIs) for permanent access

### 1.2 Repository vs. Archive: Key Differences

**Development Repositories**
- **Purpose:** Active collaborative development
- **Version Control:** Full Git/Mercurial/SVN integration
- **History:** Complete change tracking
- **Branching:** Experimental and parallel work
- **Examples:** GitHub, GitLab, Bitbucket
- **Use When:** Actively writing code, multiple developers, rapid iterations

**Archives (Data Preservation)**
- **Purpose:** Long-term preservation of final versions
- **Version Control:** Minimal (snapshot preservation)
- **History:** Limited to deposited versions
- **Immutability:** Final versions cannot be changed
- **Examples:** Zenodo, Figshare, Dataverse
- **Use When:** Publishing final datasets, archiving software releases, preservation required

**Best Practice:** Use both together
```
Active Development → GitHub/GitLab → Release → Zenodo/Archive
     (versions)     (collaboration)      (final)  (preservation)
```

### 1.3 Data Repositories

**General-Purpose Repositories:**

**Zenodo** (zenodo.org)
- Multidisciplinary storage
- Manages both data and software
- Free and unlimited
- Automatic DOI assignment
- 50 GB per record limit
- EU funding requirement
- Use for: All research outputs with archival needs

**Figshare** (figshare.com)
- Rich media support (images, presentations, videos)
- Individual file sharing and versioning
- 20 GB free storage, unlimited public files
- Custom DOIs available
- Beautiful web interface
- Use for: Visual data, figures, supplementary materials

**Open Science Framework (OSF)** (osf.io)
- Project management integrated with storage
- Version control built-in
- Preregistration and reporting workflows
- Integration with many other tools
- Free hosting
- Use for: Coordinating research projects, preregistration

**Dataverse** (dataverse.org)
- Institutional deployment options
- Tabular data tools
- Citation standards built-in
- Harvard Dataverse example
- Good for: Institutional repositories, tabular datasets

### 1.4 Discipline-Specific Repositories

**Biological Sciences:**
- **GenBank** - DNA/protein sequences (NCBI)
- **Protein Data Bank** - 3D protein structures
- **Dryad** - Data associated with publications

**Earth and Environmental Science:**
- **NOAA** - Climate and oceanographic data
- **USGS** - Geological data and maps
- **GeoNetwork** - Geographic data discovery

**Physics and Astronomy:**
- **arXiv** - Preprints and papers
- **Zenodo** - CERN's repository (multidisciplinary)

**Social Sciences:**
- **ICPSR** - Social science research data
- **Harvard Dataverse** - General-purpose institutional

**Importance of Discipline Repositories:**
- Specialized metadata standards
- Community-appropriate preservation
- Field-specific discovery tools
- Long-term stability
- Funding recognition

### 1.5 Software Repositories

**Source Code Hosting:**

**GitHub** (github.com)
- Most popular for research software
- Built on Git version control
- Public and private repositories
- Collaborative features (pull requests, issues)
- CI/CD integration
- GitHub Pages for documentation
- Free for public repositories
- Use for: Active development, collaboration

**GitLab** (gitlab.com)
- Similar to GitHub with self-hosting options
- Stronger privacy controls
- Runner infrastructure included
- Enterprise-grade features
- Use for: Privacy-sensitive work, institutional deployment

**Package Registries:**

**PyPI** (pypi.org) - Python
- 500,000+ packages
- `pip install` command standard
- Peer review through community
- Documentation hosting

**CRAN** (cran.r-project.org) - R
- 20,000+ packages
- Automated testing
- Vignettes and documentation
- Strong quality standards

**Zenodo and Software:**
- Direct software upload
- Automatic DOI for released versions
- GitHub-Zenodo integration (auto-archive releases)
- Preservation timeline: 20+ years

### 1.6 Choosing the Right Repository

**Decision Matrix:**

| Need | Best Choice | Rationale |
|------|-------------|----------|
| Active code development | GitHub/GitLab | Full version control |
| Final dataset archival | Zenodo/Figshare | Long-term preservation |
| Discipline-specific data | Domain repository | Specialized standards |
| Institutional requirement | Institutional repo | Policy compliance |
| Visual supplementary materials | Figshare | Rich media support |
| Python package distribution | PyPI | Standard ecosystem |
| Project coordination | Open Science Framework | Workflow integration |

**Getting Started:**
1. Check funder/publisher requirements (often mandate specific repositories)
2. Identify discipline-specific options
3. Consider your data sensitivity and access needs
4. Plan workflow: development → release → archive
5. Obtain persistent identifiers (DOI)

### Summary

Repositories are foundational tools for open science:
- **Development repositories** (GitHub) support collaboration
- **Data repositories** (Zenodo, Figshare) enable archival and discovery
- **Discipline-specific repositories** follow community standards
- **Software registries** (PyPI, CRAN) distribute packages
- Combine multiple repositories for maximum effectiveness

## Lesson 2: Version Control and Collaboration

### Overview
In this lesson, you learn about version control systems that track changes to code and documentation, understand different approaches to version control, explore platforms that facilitate collaboration, and practice implementing version control in your research workflow.

### 2.1 What is Version Control?

**Definition:** Version control is the practice of systematically tracking and managing changes to files, including code, documentation, and research outputs.

**Core Functions:**
1. **History tracking** - See who changed what and when
2. **Change documentation** - Messages explaining why changes were made
3. **Reversion** - Return to previous versions if needed
4. **Parallel development** - Multiple people work simultaneously
5. **Merge capability** - Combine changes from multiple developers

**Why Researchers Need It:**
- Reproducibility: Track exactly what code/analysis was used
- Collaboration: Multiple authors contribute safely
- Backup: Distributed copies prevent data loss
- Accountability: Clear record of contributions
- Experimentation: Safe to try new approaches

### 2.2 Types of Version Control Systems

**Centralized Version Control**

**How it works:**
- Single central server holds all version history
- Developers check out files to work locally
- Changes committed back to central server

**Examples:** Subversion (SVN), Perforce, CVS

**Advantages:**
- Simpler conceptual model
- Clear central authority
- Easier access control

**Disadvantages:**
- Server dependency (offline work limited)
- Network traffic for every operation
- Single point of failure

**Distributed Version Control**

**How it works:**
- Every developer has complete repository copy
- History exists locally
- Changes merged between repositories

**Examples:** Git, Mercurial (Hg), Bazaar

**Advantages:**
- Works offline (full history available)
- Redundancy (copies are backups)
- Parallel workflows easier
- Performance (local operations fast)

**Disadvantages:**
- More complex learning curve
- Larger local storage (full history)
- More merge conflict scenarios

**Modern Reality:** Git has dominated; understanding distributed concepts is essential.

### 2.3 Git Fundamentals

**Key Concepts:**

**Commit:** Snapshot of files at a point in time
```
✓ Each commit has:
  - Unique ID (hash)
  - Author and date
  - Message describing changes
  - Record of what changed
```

**Branch:** Independent development line
```
main branch:  ●---●---●---●
                    |
dev branch:         ●---●---●
```

**Merge:** Combining branches
```
Before merge:       After merge:
main: ●---●---●     main: ●---●---●---●
          |              |       |
dev:  ●---●---●         ●---●---●
```

**Workflow Example (Researcher):**
1. Create analysis branch
2. Make commits as you develop
3. Test thoroughly on branch
4. Create pull request for review
5. Merge to main branch
6. Main branch always has working code

### 2.4 Collaboration Platforms

**GitHub** (github.com) - Dominant platform
- **Users:** 100+ million, especially in open source
- **Free tier:** Public repositories unlimited, private with limits
- **Features:**
  - Pull requests (code review)
  - Issues (discussion and bug tracking)
  - GitHub Actions (automation/CI)
  - GitHub Pages (documentation websites)
  - Discussions (community support)
- **Best for:** Open source, large teams, educational use

**GitLab** (gitlab.com) - Full-featured alternative
- **Users:** 30+ million, growing in enterprise
- **Free tier:** Generous for public and private
- **Features:**
  - All GitHub features
  - Self-hosting options available
  - Built-in runners for CI/CD
  - Stronger privacy controls
- **Best for:** Privacy-sensitive work, institutional deployment

**Bitbucket** (bitbucket.org) - Atlassian ecosystem
- **Users:** Popular in enterprise, less in research
- **Features:**
  - Supports Git and Mercurial
  - Jira integration (project management)
  - Atlassian ecosystem integration
- **Best for:** Teams using Jira and other Atlassian tools

**Institutional Repositories:**
- GitLab Community Edition (self-hosted)
- Gitea (lightweight self-hosted)
- Gitlab Cloud Dedicated
- For privacy requirements and institutional control

### 2.5 Best Practices for Research

**Repository Organization:**
```
my-research-project/
├── README.md              (project overview)
├── .gitignore             (files to exclude)
├── data/                  (raw data, not code)
├── code/                  (analysis scripts)
├── results/               (outputs, often generated)
├── manuscripts/           (papers)
├── docs/                  (documentation)
└── .github/
    └── workflows/         (automation)
```

**Commit Message Best Practices:**
```
✓ Good: "Add confidence intervals to figure 3 analysis"
✗ Bad: "update"

✓ Good: "Fix dimension mismatch in preprocessing (issue #42)"
✗ Bad: "debug"

✓ Good: "Replace old data cleaning code with new function"
✗ Bad: "cleanup"
```

**Collaboration Workflow:**
1. Create branch for new feature: `git checkout -b feature-name`
2. Make small, focused commits
3. Push branch: `git push origin feature-name`
4. Create pull request with description
5. Request review from collaborators
6. Address feedback with additional commits
7. Merge to main after approval
8. Delete branch after merge

**What to Version Control:**
- ✓ Code and scripts
- ✓ Documentation and manuscripts
- ✓ Configuration files
- ✓ Results and figures (if small)
- ✗ Raw data (use data repositories instead)
- ✗ Large files (use Git LFS or data repositories)
- ✗ Sensitive information (use environment variables)

### Summary

Version control is essential for open science:
- **Distributed systems** (Git) enable offline work and redundancy
- **Platforms** (GitHub, GitLab) add collaboration features
- **Best practices** ensure code quality and reproducibility
- **Workflow discipline** prevents conflicts and maintains clarity
- **Version control + repositories** = complete research preservation

## Lesson 3: Persistent Identifiers and Citation

### Overview
In this lesson, you learn about persistent identifiers that ensure your research outputs remain discoverable and citable over time. You explore different types of identifiers, understand how they work technically, and practice obtaining and using them in your research.

### 3.1 What is a Persistent Identifier?

**Definition:** A persistent identifier (PID) is a long-lasting reference to a digital resource that remains valid and points to the same content indefinitely, even if URLs or storage locations change.

**Why Important:**
- URLs break (average: 1.6 per day on Wikipedia)
- Institutions reorganize and move files
- Server migrations happen
- Research outputs need permanent references

**Persistent ID Properties:**
1. **Permanence:** Reference valid indefinitely
2. **Uniqueness:** Identifies specific version/item
3. **Resolvability:** Directs to current location
4. **Universal:** Works across institutions/platforms
5. **Citable:** Standard format for citations

**Example Problem Solved by PIDs:**
```
Without PID:
Link: http://myuniversity.edu/research/data/study123
↓ (Months later)
My files moved → Link broken → Research unreachable

With PID (DOI):
DOI: 10.5281/zenodo.1234567
↓ (Months later)
Files moved → DOI resolver updated → Still works
```

### 3.2 Digital Object Identifier (DOI)

**What is a DOI?**
- Most widely used PID in research
- Standardized by ISO (International Organization for Standardization)
- Managed globally by registration agencies

**Format:**
```
10.5281/zenodo.1234567
┬─ ┬──────────────────
│  └─ Suffix (unique identifier)
└─── Prefix (registration agency)
```

**Major DOI Registration Agencies:**

**CrossRef** (crossref.org) - Academic publishing
- Issues ~100 million DOIs annually
- Articles, conference proceedings, books
- Journal publishers primary users
- Resolves through doi.org

**DataCite** (datacite.org) - Research data
- Issues ~50 million DOIs annually
- Datasets, software, other research outputs
- Repositories: Zenodo, Figshare, Dryad
- Rich metadata support

**How DOI Resolution Works:**
```
1. You cite: doi.org/10.5281/zenodo.1234567
2. User clicks/types the DOI
3. doi.org proxy resolves to current URL
4. User reaches content (wherever it is now)
```

**Obtaining DOIs:**

**For Published Articles:**
- Publisher automatically issues
- Available after publication
- Usually free

**For Research Data:**
- Deposit in DataCite member repository
- Zenodo: Automatic DOI on upload
- Figshare: Automatic DOI on publication
- Dataverse: Automatic DOI
- Free

**For Software:**
- GitHub → Zenodo integration (GitHub releases auto-archived)
- Direct Zenodo upload
- PyPI/CRAN packages

**Metadata Requirements:**
- Title
- Creators/Authors
- Publication date
- Resource type (dataset, software, article)
- Description (optional but recommended)

### 3.3 ORCID: Researcher Identifier

**What is ORCID?**
- Open Researcher and Contributor ID
- Unique 16-digit identifier for researchers
- Links your publications, datasets, contributions
- International standard (ISO 27729)

**ORCID Format:**
```
ORCID: 0000-0002-1825-0097
       │      │    │    │
       └──────┴────┴────┴─ Unique number
```

**Why Researchers Need ORCID:**

**Name Disambiguation:**
- "John Smith" appears 10,000+ times
- ORCID uniquely identifies you
- Works across languages and transliteration

**Comprehensive Profile:**
- All your publications in one place
- Datasets and software you've produced
- Grants and funding
- Affiliations and employment history
- Works across all databases

**Integration with Systems:**
- Funding agencies (NSF, NIH, EU)
- Repositories (Zenodo, Figshare)
- Journals (Nature, Science, eLife)
- University repositories
- Automated data import from CrossRef/DataCite

**Getting and Using ORCID:**
1. Create account at orcid.org (free)
2. Add biographical information
3. Add publications and works (manual or auto-import)
4. Set privacy settings (public/limited/private)
5. Use ORCID in funding/publication submissions
6. Example: "Josephine Doe (ORCID: 0000-0002-1825-0097)"

**Citation Impact:**
- ORCID profiles increase discoverability
- Better tracking of research impact
- Funder recognition of your contributions
- Clear career record for job applications

### 3.4 Other Persistent Identifier Types

**ARK (Archival Resource Key)**
- Emphasis on long-term preservation
- Especially for library and archive materials
- Example: ark:/13030/c7h0rt9s
- Used by: Internet Archive, libraries, archives
- Best for: Cultural heritage, manuscripts

**Handle System**
- Protocol and network for PID resolution
- Foundation that DOI system is built on
- More complex than DOI for end-users
- Used for: Large digital collections

**URLs with Preservation:**
- Institutional repositories often issue URLs
- Less stable than formal PIDs
- Solution: Use alongside DOI

**ISBN/ISSN (Publications)**
- ISBN: Books
- ISSN: Serial publications (journals, magazines)
- Limited to specific formats
- Important for: Citation of monographs and journals

### 3.5 Using Persistent Identifiers in Citations

**Citation Format Examples:**

**Dataset with DOI:**
```
Author, A. (2024). Title of dataset (Version 1.0.0) 
[Data set]. Zenodo. https://doi.org/10.5281/zenodo.1234567
```

**Software with DOI:**
```
Author, A. (2024). Software name (v2.1.0). Zenodo. 
https://doi.org/10.5281/zenodo.1234567
```

**Journal Article:**
```
Smith, J., Jones, B., & Brown, C. (2024). Title. 
Journal Name, 15(3), 123-145. 
https://doi.org/10.1234/journal.2024.001234
```

**Including Author ORCID:**
```
Smith, J. (ORCID: 0000-0002-1825-0097), Jones, B. & Brown, C. 
(2024). Title. Journal Name, 15(3), 123-145.
```

**Automatic Citation Generation:**
- Most repositories provide citation in multiple formats
- Zenodo: BibTeX, JSON, DataCite, Dublin Core, RIS
- Figshare: Same formats
- Google Scholar: Bibtex, Abstract
- Copy-paste into bibliography

### 3.6 Best Practices with Persistent Identifiers

**For Research Data:**
1. Use repository that issues DOIs (Zenodo, Figshare, Dryad)
2. Complete metadata (title, creators, description)
3. Use DataCite schema
4. Include in data availability statement
5. Cite in publications when used

**For Software:**
1. Create GitHub releases
2. Connect to Zenodo for archival and DOI
3. Each release gets unique DOI
4. Version semantically (1.0.0 format)
5. Cite software in publications (Software Citation Principles)

**For Yourself:**
1. Create ORCID profile
2. Keep it up to date
3. Set appropriate privacy levels
4. Use in grant applications and submissions
5. Link your research outputs

**In Publications:**
1. Include data availability statements with DOIs
2. Link to code repositories and software
3. List contributor ORCIDs
4. Use persistent links (DOIs, not URLs)
5. Make supplementary materials citable

### Summary

Persistent identifiers are essential research infrastructure:
- **DOIs** ensure long-term access to research outputs
- **ORCIDs** uniquely identify researchers and their contributions
- **Proper use** enables discovery, citation tracking, and impact measurement
- **Best practices** maximize discoverability and credit attribution

## Lesson 4: Open Science Software Ecosystems

### Overview
In this lesson, you explore the broader ecosystem of tools used in open science beyond version control and repositories. You learn about tools for documentation, collaboration, preprint sharing, project management, and data management planning. You understand how these tools integrate to support reproducible research.

### 4.1 Documentation and Manuscript Tools

**Overleaf** (overleaf.com) - Collaborative LaTeX Writing
- **Purpose:** Cloud-based LaTeX editor for manuscripts
- **Features:**
  - Real-time collaboration (like Google Docs)
  - 10,000+ templates (journal formats, theses)
  - Integrated version history
  - Bibliography management (BibTeX)
  - Direct submission to journals
- **Pricing:** Free version limited, premium $12-30/month
- **Best for:** Collaborative manuscript writing, complex formatting
- **Integration:** Works with Git (optional)

**Google Docs** - Cloud Collaboration
- **Purpose:** Simple collaborative writing
- **Advantages:**
  - Extremely easy to use
  - Simultaneous real-time editing
  - Comment and suggestion modes
  - Built-in version history
  - Free (Google account required)
- **Limitations:** Not ideal for formatted manuscripts
- **Best for:** Early drafts, quick collaboration, non-technical teams

**Microsoft Word with OneDrive**
- **Purpose:** Familiar alternative to Google Docs
- **Features:** Co-authoring, comments, track changes
- **Best for:** Teams already in Microsoft ecosystem

**Markdown + GitHub**
- **Purpose:** Lightweight manuscript writing
- **Advantages:** Version control, plain text, reviewable diffs
- **Tools:** Pandoc, Jupyter Book, Quarto
- **Best for:** Technical manuscripts, reproducible research

### 4.2 Computational Research Tools

**Jupyter Notebooks** (jupyter.org)
- **What:** Interactive documents mixing code, output, and narrative
- **Supported languages:** Python, R, Julia, 100+ kernels
- **Advantages:**
  - Explains analysis alongside code
  - Reproducible from notebook
  - Rich output (plots, tables, LaTeX)
  - Educational and publication-ready
- **Use cases:** 
  - Teaching and tutorials
  - Data exploration
  - Publication of analyses
- **Archiving:** Can be deposited in repositories with DOIs

**Quarto** (quarto.org)
- **What:** Scientific publishing system
- **Capabilities:**
  - Mix code and prose (Python, R, Julia, Observable)
  - Render to HTML, PDF, Word, presentations
  - Cross-references, citations, figures
  - Websites and books
- **Advantages:** More flexible than Jupyter
- **Best for:** Complete research communication

**R Markdown**
- **What:** R-specific document format
- **Creates:** PDFs, HTML, Word documents
- **Advantages:** Seamless R integration
- **Best for:** R-focused research

**Jupyter Book** (jupyterbook.org)
- **What:** Build publication-quality books from Jupyter Notebooks
- **Features:**
  - Table of contents and navigation
  - Cross-references
  - Bibliography management
  - Web hosting ready
- **Best for:** Textbooks, theses, comprehensive analyses

### 4.3 Preprint Servers

**arXiv** (arxiv.org) - Multidisciplinary Preprints
- **Coverage:** Physics, astronomy, mathematics, computer science, quantitative biology
- **Volume:** 500,000+ papers annually
- **Timeline:** No peer review (moderation only)
- **Permanence:** Permanent (no deletion)
- **Discovery:** Heavily indexed by search engines
- **Best for:** Physics-heavy research

**bioRxiv** (biorxiv.org) - Biology Preprints
- **Coverage:** All biology fields
- **Volume:** 100,000+ papers annually
- **Timeline:** Typically published to journal within 6 months
- **Features:** Integrated with journal submission workflows
- **Best for:** Biological sciences

**medRxiv** (medrxiv.org) - Medicine and Health
- **Coverage:** Medicine, health sciences
- **Rapid dissemination:** Important for urgent health findings
- **COVID-19 rapid response:** Enabled pre-publication sharing
- **Best for:** Medical research

**PsyArXiv** (psyarxiv.org) - Psychology Preprints
- **Coverage:** Psychology and related fields
- **Features:** Integrated with Open Science Framework
- **Best for:** Psychological sciences

**OSF Preprints** (osf.io/preprints) - Multidisciplinary
- **Coverage:** All disciplines
- **Features:** Integrated with project management
- **Best for:** Researchers already using OSF

**Benefits of Preprints:**
- Rapid dissemination (days vs. months)
- Priority establishment (before formal publication)
- Feedback collection (improves final version)
- Global visibility
- Often required by funders

### 4.4 Project Management and Workflows

**Open Science Framework (OSF)** (osf.io)
- **What:** Integrated research project management platform
- **Features:**
  - Project organization and file storage
  - Preregistration (registered reports)
  - Collaboration and team management
  - Wiki documentation
  - Integration with GitHub, Dropbox, Google Drive
  - Preprint server
- **Pricing:** Free
- **Best for:** Coordinating all project aspects, preregistration

**GitHub Projects**
- **What:** Project management integrated with repositories
- **Features:**
  - Kanban boards (To Do, In Progress, Done)
  - Issue tracking and milestones
  - Automation (assign to issues, automatic closing)
  - Limited but sufficient for research
- **Pricing:** Free (included with GitHub)
- **Best for:** Code-heavy projects

**Lab Notebooks**
- **Traditional:** Physical notebooks (permanent record)
- **Digital:**
  - Notion, OneNote (note-taking)
  - GitHub wikis (collaborative)
  - OSF wiki (research-specific)
- **Requirements:**
  - Dated entries
  - Experiments recorded
  - Methods documented
  - Results noted
  - Accessible to team

### 4.5 Data Management Planning

**DMPTool** (dmptool.org)
- **What:** Data management plan (DMP) writing assistant
- **Features:**
  - Templates for major funders (NSF, NIH, EU)
  - Question prompts with guidance
  - Institutional support integration
  - Export to PDF or funder formats
- **Pricing:** Free
- **Best for:** Grant proposals requiring DMPs

**Data Stewardship Wizard** (dsw.fairdata.eu)
- **What:** European alternative to DMPTool
- **Features:**
  - Comprehensive question sets
  - Output to multiple formats
  - Integration with FAIR principles
- **Pricing:** Free
- **Best for:** FAIR compliance

**Funders Requiring DMPs:**
- **NSF:** Required for all grants
- **NIH:** Common for certain mechanisms
- **EU Horizon Europe:** Required
- **NIH DMSP:** New requirement (2023+)
- **Most foundations:** Increasingly required

**Key DMP Sections:**
1. Data types and collection
2. Data storage and backup
3. Data quality and documentation
4. Access and sharing plans
5. Archival and preservation strategy
6. Roles and responsibilities
7. Budget and resources

### 4.6 Team Communication

**Slack** - Team Messaging
- **Features:** Real-time chat, channels, integrations
- **Research use:** Lab communication, integration with tools
- **Pricing:** Free with limitations, $10+/month paid

**Discord** - Community Communication
- **Features:** Voice, video, text, community-focused
- **Research use:** Open science communities, study groups
- **Pricing:** Free

**Mailing Lists**
- **Traditional:** Email-based discussion
- **Tools:** Google Groups, Listserv
- **Advantages:** Accessible, persistent, searchable

### Summary

Comprehensive tool ecosystem supports open science:
- **Documentation tools** enable collaborative manuscript writing
- **Computational tools** make analyses reproducible and transparent
- **Preprint servers** enable rapid dissemination
- **Project management** coordinates research activities
- **Planning tools** help meet funder requirements
- **Communication tools** support team collaboration

## Lesson 5: Building Your Open Science Toolkit

### Overview
In this final lesson, you integrate the tools learned throughout this module into a practical toolkit. You learn to select appropriate tools for your research, implement them systematically, and build sustainable practices. You also explore communities, resources, and next steps for deepening your tool expertise.

### 5.1 Assessing Your Tool Needs

**Research Stage Analysis:**

**Planning Phase:**
- **Tools:** DMPTool, preregistration (OSF)
- **Purpose:** Plan data management, register hypotheses
- **Output:** DMP document, registration URL

**Active Research Phase:**
- **Tools:** Lab notebooks (digital or Notion), GitHub, OSF
- **Purpose:** Document experiments, version code, track progress
- **Output:** Documented notebook, version-controlled code

**Analysis Phase:**
- **Tools:** Jupyter notebooks/Quarto, GitHub, version control
- **Purpose:** Reproducible analyses, documented workflows
- **Output:** Executable code documents with results

**Publication Phase:**
- **Tools:** Preprint server, Overleaf/Google Docs, GitHub
- **Purpose:** Rapid dissemination, collaborative writing
- **Output:** Preprint with DOI, peer review feedback

**Archival Phase:**
- **Tools:** Zenodo, Figshare, data repositories, GitHub releases
- **Purpose:** Long-term preservation, discovery, citation
- **Output:** Datasets and code with DOIs, permanent URLs

### 5.2 Discipline-Specific Tool Recommendations

**Computational Sciences** (Computer Science, Statistics, Physics)
- **Code:** GitHub (essential)
- **Notebooks:** Jupyter or Quarto
- **Manuscripts:** Overleaf or Markdown + Pandoc
- **Preprints:** arXiv
- **Archival:** Zenodo
- **Data:** Zenodo or figshare
- **Project mgmt:** GitHub Projects or OSF

**Biological Sciences** (Biology, Medicine, Life Sciences)
- **Code:** GitHub
- **Manuscripts:** Overleaf or Word
- **Preprints:** bioRxiv or medRxiv
- **Data:** Zenodo, Figshare, Dryad, or domain-specific repositories
- **Samples/sequences:** GenBank, PDB
- **Project mgmt:** OSF (for workflows), GitHub

**Social Sciences** (Psychology, Economics, Sociology)
- **Code:** GitHub or OSF repository
- **Preregistration:** OSF (strongly recommended)
- **Data:** OSF, Zenodo, Figshare (sensitivity)
- **Manuscripts:** Google Docs or Overleaf
- **Project mgmt:** Open Science Framework

**Environmental Sciences** (Ecology, Climate, Geology)
- **Data:** Discipline-specific (NOAA, USGS) or Zenodo
- **Code:** GitHub
- **Notebooks:** Jupyter for analysis documentation
- **Preprints:** EarthArXiv
- **Data access:** Domain repositories essential

**Humanities** (History, Literature, Languages)
- **Repositories:** Institutional repositories, digital humanities platforms
- **Manuscripts:** Google Docs, Markdown
- **Data:** Zenodo for primary sources
- **Version control:** Git for collaborative projects
- **Preprints:** limited uptake (varies by discipline)

### 5.3 Building Your Toolkit: Step by Step

**Month 1: Foundation**
```
Week 1:
  ☐ Create GitHub account
  ☐ Create ORCID profile
  ☐ Set up local Git

Week 2-3:
  ☐ Create first repository
  ☐ Initialize basic structure
  ☐ Add README and license

Week 4:
  ☐ Learn Git basics (commits, branches)
  ☐ Practice with small project
```

**Month 2: Documentation**
```
Week 1-2:
  ☐ Choose documentation approach (Jupyter/Markdown/Overleaf)
  ☐ Start documenting current project
  ☐ Create template for future projects

Week 3-4:
  ☐ Document data management practices
  ☐ Create lab notebook system
  ☐ Practice with code documentation
```

**Month 3: Data and Code**
```
Week 1:
  ☐ Audit current data management
  ☐ Write basic DMP (even if not required)
  ☐ Plan data archival strategy

Week 2-3:
  ☐ Organize code repository
  ☐ Add tests or validation
  ☐ Create documentation

Week 4:
  ☐ Publish to data repository
  ☐ Obtain DOI
  ☐ Update ORCID profile
```

**Ongoing:**
```
Monthly:
  ☐ Review and update ORCID
  ☐ Version control commits (regular pushes)
  ☐ Data backups verified

Quarterly:
  ☐ Review tool choices
  ☐ Update documentation
  ☐ Join relevant communities

Annually:
  ☐ Archive completed projects
  ☐ Review tool updates
  ☐ Plan next year's open science goals
```

### 5.4 Common Tool Combinations

**Minimal Setup** (Easiest Entry Point)
```
Version Control:  GitHub
Data:             Zenodo (or Figshare)
Manuscripts:      Google Docs
Preprints:        Disciplinary server
Identification:   ORCID
```

**Standard Setup** (Balanced Approach)
```
Version Control:  GitHub
Project Mgmt:     GitHub Projects or OSF
Documentation:    Jupyter Notebooks or Quarto
Data:             GitHub (code) + Zenodo (data)
Manuscripts:      Overleaf or Google Docs
Preprints:        Disciplinary server
Identification:   DOI (auto from Zenodo), ORCID
```

**Comprehensive Setup** (Maximum Integration)
```
Planning:         OSF + DMPTool
Preregistration:  OSF
Code/VCS:         GitHub
Project Mgmt:     GitHub Projects + OSF
Notebooks:        Jupyter + GitHub
Data Mgmt:        GitHub (code), Zenodo (data)
Lab Notebook:     OSF wiki or digital notebook
Manuscripts:      Overleaf
Preprints:        Disciplinary server
Identification:   ORCID, DOIs (auto), GitHub DOI archive
Collaboration:    GitHub issues, Slack
```

### 5.5 Open Science Tool Communities

**Software Carpentry / The Carpentries**
- **Focus:** Teaching open science skills
- **Specialties:** Git, data management, research software
- **Format:** Free 2-day workshops
- **Website:** carpentries.org
- **How to join:** Register for local workshop or teach

**rOpenSci / PyOpenSci**
- **Focus:** Open source tools for research
- **Specialties:** R/Python packages, code review
- **Activities:** Collaborative development, peer review
- **Websites:** ropensci.org, pyopensci.org

**Research Software Engineering (RSE) Communities**
- **US-RSE:** usrse.org
- **International-RSE:** international-rse.org
- **Focus:** Professional development for research software

**Repository-Specific Communities**
- **Zenodo:** Zenodo users community
- **GitHub:** GitHub discussions, GitHub Community Forum
- **OSF:** Open Science Framework community

**Tool-Specific Resources**
- **Git:** Pro Git book (free), Atlassian tutorials
- **Jupyter:** Jupyter community, JupyterHub documentation
- **Quarto:** Quarto documentation and forum

### 5.6 Troubleshooting Common Tool Issues

**Problem: "I'm using too many tools"**
- Solution: Consolidate where possible (e.g., GitHub for both code and project management)
- Reality: Most researchers use 3-5 core tools
- Approach: Start minimal, add tools as needed

**Problem: "My institution doesn't support these tools"**
- Solution: Use cloud-based alternatives (GitHub, Zenodo, Google Docs)
- Advocate: Request institutional support or training
- Bridge: Use free options while advocating

**Problem: "My collaborators don't know these tools"**
- Solution: Provide training or pair programming
- Resources: The Carpentries workshops
- Phased approach: Learn together incrementally

**Problem: "These tools feel overwhelming"**
- Solution: Start with one tool well (usually Git)
- Timeframe: 3-6 months to become comfortable
- Support: Find local experts or mentors
- Reality: Tools improve workflow significantly after learning curve

### 5.7 Your Open Science Toolkit Checklist

**Essential (Start Here):**
- ☐ Version control (GitHub)
- ☐ ORCID profile
- ☐ Persistent identifiers (DOI from repository)

**Highly Recommended (Month 2-3):**
- ☐ Data repository (Zenodo or discipline-specific)
- ☐ Preprint server
- ☐ Collaborative writing tool (Overleaf or Google Docs)
- ☐ Lab notebook system

**Project Management (Ongoing):**
- ☐ Issue tracking (GitHub Issues)
- ☐ Project board (GitHub Projects or OSF)
- ☐ Team communication (Slack/Discord or email)

**Planning & Compliance:**
- ☐ Data management plan (DMPTool)
- ☐ Preregistration (OSF) if applicable
- ☐ Funder requirement documentation

**Documentation & Discovery:**
- ☐ README files
- ☐ Code documentation/comments
- ☐ Data dictionaries
- ☐ Method documentation

### 5.8 Measuring Success

**Tool Adoption Metrics:**
- Consistency: Regular commits, updates
- Discoverability: DOI cited in publications
- Collaboration: Pull requests, contributions
- Impact: Citation metrics from Altmetric, ORCID

**Process Improvements:**
- Time saved through reuse of documented code
- Reproducibility verified through others using your tools/data
- Efficiency gains from automation
- Team alignment and reduced miscommunication

**Research Impact:**
- Citations to your work (DOI tracking)
- Reuse of your code/data
- Collaboration opportunities from visible work
- Funding success (increasingly valued by funders)

### Summary

Building an open science toolkit involves:
- **Assessment:** Understand your needs by research stage
- **Selection:** Choose appropriate tools for your discipline
- **Integration:** Combine tools into coherent workflow
- **Practice:** Build skills gradually through consistent use
- **Community:** Join communities for support and learning
- **Sustainability:** Establish practices that persist long-term
- **Impact:** Measure benefits through discovery, collaboration, and citations

**Remember:**
- You don't need every tool
- Start with essentials (Git, ORCID, DOI)
- Learn at your own pace
- Community support is available
- Tools enable better science
- Your toolkit will evolve

**Your Next Steps:**
1. Choose one tool to learn this week (probably Git/GitHub)
2. Complete one tutorial or workshop
3. Apply it to your next project
4. Join a relevant community
5. Help others learn

**Welcome to the open science tools community. Let's make research better together.**
