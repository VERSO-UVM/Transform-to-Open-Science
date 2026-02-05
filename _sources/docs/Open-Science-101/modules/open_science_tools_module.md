# Module 5 - Open Science Tools

## Introduction

Open science tools are digital resources and instruments that support research through data storage, code collaboration, persistent identification, documentation, and community engagement. These tools are essential for implementing open science practices, enabling reproducibility, and facilitating collaboration.

## Learning Objectives

After completing this module, you should be able to:
- Describe the purpose and types of repositories used in open science, including development repositories, data archives, and discipline-specific platforms.
- Explain version control systems and how they enable collaborative research through tracking changes and managing contributions.
- Understand persistent identifiers (DOIs, ORCIDs, ARKs) and how they enable citation, discoverability, and long-term access to research outputs.
- Evaluate open science tools and platforms to select appropriate ones for your research workflow and data management needs.
- Implement a comprehensive toolkit combining repositories, version control, persistent identifiers, and collaboration tools.
- Build sustainable practices for managing, sharing, and preserving research outputs using appropriate open science infrastructure.

---

## Lesson 1: Repositories and Data Storage

### Overview
In this lesson, you explore the different types of repositories used to store and preserve research data and software, understand the differences between development repositories and archives, and learn how to select appropriate platforms for your research outputs.

### 1.1 What is a Repository?

A repository is a digital storage system that keeps research data, code, and documentation organized and accessible. It provides a stable home for your outputs, makes them discoverable through search and indexing, and preserves them for long-term use so others can return to the work years later. Repositories also support versioning, which means changes can be tracked over time and specific releases can be referenced when results are cited or reused.

At its core, a repository delivers five essential services. It offers **storage** through secure and reliable hosting, **access** through public or restricted permissions, and **preservation** by maintaining files and migrating formats as needed. It also supplies **metadata** that describes what the content is and how to use it, and **persistence** by assigning identifiers such as DOIs so the work can always be found and cited.

### 1.2 Repository vs. Archive: Key Differences

| Development Repositories | Archives (Data Preservation) |
|---|---|
| **Purpose:** Active collaborative development | **Purpose:** Long-term preservation of final versions |
| **Version Control:** Full Git/Mercurial/SVN integration | **Version Control:** Minimal (snapshot preservation) |
| **History:** Complete change tracking | **History:** Limited to deposited versions |
| **Branching:** Experimental and parallel work | **Immutability:** Final versions cannot be changed |
| **Examples:** GitHub, GitLab, Bitbucket | **Examples:** Zenodo, Figshare, Dataverse |
| **Use When:** Actively writing code, multiple developers, rapid iterations | **Use When:** Publishing final datasets, archiving software releases, preservation required |

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

**Open Science Framework (OSF)** ([https://osf.io/](https://osf.io/))
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

Discipline-specific repositories matter because they use field-appropriate metadata standards, align with community practices, and provide discovery tools tailored to how your field searches for data. They also prioritize long-term preservation and help ensure that data sharing aligns with funder expectations and disciplinary norms, which strengthens reuse and recognition.

**Biological Sciences:**
- **GenBank** - DNA/protein sequences (NCBI) ([https://www.ncbi.nlm.nih.gov/genbank/](https://www.ncbi.nlm.nih.gov/genbank/))
- **Protein Data Bank** - 3D protein structures ([https://www.rcsb.org/](https://www.rcsb.org/))
- **Dryad** - Data associated with publications ([https://datadryad.org/](https://datadryad.org/))

**Earth and Environmental Science:**
- **NOAA** - Climate and oceanographic data ([https://www.noaa.gov/](https://www.noaa.gov/))
- **USGS** - Geological data and maps ([https://www.usgs.gov/](https://www.usgs.gov/))
- **GeoNetwork** - Geographic data discovery ([https://geonetwork-opensource.org/](https://geonetwork-opensource.org/))

**Physics and Astronomy:**
- **arXiv** - Preprints and papers ([https://arxiv.org/](https://arxiv.org/))
- **Zenodo** - CERN's repository (multidisciplinary) ([https://zenodo.org/](https://zenodo.org/))

**Social Sciences:**
- **ICPSR** - Social science research data ([https://www.icpsr.umich.edu/](https://www.icpsr.umich.edu/))
- **Harvard Dataverse** - General-purpose institutional ([https://dataverse.harvard.edu/](https://dataverse.harvard.edu/))

### 1.5 Software Repositories

Software repositories provide the infrastructure for developing, sharing, and sustaining research code. They make collaboration practical by tracking changes, enabling review, and preserving project history so others can verify, reuse, and build on your work. Platforms like GitHub and GitLab are central to this ecosystem because they pair Git version control with collaboration features (issues, pull/merge requests, CI/CD, documentation hosting) that help research teams work transparently and reproducibly.

| Feature | GitHub | GitLab |
|---|---|---|
| **Primary strength** | Large open-source community and discovery | Integrated DevOps and strong self-hosting options |
| **Hosting options** | Cloud-hosted (GitHub.com), enterprise options | Cloud-hosted (GitLab.com) and robust self-hosted | 
| **Collaboration** | Pull requests, issues, discussions | Merge requests, issues, epics |
| **CI/CD** | GitHub Actions (marketplace-driven) | Built-in CI/CD with runners |
| **Privacy controls** | Private repos and org controls | Stronger enterprise privacy and on-prem controls |
| **Best fit** | Open-source visibility and broad community | Institutions needing self-hosting or integrated pipelines |

**Package Registries:**

Package registries are centralized catalogs that host, index, and distribute reusable software packages. They make it easy for researchers to share code with consistent versioning, dependencies, and documentation, and they allow others to install and update packages reliably using standard tools (for example, `pip` for Python or `install.packages()` for R). In practice, registries act as the publication layer for research software, enabling discoverability, citation, and long-term reuse.

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

### Summary

Repositories are foundational tools for open science:
- **Development repositories** (GitHub) support collaboration
- **Data repositories** (Zenodo, Figshare) enable archival and discovery
- **Discipline-specific repositories** follow community standards
- **Software registries** (PyPI, CRAN) distribute packages
- Combine multiple repositories for maximum effectiveness

:::{admonition} Activities for Lesson 1
:class: activity

Complete at least two of the following activities to apply repository concepts:

**Activity 1.1: Repository Mapping**
Choose one of your current or planned projects and map where each output should live (code, raw data, cleaned data, figures, manuscript, preregistration). Identify the specific repository or platform for each output and explain why it fits.

**Activity 1.2: Development vs. Archive Decision**
Select a research artifact (e.g., codebase, dataset). Decide what should stay in a development repository versus what should be archived, and draft a release plan that includes a version number and an archival repository with a DOI.

**Activity 1.3: Data Repository Shortlist**
Create a shortlist of three repositories for your field and compare them on scope, storage limits, metadata requirements, and long-term preservation. Write 150-200 words explaining which one you would choose and why.

**Activity 1.4: Repository Metadata Draft**
Draft a metadata record for a dataset you have or plan to produce. Include title, description, creators, keywords, license, and a short README outline.
:::

## Lesson 2: Version Control and Collaboration

### Overview
In this lesson, you learn about version control systems that track changes to code and documentation, understand different approaches to version control, explore platforms that facilitate collaboration, and practice implementing version control in your research workflow.

### 2.1 What is Version Control?

Version control is a systematic way to track and manage changes to files such as code, documentation, and research outputs. Rather than relying on ad hoc file naming, it preserves a detailed history of edits so you can see who changed what, when, and why. This history also makes it easy to revert to earlier versions if something breaks or a result needs to be reproduced exactly.

Beyond tracking changes, version control enables multiple people to work in parallel and later merge their contributions into a coherent whole. That collaborative workflow is what makes modern research software development scalable and reliable. For researchers, version control supports reproducibility by pinning analyses to specific versions of code, improves accountability with clear attribution, and provides a robust backup strategy through distributed copies. It also makes experimentation safer, since you can try new ideas without risking the integrity of your main workflow.

### 2.2 Types of Version Control Systems

**Centralized Version Control**

**How it works:**
Centralized version control relies on a single central server that holds the full version history. Developers check out files to work locally and then commit their changes back to that central server.

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
In a distributed model, every developer has a complete copy of the repository, including its history. Work can proceed locally, and changes are shared and merged between repositories when collaborators synchronize their work.

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

### 2.4 Collaborative Workflows on GitHub

**Pull Request Workflow (code review):**

1. Colleague creates branch: `git checkout -b new-feature`
2. Makes changes and pushes: `git push origin new-feature`
3. Opens Pull Request on GitHub (describes what changed and why)
4. You review code: add comments, suggest changes
5. Colleague updates based on feedback
6. Once approved: merge to main

**Why this matters for research:**
- Code review catches errors before they reach your paper
- Transparent record of who suggested what changes
- Prevents accidentally breaking the analysis

**Issue Tracking (bug reports and features):**

GitHub Issues organize project work:
- "Bug: outlier detection failing on dataset X" → someone claims it, fixes it
- "Feature: add visualization for results" → someone volunteers
- Link issues to pull requests: "closes #15" in PR description

**Continuous Integration (automated testing):**

GitHub Actions run tests automatically:
```yaml
# When someone pushes code:
1. GitHub runs your analysis script
2. Checks for errors
3. Reports pass/fail
4. Prevents broken code from merging
```

**For institutions with privacy requirements:** GitLab (self-hosted on your servers) or Gitea provide the same workflows with full data control.

### 2.5 Repository Best Practices

**Organize your project:**
```
my-research/
├── README.md              # Project overview and how to run it
├── .gitignore             # Files to exclude (e.g., large data, secrets)
├── LICENSE                # MIT, GPL, Apache 2.0, etc.
├── data/                  # Raw data (read-only, with checksums)
├── code/analysis.py       # Scripts for analysis
├── results/               # Generated outputs (outputs only, not committed)
├── manuscript/            # Paper drafts and LaTeX
├── notebooks/             # Jupyter notebooks for exploration
└── .github/workflows/     # GitHub Actions for automated tests
```

**Write clear commits:**
```bash
✓ Good: git commit -m "Add outlier detection with z-score (resolves #42)"
✗ Bad:  git commit -m "update"

✓ Good: git commit -m "Fix data import error for missing values"
✗ Bad:  git commit -m "debug"
```

**Collaborate safely:**
1. Never commit passwords, API keys, or large data files
2. Use `.gitignore` to exclude: `*.csv`, `*.h5`, `.env`
3. Always create a branch for new features
4. Require code review before merging
5. Run tests automatically (GitHub Actions)

### Summary

Version control is essential for open science:
- **Distributed systems** (Git) enable offline work and redundancy
- **Platforms** (GitHub, GitLab) add collaboration features
- **Best practices** ensure code quality and reproducibility
- **Workflow discipline** prevents conflicts and maintains clarity
- **Version control + repositories** = complete research preservation

:::{admonition} Activities for Lesson 2
:class: activity

Complete at least two of the following activities to practice version control:

**Activity 2.1: Initialize a Research Repository**
Create a new Git repository for a small research project. Add a README, a license, and a basic folder structure (data, code, docs, results). Make at least three commits with clear messages.

**Activity 2.2: Branch and Merge Practice**
Create a feature branch, make a change to a file, and merge it back into `main`. Write a short reflection on what you learned about branching and merging.

**Activity 2.3: .gitignore Audit**
Create or update a `.gitignore` file for your project. Explain why each ignored category (raw data, secrets, build artifacts) should not be tracked in Git.

**Activity 2.4: Collaboration Simulation**
Open an issue describing a small improvement, then create a pull/merge request that resolves it. Write a brief summary as if you were reviewing your own change.
:::

## Lesson 3: Getting DOIs and ORCIDs

### Overview
In this lesson, you learn how to obtain and use persistent identifiers (DOIs and ORCIDs) that make your research permanently discoverable and citable. You'll get practical experience setting up your researcher profile and archiving research outputs with permanent identifiers.

### 3.1 Getting Your DOI

**When you need a DOI:**
- Publishing a dataset on **Zenodo**, **Figshare**, or **Dryad**
- Archiving code associated with a paper
- Publishing software as a package
- Sharing supplementary materials

**Step-by-step for Zenodo (free, easy, recommended):**

1. Go to [zenodo.org](https://zenodo.org)
2. Sign in with GitHub account
3. Click "Upload" → "New Upload"
4. Add files (data, code, manuscript)
5. Fill metadata:
   - Title: "Ocean temperature dataset, 2020-2024"
   - Authors: Your name + ORCID
   - Description: 1-2 sentences
   - License: CC-BY-4.0 (or your choice)
6. Click "Publish" → **DOI automatically created**
7. Copy DOI: `10.5281/zenodo.1234567`

**Using your DOI:**
- Cite in paper: Add to data availability statement
- Share on GitHub: Add to README
- Link in author profile: Add to CV/ORCID
- Permanent reference: Share in presentations

**Other repositories:**
- **Figshare** (figshare.com): Easy interface, good for figures and supplementary materials
- **Dryad** (datadryad.org): Discipline-specific data, curated submissions
- **Dataverse** (dataverse.org): University-hosted option

### 3.2 Getting Your ORCID

**What ORCID does:**
- Creates a unique researcher ID (0000-XXXX-XXXX-XXXX)
- Links all your work across platforms (Zenodo, journals, funding agencies)
- Separates you from every other researcher with your name
- Used by NSF, NIH, EU, and major journals

**Step-by-step to set up ORCID:**

1. Go to [orcid.org](https://orcid.org)
2. Click "Register" (free)
3. Fill basic info:
   - Name
   - Email
   - Password
4. Verify email (check inbox)
5. Add researcher information:
   - Affiliations (current and past institutions)
   - Funding: Search for grants you've received
   - Works: Auto-import from CrossRef or manually add
6. Set privacy: Usually "Public" (or "Limited" if preferred)
7. Copy your ORCID: **0000-XXXX-XXXX-XXXX**

**Where to use your ORCID:**
- Funding applications: NSF, NIH, EU all require ORCID now
- Journal submissions: Add to author metadata
- Your GitHub profile: Add to README
- Your email signature: `Jane Doe (ORCID: 0000-0002-1825-0097)`
- Zenodo: Link when uploading data
- LinkedIn/CV: Include in researcher profile

**Linking repositories to ORCID:**
- Zenodo auto-imports publications if you authorize it
- Search for past publications to add
- ORCID continuously updates as you publish
- Automatic imports from CrossRef, DataCite

### 3.3 Other Persistent Identifiers

**GitHub Release Versioning** (for code):
- Create GitHub release with version tag: `v1.0.0`, `v2.1.0`
- Connect to Zenodo (auto-creates DOI for each release)
- Stable snapshot for papers: "This analysis used our code v2.1.0 (doi: 10.5281/zenodo.1234567)"

**ISBN/ISSN** (for books/journals):
- ISBN: Books (13-digit, looks like ISBN: 978-3-16-148410-0)
- ISSN: Journal issues (8-digit, looks like ISSN: 0028-0836)
- Use when citing published books or journals

**Repository-specific Identifiers:**
- Figshare: Auto-generate URL for each item
- Dryad: DataCite DOI (required for publications)
- Dataverse: DOI assigned by Dataverse instance

**When to use DOI vs. GitHub URL:**
- Use GitHub URL: While code is under active development, linking to specific commits
- Use DOI: When publishing paper, submitting to journal, or archiving final version
- Both: Add DOI to GitHub README pointing to Zenodo

### 3.4 Citing Your Work

**Copy-paste citations from repositories:**

Zenodo, Figshare, and most journals provide citation formats. Example from Zenodo page:
```
Author, A. (2024). Title of dataset (Version 1.0.0) 
[Data set]. Zenodo. https://doi.org/10.5281/zenodo.1234567
```

**Adding to your paper:**

In manuscript text:
```
"Data were processed using custom Python code (Doe, 2024, 
https://doi.org/10.5281/zenodo.5678901) and statistical 
analysis was performed using R version 4.2.1 (R Core Team, 2024)."
```

In references/bibliography:
```
Doe, J., Smith, A., & Jones, B. (2024). Analysis of ocean 
temperature anomalies. Version 2.1.0. Zenodo. 
https://doi.org/10.5281/zenodo.1234567

R Core Team (2024). R: A language and environment for 
statistical computing. Version 4.2.1. Vienna, Austria: 
R Foundation for Statistical Computing.
```

**BibTeX format** (for LaTeX users):
- Zenodo: Copy BibTeX from right-side menu
- Figshare: Export → BibTeX
- GitHub: Use GitHub BibTeX export tool

**Citation managers:**
- **Zotero** (zotero.org): Free, open-source, captures DOI automatically
- **Mendeley**: Free, syncs across devices
- **Overleaf**: Built-in citation integration

### 3.5 Best Practices for Identifiers

**When publishing a paper:**
1. Get DOI for all data/code before submission
2. Add DOI to data availability statement
3. Include ORCID in author metadata
4. Reference versions in methods section

**For long-term persistence:**
- Use Zenodo over personal websites (persistence guaranteed 20+ years)
- Use DataCite repositories (Zenodo, Figshare, Dryad) - more stable than GitHub
- Archive each version: v1.0 (first publication), v1.1 (bug fix), v2.0 (major update)
- Set metadata: license, creators, dates

**Making your work discoverable:**
```
On Zenodo/Figshare:
✓ Detailed title: "Ocean surface temperature dataset, 2020-2024, 
   North Atlantic"
✓ Keywords: "temperature", "oceanography", "North Atlantic"
✓ License: CC-BY-4.0 (allows reuse with attribution)

✗ Vague: "Data"
✗ Generic title: "Dataset"
```

**Connecting across platforms:**
- Link DOI → GitHub repo in description
- Link GitHub → Zenodo DOI in README
- Add ORCID → Links everything together
- Use consistent author names (first initial + last name)

**Troubleshooting:**
- "DOI not working?" → Check prefix/suffix format (10.XXXX/xxxxx)
- "ORCID won't sync publications?" → Authorize CrossRef integration
- "Can't find old paper?" → Search Google Scholar, add manually to ORCID

**For Software:**
- Create versioned releases and archive with Zenodo for DOIs
- Use semantic versioning (e.g., 1.0.0)
- Cite software per software citation principles

**For Yourself:**
- Create and maintain an ORCID profile
- Set appropriate privacy levels
- Link all research outputs and use ORCID in submissions

**In Publications:**
- Include data availability statements with DOIs
- Link to code repositories and software
- List contributor ORCIDs
- Use persistent links and cite supplementary materials

### Summary

Persistent identifiers are essential research infrastructure:
- **DOIs** ensure long-term access to research outputs
- **ORCIDs** uniquely identify researchers and their contributions
- **Proper use** enables discovery, citation tracking, and impact measurement
- **Best practices** maximize discoverability and credit attribution

:::{admonition} Activities for Lesson 3
:class: activity

Complete at least two of the following activities to practice using persistent identifiers:

**Activity 3.1: ORCID Setup and Update**
Create or update your ORCID profile. Add at least one publication, dataset, or software entry and set appropriate visibility permissions.

**Activity 3.2: DOI Planning**
Choose a research output and draft a plan to mint a DOI (which repository, what metadata you will provide, and how you will cite it).

**Activity 3.3: Citation Practice**
Write citations for one dataset, one software package, and one paper using DOI-based formats. Note any differences in formatting across resource types.

**Activity 3.4: Identifier Inventory**
List the identifiers used in your lab or project (DOIs, ORCIDs, grant numbers). Identify one gap and propose how to fill it.
:::

## Lesson 4: Open Science Software Ecosystems

### Overview
In this lesson, you explore the broader ecosystem of tools used in open science beyond version control and repositories. You learn about tools for documentation, collaboration, preprint sharing, project management, and data management planning. You understand how these tools integrate to support reproducible research.

### 4.1 Documentation and Manuscript Tools

**Overleaf** ([https://www.overleaf.com/](https://www.overleaf.com/)) - Collaborative LaTeX Writing
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

**Google Docs** ([https://docs.google.com/](https://docs.google.com/)) - Cloud Collaboration
- **Purpose:** Simple collaborative writing
- **Advantages:**
  - Extremely easy to use
  - Simultaneous real-time editing
  - Comment and suggestion modes
  - Built-in version history
  - Free (Google account required)
- **Limitations:** Not ideal for formatted manuscripts
- **Best for:** Early drafts, quick collaboration, non-technical teams

**Microsoft Word** ([https://www.microsoft.com/microsoft-365/word](https://www.microsoft.com/microsoft-365/word)) with **OneDrive** ([https://onedrive.live.com/](https://onedrive.live.com/))
- **Purpose:** Familiar alternative to Google Docs
- **Features:** Co-authoring, comments, track changes
- **Best for:** Teams already in Microsoft ecosystem

**Markdown + GitHub** ([https://github.com/](https://github.com/))
- **Purpose:** Lightweight manuscript writing
- **Advantages:** Version control, plain text, reviewable diffs
- **Tools:** [https://pandoc.org/](https://pandoc.org/), [https://jupyterbook.org/](https://jupyterbook.org/), [https://quarto.org/](https://quarto.org/)
- **Best for:** Technical manuscripts, reproducible research

### 4.2 Computational Research Tools

**Jupyter Notebooks** ([https://jupyter.org/](https://jupyter.org/))
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

**Quarto** ([https://quarto.org/](https://quarto.org/))
- **What:** Scientific publishing system
- **Capabilities:**
  - Mix code and prose (Python, R, Julia, Observable)
  - Render to HTML, PDF, Word, presentations
  - Cross-references, citations, figures
  - Websites and books
- **Advantages:** More flexible than Jupyter
- **Best for:** Complete research communication

**R Markdown** ([https://rmarkdown.rstudio.com/](https://rmarkdown.rstudio.com/))
- **What:** R-specific document format
- **Creates:** PDFs, HTML, Word documents
- **Advantages:** Seamless R integration
- **Best for:** R-focused research

**Jupyter Book** ([https://jupyterbook.org/](https://jupyterbook.org/))
- **What:** Build publication-quality books from Jupyter Notebooks
- **Features:**
  - Table of contents and navigation
  - Cross-references
  - Bibliography management
  - Web hosting ready
- **Best for:** Textbooks, theses, comprehensive analyses

### 4.3 Preprint Servers

**arXiv** ([https://arxiv.org/](https://arxiv.org/)) - Multidisciplinary Preprints
- **Coverage:** Physics, astronomy, mathematics, computer science, quantitative biology
- **Volume:** 500,000+ papers annually
- **Timeline:** No peer review (moderation only)
- **Permanence:** Permanent (no deletion)
- **Discovery:** Heavily indexed by search engines
- **Best for:** Physics-heavy research

**bioRxiv** ([https://www.biorxiv.org/](https://www.biorxiv.org/)) - Biology Preprints
- **Coverage:** All biology fields
- **Volume:** 100,000+ papers annually
- **Timeline:** Typically published to journal within 6 months
- **Features:** Integrated with journal submission workflows
- **Best for:** Biological sciences

**medRxiv** ([https://www.medrxiv.org/](https://www.medrxiv.org/)) - Medicine and Health
- **Coverage:** Medicine, health sciences
- **Rapid dissemination:** Important for urgent health findings
- **COVID-19 rapid response:** Enabled pre-publication sharing
- **Best for:** Medical research

**PsyArXiv** ([https://psyarxiv.com/](https://psyarxiv.com/)) - Psychology Preprints
- **Coverage:** Psychology and related fields
- **Features:** Integrated with Open Science Framework
- **Best for:** Psychological sciences

**OSF Preprints** ([https://osf.io/preprints/](https://osf.io/preprints/)) - Multidisciplinary
- **Coverage:** All disciplines
- **Features:** Integrated with project management
- **Best for:** Researchers already using OSF

Preprints speed dissemination from months to days, establish priority before formal publication, and invite community feedback that can strengthen the final manuscript. They also increase global visibility by making results discoverable early and, in many fields, help meet funder expectations for timely sharing.

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

**GitHub Projects** ([https://github.com/features/issues](https://github.com/features/issues))
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
  - Notion ([https://www.notion.so/](https://www.notion.so/)), OneNote ([https://www.microsoft.com/microsoft-365/onenote](https://www.microsoft.com/microsoft-365/onenote)) (note-taking)
  - GitHub wikis ([https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis](https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis)) (collaborative)
  - OSF wiki ([https://help.osf.io/article/393-wiki](https://help.osf.io/article/393-wiki)) (research-specific)
- **Requirements:**
  - Dated entries
  - Experiments recorded
  - Methods documented
  - Results noted
  - Accessible to team

### 4.5 Data Management Planning

**DMPTool** ([https://dmptool.org/](https://dmptool.org/))
- **What:** Data management plan (DMP) writing assistant
- **Features:**
  - Templates for major funders (NSF, NIH, EU)
  - Question prompts with guidance
  - Institutional support integration
  - Export to PDF or funder formats
- **Pricing:** Free
- **Best for:** Grant proposals requiring DMPs

**Data Stewardship Wizard** ([https://dsw.fairdata.eu/](https://dsw.fairdata.eu/))
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

A strong data management plan outlines the data types and collection methods, storage and backup strategies, and documentation standards for data quality. It also specifies access and sharing plans, long-term archival and preservation approaches, roles and responsibilities across the team, and the budget or resources required to carry out the plan.

### 4.6 Team Communication

Effective team communication combines real-time chat for quick coordination, asynchronous channels for broader participation, and searchable archives that preserve decisions over time. Choosing tools that match team size, privacy needs, and institutional norms helps reduce miscommunication and keeps research work transparent and reproducible.

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

:::{admonition} Activities for Lesson 4
:class: activity

Complete at least two of the following activities to explore the open science software ecosystem:

**Activity 4.1: Toolchain Blueprint**
Sketch a toolchain for a real project, from planning to publication. Include at least one tool for documentation, computation, preprints, project management, and data management planning.

**Activity 4.2: Documentation Tool Trial**
Choose one documentation tool (Overleaf, Quarto, Jupyter Book, or Markdown + Git). Create a short sample document with a figure and a citation.

**Activity 4.3: Preprint Decision Memo**
Write a 200-300 word memo on whether you would post a preprint for a current project, including benefits, risks, and timing.

**Activity 4.4: DMP Mini-Plan**
Draft a one-page data management mini-plan using DMPTool or a similar template, focusing on storage, documentation, sharing, and preservation.
:::

## Lesson 5: Building Your Open Science Toolkit

### Overview
In this final lesson, you integrate the tools learned throughout this module into a practical toolkit. You learn to select appropriate tools for your research, implement them systematically, and build sustainable practices. You also explore communities, resources, and next steps for deepening your tool expertise.

### 5.1 Assessing Your Tool Needs

***Research Stage Analysis:**

![Research Stage Analysis: Tools and Workflow](../images/research_stage_analysis.svg)

### 5.2 Discipline-Specific Tool Recommendations

Research communities have evolved distinct practices and standards shaped by disciplinary norms, funding requirements, publication cultures, and data types. While core open science principles apply across fields, the specific tools you choose should reflect your discipline's expectations and your research workflow. This section outlines recommended toolchains for major disciplinary areas. Use these as starting points and adapt them based on your institution's requirements, your collaborators' expertise, and your specific research needs. Many tools work across disciplines, but disciplinary preferences and integrations can significantly improve adoption and sustainability.

**Computational Sciences** (Computer Science, Statistics, Physics)
- **Code:** **GitHub** ([https://github.com/](https://github.com/)) (essential)
- **Notebooks:** **Jupyter** ([https://jupyter.org/](https://jupyter.org/)) or **Quarto** ([https://quarto.org/](https://quarto.org/))
- **Manuscripts:** **Overleaf** ([https://www.overleaf.com/](https://www.overleaf.com/)) or Markdown + **Pandoc** ([https://pandoc.org/](https://pandoc.org/))
- **Preprints:** **arXiv** ([https://arxiv.org/](https://arxiv.org/))
- **Archival:** **Zenodo** ([https://zenodo.org/](https://zenodo.org/))
- **Data:** **Zenodo** ([https://zenodo.org/](https://zenodo.org/)) or **figshare** ([https://figshare.com/](https://figshare.com/))
- **Project mgmt:** **GitHub Projects** ([https://github.com/features/issues](https://github.com/features/issues)) or **OSF** ([https://osf.io/](https://osf.io/))

**Biological Sciences** (Biology, Medicine, Life Sciences)
- **Code:** **GitHub** ([https://github.com/](https://github.com/))
- **Manuscripts:** **Overleaf** ([https://www.overleaf.com/](https://www.overleaf.com/)) or **Microsoft Word** ([https://www.microsoft.com/microsoft-365/word](https://www.microsoft.com/microsoft-365/word))
- **Preprints:** **bioRxiv** ([https://www.biorxiv.org/](https://www.biorxiv.org/)) or **medRxiv** ([https://www.medrxiv.org/](https://www.medrxiv.org/))
- **Data:** **Zenodo** ([https://zenodo.org/](https://zenodo.org/)), **Figshare** ([https://figshare.com/](https://figshare.com/)), **Dryad** ([https://datadryad.org/](https://datadryad.org/)), or domain-specific repositories
- **Samples/sequences:** **GenBank** ([https://www.ncbi.nlm.nih.gov/genbank/](https://www.ncbi.nlm.nih.gov/genbank/)), **PDB** ([https://www.rcsb.org/](https://www.rcsb.org/))
- **Project mgmt:** **OSF** ([https://osf.io/](https://osf.io/)) (for workflows), **GitHub** ([https://github.com/](https://github.com/))

**Social Sciences** (Psychology, Economics, Sociology)
- **Code:** **GitHub** ([https://github.com/](https://github.com/)) or **OSF** ([https://osf.io/](https://osf.io/)) repository
- **Preregistration:** **OSF** ([https://osf.io/](https://osf.io/)) (strongly recommended)
- **Data:** **OSF** ([https://osf.io/](https://osf.io/)), **Zenodo** ([https://zenodo.org/](https://zenodo.org/)), **Figshare** ([https://figshare.com/](https://figshare.com/)) (sensitivity)
- **Manuscripts:** **Google Docs** ([https://docs.google.com/](https://docs.google.com/)) or **Overleaf** ([https://www.overleaf.com/](https://www.overleaf.com/))
- **Project mgmt:** **Open Science Framework** ([https://osf.io/](https://osf.io/))

**Environmental Sciences** (Ecology, Climate, Geology)
- **Data:** Discipline-specific (**NOAA** ([https://www.noaa.gov/](https://www.noaa.gov/)), **USGS** ([https://www.usgs.gov/](https://www.usgs.gov/))) or **Zenodo** ([https://zenodo.org/](https://zenodo.org/))
- **Code:** **GitHub** ([https://github.com/](https://github.com/))
- **Notebooks:** **Jupyter** ([https://jupyter.org/](https://jupyter.org/)) for analysis documentation
- **Preprints:** **EarthArXiv** ([https://eartharxiv.org/](https://eartharxiv.org/))
- **Data access:** Domain repositories essential

**Humanities** (History, Literature, Languages)
- **Repositories:** Institutional repositories, digital humanities platforms
- **Manuscripts:** **Google Docs** ([https://docs.google.com/](https://docs.google.com/)), **Markdown** + **GitHub** ([https://github.com/](https://github.com/))
- **Data:** **Zenodo** ([https://zenodo.org/](https://zenodo.org/)) for primary sources
- **Version control:** **Git** + **GitHub** ([https://github.com/](https://github.com/)) for collaborative projects
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

Learning open science tools is easier and more sustainable within communities of practice. These groups offer workshops, documentation, peer support, and shared resources that accelerate skill development and help you troubleshoot challenges. Communities also keep you informed about tool updates, emerging best practices, and new features. Whether you're just starting or deepening your expertise, connecting with others using the same tools transforms your experience from isolated learning to collaborative growth. Below are major communities organized by focus area, along with ways to get involved.

**Software Carpentry / The Carpentries** ([https://carpentries.org/](https://carpentries.org/))
- **Focus:** Teaching open science skills
- **Specialties:** Git, data management, research software
- **Format:** Free 2-day workshops
- **Website:** [https://carpentries.org/](https://carpentries.org/)
- **How to join:** Register for local workshop or teach

**rOpenSci** ([https://ropensci.org/](https://ropensci.org/)) / **PyOpenSci** ([https://www.pyopensci.org/](https://www.pyopensci.org/))
- **Focus:** Open source tools for research
- **Specialties:** R/Python packages, code review
- **Activities:** Collaborative development, peer review
- **Websites:** [https://ropensci.org/](https://ropensci.org/), [https://www.pyopensci.org/](https://www.pyopensci.org/)

**Research Software Engineering (RSE) Communities**
- **US-RSE:** [https://us-rse.org/](https://us-rse.org/)
- **International-RSE:** [https://researchsoftware.org/](https://researchsoftware.org/)
- **Focus:** Professional development for research software

**Repository-Specific Communities**
- **Zenodo:** [https://zenodo.org/communities/](https://zenodo.org/communities/) (Zenodo users community)
- **GitHub:** [https://github.community/](https://github.community/) (GitHub Community Forum)
- **OSF:** [https://osf.io/support/](https://osf.io/support/) (Open Science Framework community)

**Tool-Specific Resources**
- **Git:** [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2) (Pro Git book, free), [https://www.atlassian.com/git/tutorials](https://www.atlassian.com/git/tutorials) (Atlassian tutorials)
- **Jupyter:** [https://jupyter.org/community](https://jupyter.org/community) (Jupyter community), [https://jupyterhub.readthedocs.io/](https://jupyterhub.readthedocs.io/) (JupyterHub documentation)
- **Quarto:** [https://quarto.org/docs/resources/](https://quarto.org/docs/resources/) (Quarto documentation and forum)

### 5.6 Troubleshooting Common Tool Issues

> **Problem: "I'm using too many tools"**
> 
> - Solution: Consolidate where possible (e.g., GitHub for both code and project management)
> - Reality: Most researchers use 3-5 core tools
> - Approach: Start minimal, add tools as needed

> **Problem: "My institution doesn't support these tools"**
> 
> - Solution: Use cloud-based alternatives (GitHub, Zenodo, Google Docs)
> - Advocate: Request institutional support or training
> - Bridge: Use free options while advocating

> **Problem: "My collaborators don't know these tools"**
> 
> - Solution: Provide training or pair programming
> - Resources: The Carpentries workshops
> - Phased approach: Learn together incrementally

> **Problem: "These tools feel overwhelming"**
> 
> - Solution: Start with one tool well (usually Git)
> - Timeframe: 3-6 months to become comfortable
> - Support: Find local experts or mentors
> - Reality: Tools improve workflow significantly after learning curve

### 5.7 Your Open Science Toolkit Checklist

Building an open science toolkit is a gradual process, not an all-at-once migration. The checklist below organizes tools by adoption stage and use case, helping you prioritize what to implement first and when to add additional capabilities. Start with the essential tools—these form the foundation and address the most common research needs. Then progress through highly recommended and project management tools as you grow comfortable with the basics. Remember that this is a personalized toolkit; you may not need every item, and you may add tools specific to your discipline or institution. Use this checklist as a planning guide rather than a rigid requirement, adapting it to your research context and goals.

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

Measuring success with open science tools means tracking three interconnected dimensions: adoption, process, and impact.

**Tool Adoption** demonstrates whether your toolkit is becoming integrated into your workflow. Consistency—measured by regular commits, updates, and active use—shows that tools are becoming habitual rather than burdensome. Discoverability indicates that your work is being found; tracking how often your DOI is cited in publications reflects whether others are discovering and using your outputs. Collaboration metrics like pull requests and contributions reveal whether your open practices are attracting co-workers and peer engagement. Finally, citation metrics from services like Altmetric and your ORCID profile aggregate signals of your research's reach and influence.

**Process Improvements** capture how tools change your day-to-day research work. You may find time savings through the reuse of well-documented code and existing workflows, reducing the need to rebuild analyses from scratch. Reproducibility becomes verifiable when others use your tools or data and independently confirm your results, validating your documentation and methods. Efficiency gains accumulate through automation—version control branches, CI/CD pipelines, and preregistration templates all reduce manual steps. Team alignment improves when tools create shared project spaces and searchable records, reducing miscommunication and duplicate effort.

**Research Impact** captures the ultimate benefit of open science tools: increased visibility, collaboration, and funding success. Citations to your work—tracked through DOI resolution and ORCID profiles—demonstrate recognition of your contributions. The reuse of your code and data by other researchers extends the value of your work beyond your own projects and supports the broader mission of open science. Visible, well-documented work creates collaboration opportunities as other researchers discover your expertise and approach you for partnerships. Finally, open science practices are increasingly valued by funders, who recognize that transparency, reproducibility, and broad dissemination advance science more effectively than closed practices.

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

:::{admonition} Activities for Lesson 5
:class: activity

Complete at least one of the following activities to build your personal toolkit:

**Activity 5.1: Toolkit Audit and Upgrade**
List the tools you currently use for planning, coding, documentation, sharing, and preservation. Identify two gaps and create a 30-day plan to fill them.

**Activity 5.2: Sustainable Workflow Plan**
Create a workflow checklist you will reuse for every project (e.g., ORCID update, repository setup, README, data archiving, DOI minting). Share it with your team.

**Activity 5.3: Community Engagement**
Join one community (The Carpentries, rOpenSci, RSE, or a discipline-specific group). Attend one meeting or complete one training and summarize what you learned.

**Activity 5.4: Publish a Minimal Example**
Publish a small code or data artifact with documentation and a clear license. If possible, archive a release in Zenodo to obtain a DOI.
:::

