# Module 3 - Open Software

## Introduction

Open software and code are critical components of open science research. This module explores the principles of open software development, assessment criteria, documentation standards, licensing frameworks, and practical implementation strategies for creating and maintaining research software.

## Learning Objectives

After completing this module, you should be able to:
- Define research software and understand its spectrum from scripts to professional packages, as well as the software development lifecycle specific to research contexts.
- Discover, evaluate, and assess open research software for functionality, usability, reliability, and performance before integrating it into your research.
- Write high-quality, well-documented, and maintainable research code following best practices for readability, style, documentation, and testing.
- Apply appropriate open source licenses to research software, prepare code for sharing, and understand how to make software discoverable and citable.
- Develop comprehensive strategies for creating and maintaining sustainable research software with community engagement and long-term preservation.

---

## Lesson 1: Understanding Research Software

### Overview
In this lesson, you explore what research software is, the different types of software used in science, the software development lifecycle, and the benefits of developing open software. You understand how research software differs from commercial software and why open practices are essential for reproducible science.

### 1.1 What is Research Software?

**Definition:** Research software is any code or software tool created to support research activities, including analysis, simulation, data processing, visualization, and instrument control.

**Key Characteristics:**
- **Purpose-driven:** Built to answer research questions
- **Evolving:** Changes as research progresses
- **Unique:** Often specialized for specific projects
- **Complex:** May involve sophisticated algorithms
- **Critical:** Results depend on software correctness

**Scale of Research Software:**
- **Scripts:** Single-file analyses (50-200 lines)
- **Tools:** Multi-file projects (1,000-10,000 lines)
- **Packages:** Distributable software (10,000+ lines)
- **Platforms:** Large systems (100,000+ lines)

**Examples Across Disciplines:**
- **Genomics:** BLAST (sequence analysis), Samtools (BAM processing)
- **Physics:** Geant4 (particle simulation), OpenFOAM (fluid dynamics)
- **Climate:** GROMACS (molecular dynamics), WRF (weather research)
- **Astronomy:** Astropy (data processing), Galsim (simulation)
- **Social Science:** Stan (statistical inference), EggNOG (sequence annotation)

### 1.2 From Code to Software: The Spectrum

**Research Script** (Minimal)
```python
# One-off analysis for a specific dataset
import pandas as pd
data = pd.read_csv('experiment.csv')
results = data[data['valid'] == True].mean()
print(results)
```
**Characteristics:** Quick, specific, minimal documentation
**Problem:** Hard to reuse, hard to maintain

**Research Tool** (Moderate)
```python
# Reusable but limited to specific domain/task
# - Function definitions
# - Some documentation
# - Basic examples
# - Single file or simple structure
```
**Characteristics:** Better organized, documented, reusable
**Use:** Specific analyses, specialized tasks

**Research Package** (Professional)
```python
# Distributable, documented, tested
# - Multiple files/modules
# - Comprehensive documentation
# - Test suite
# - CI/CD pipeline
# - Version management
# - Package registration (PyPI/CRAN)
```
**Characteristics:** Production-quality, maintained, discoverable
**Use:** Widespread community use

### 1.3 Types of Research Software

**General Purpose Programming Languages**
- **[Python](https://www.python.org/):** Most popular (data science, machine learning, general)
- **[R](https://www.r-project.org/):** Statistics and visualization
- **[Julia](https://julialang.org/):** Scientific computing and numerical analysis
- **C/C++:** High-performance computing
- **[Fortran](https://gcc.gnu.org/fortran/):** Legacy scientific computing
- **[MATLAB](https://www.mathworks.com/products/matlab.html):** Engineering and signal processing

**Domain-Specific Software:**

**Molecular Dynamics:**
- [GROMACS](https://www.gromacs.org/), [AMBER](https://ambermd.org/), [LAMMPS](https://www.lammps.org/), [NAMD](https://www.ks.uiuc.edu/Research/namd/)

**Structural Biology:**
- [PYMOL](https://pymol.org/), [VMD](https://www.ks.uiuc.edu/Research/vmd/), [Chimera](https://www.cgl.ucsf.edu/chimera/)

**Quantum Chemistry:**
- [GAUSSIAN](https://gaussian.com/), [ORCA](https://www.factsci.com/orca), [MOPAC](https://www.semi-empirical.com/)

**Climate/Weather:**
- [WRF](https://www.mmm.ucar.edu/models/wrf), [CESM](https://www.cesm.ucar.edu/), [GFDL models](https://www.gfdl.noaa.gov/)

**Astronomy/Astrophysics:**
- [Astropy](https://www.astropy.org/), [IRAF](https://iraf.noaa.gov/), [SDSS software](https://www.sdss.org/)

**Machine Learning:**
- [TensorFlow](https://www.tensorflow.org/), [PyTorch](https://pytorch.org/), [Scikit-learn](https://scikit-learn.org/)

**Genomics:**
- [BLAST](https://blast.ncbi.nlm.nih.gov/), [Bowtie](https://bowtie-bio.sourceforge.net/), [GATK](https://gatk.broadinstitute.org/), [Samtools](http://samtools.sourceforge.net/)

### 1.4 The Software Development Lifecycle for Research

```{image} ../images/sdlc_diagram.svg
:alt: Software Development Lifecycle for Research
:width: 100%
```

### 1.5 Benefits of Open Research Software

The benefits of open research software extend far beyond individual developers to transform entire fields and society. When you share your code openly, you unlock immediate personal advantages: research papers with open code receive 20-30% more citations, visible code attracts collaborators who build on your work, and you gain recognition as an open science leader. Beyond personal benefits, the research community gains tremendously—others can verify your results through reproducible code, avoiding the wasteful duplication of development efforts that plague closed-source approaches. As researchers build upon each other's openly available code, community standards emerge naturally, sparks of innovation ignite from unexpected combinations of existing tools, and future researchers learn best practices through studying well-written, open implementations. Open source experience has also become increasingly valued in the job market, creating tangible career advantages.

At a broader scale, open research software benefits all of science and society. Transparency enables scientific scrutiny and catches errors early through peer review and community feedback, while global access to research tools breaks down barriers created by proprietary software—ensuring that researchers in under-resourced regions can participate fully in advancing knowledge. The efficiency gains are enormous: rather than thousands of researchers independently solving identical problems, communities can collectively improve shared tools, multiplying research output across fields. Open software fundamentally democratizes research by making powerful computational tools available regardless of funding or institutional affiliation, accelerating discovery and enabling innovations that might never occur under proprietary lock-in. Ultimately, better tools created through open collaboration improve research quality across every scientific discipline, generating impact that benefits not just science but society as a whole through better solutions to critical problems.

### 1.6 Challenges and Misconceptions

**"My code is too messy/incomplete to share"**
- Reality: Shared code is always improved
- Solution: Share at any stage, document limitations
- Truth: Perfectionism delays sharing and reduces impact

**"I don't have time to document"**
- Reality: Documentation saves time long-term (even for you)
- Solution: Document as you develop, not after
- Truth: Every project benefits from future documentation

**"Others will scoop my ideas"**
- Reality: Publication date (preprint) establishes priority
- Solution: Open code + preprint = clear priority
- Truth: Collaborations often more valuable than competition

**"My code is too specific"**
- Reality: Others have similar problems
- Solution: Share anyway, reusability improves with use
- Truth: Code often finds applications beyond original intent

**"I don't know how to license it"**
- Reality: Choose MIT (permissive) or GPL (copyleft)
- Solution: License matters less than being open
- Truth: Licensing framework prevents legal uncertainty

### 1.7 Software Development Models

**Waterfall Model** (Traditional)
- Plan → Design → Code → Test → Release
- Issues: Inflexible, long cycles
- When useful: Large projects with clear requirements

**Agile Model** (Modern)
- Iterative: Short cycles of plan-code-test-review
- Advantages: Flexible, responds to feedback
- Common in: Open source, rapidly evolving projects

**Research Software Model** (Hybrid)
- Start: Script/prototype with minimal process
- Middle: Add structure as reuse becomes clear
- Mature: Professional processes if community adoption
- Reality: Most research software evolves naturally

### Summary

Research software is essential infrastructure:
- **Spectrum:** From scripts to professional packages
- **Diversity:** Domain-specific and general-purpose tools
- **Lifecycle:** Evolves from prototype to mature product
- **Benefits:** Impact multiplies through openness
- **Challenges:** Manageable with planning and community support
- **Future:** Open software is becoming standard practice

:::{admonition} Activities for Lesson 1
:class: activity

Complete at least two of the following activities to understand research software:

**Activity 1.1: Software Spectrum Assessment**
Examine a research project you know (yours or published). Classify its software on the spectrum:
- Where does it fall: Script → Tool → Package → Platform?
- What is the current stage of the lifecycle: Prototype → Evolving → Mature?
- What would be required to move it to the next level?
- What benefits and costs would that entail?

Write 200-300 words reflecting on this classification and what stage is appropriate for your project.

**Activity 1.2: Explore Research Software in Your Field**
Research three significant research software projects in your discipline:
- What problem does each solve?
- What is the development status (active/maintained/archived)?
- How is it distributed (GitHub, package registry, standalone)?
- What is the user base/impact?
- What documentation exists?

Create a table comparing these projects and identify best practices from the most successful one.

**Activity 1.3: Understand Software Lifecycle**
Choose one open research software project. Document:
- Initial problem it solved
- How it has evolved over time
- Current features and capabilities
- Community involvement (if any)
- Future direction (if documented)

Reflect on factors that contributed to its success or challenges.

**Deliverable:** Your choice of analysis from activities above (1-2 pages total).
:::

## Lesson 2: Assessing and Using Open Software

### Overview
In this lesson, you learn how to evaluate research software for quality and reliability, understand criteria for assessing software for your own use, discover how to find and evaluate open software, and practice critical assessment of research tools.

### 2.1 Where to Find Research Software

**Software Discovery Sources:**

**General Repositories:**
- **[GitHub](https://github.com/):** 100+ million repositories, search by language/topic
- **[GitLab](https://about.gitlab.com/):** Similar to GitHub, often with institutional options
- **[SourceForge](https://sourceforge.net/):** Historical, older projects

**Package Repositories:**
- **[PyPI](https://pypi.org/)** (Python): 500,000+ packages, `pip search` or web search
- **[CRAN](https://cran.r-project.org/)** (R): 20,000+ packages with searchable interface
- **[Bioconductor](https://www.bioconductor.org/):** 2,000+ biology packages
- **[npm](https://www.npmjs.com/)** (JavaScript): 3 million+ packages
- **[Maven Central](https://mvnrepository.com/)** (Java): 500,000+ artifacts

**Domain-Specific Registries:**
- **[Bio.Tools](https://bio.tools/):** 15,000+ bioinformatics tools with annotations
- **[Conda-Forge](https://conda-forge.org/):** 25,000+ scientific packages
- **[Galaxy Tools](https://toolshed.g2.bx.psu.edu/):** 10,000+ bioinformatics tools
- **[Biohackathon Projects](https://biohackathon.org/):** Collaborative research tools

**Academic Databases:**
- **[SciCrunch](https://scicrunch.org/):** Research tools with detailed metadata
- **[OMICtools](https://www.omictools.com/):** Bioinformatics tool directory
- **[Google Scholar](https://scholar.google.com/):** Search for software papers
- **Journal supplements:** Tools described in publications

**Community Resources:**
- **[rOpenSci](https://ropensci.org/)/[PyOpenSci](https://www.pyopensci.org/):** Curated, peer-reviewed packages
- **[Carpentries](https://carpentries.org/):** Training materials mentioning tools
- **Research communities:** Reddit r/bioinformatics, etc.
- **Twitter/Mastodon:** Follow developers in your field

### 2.2 Criteria for Assessing Software Quality

**Functionality Assessment**

**Does it solve your problem?**
- Read documentation (README, tutorial)
- Check if output matches your expected format
- Look for papers describing the tool
- Try on small test dataset first

**Handling of edge cases:**
- Empty input
- Very large data
- Missing data/parameters
- Invalid input
- Look for error messages and documentation

**Scientific validity:**
- Is the algorithm correctly implemented?
- Check for published validation studies
- Compare against known reference
- Verify on your data

**Usability Assessment**

**Documentation quality:**
```
Good Documentation:
✓ Clear README (one page overview)
✓ Installation instructions
✓ Quick start example
✓ Complete API documentation
✓ Troubleshooting guide
✓ Examples with expected outputs

Poor Documentation:
✗ "Just read the code"
✗ Outdated examples
✗ Missing parameter descriptions
✗ No error explanations
```

**Ease of installation:**
- Automatic package managers (pip, conda) best
- Source compilation acceptable if documented
- Container (Docker) excellent alternative
- No documentation of dependencies: red flag

**User interface:**
- Command-line tools: clear help/usage text
- GUI: intuitive navigation
- Python library: sensible function names and parameters
- R package: follows tidyverse conventions

**Reliability Assessment**

**Maintenance status:**
```
✓ Active (commits within last month)
✓ Stable (no recent major changes)
✓ Responsive (issues replied to within weeks)

⚠ Dormant (last commit 6-12 months ago)
⚠ Slow responses (issues unanswered for months)

✗ Abandoned (no updates in years)
✗ No issue tracking
```

**Community indicators:**
- GitHub stars: 100+ indicates meaningful use
- Citation count: How many papers cite this tool?
- Forks: Are people building on it?
- Issue responses: Do developers engage?
- Contributor count: Single developer more risk

**Testing and quality:**
- Unit tests present? Good sign
- Continuous integration (CI)? Shows quality care
- Code coverage reported? Standard in good projects
- Static analysis? Shows attention to quality

**Bug tracking:**
- Open issues: Indicates active development
- Closed issues: Shows bugs get fixed
- Old unresolved issues: Concern if critical

**Performance Assessment**

**Computational requirements:**
- Memory: Check documentation or paper
- Runtime: Try on your data
- CPU cores: Can it parallelize?
- Disk space: Output file sizes?

**Scalability:**
- Tested on your data size?
- Does performance degrade with size?
- Are there benchmarks published?
- Can you test on subset first?

**Optimization:**
- Written in compiled language (C, Rust)? Fast
- Python/R with vectorization? Acceptable
- Interpreted without optimization? Slow
- Can you parallelize? Important for big data

### 2.3 Critical Questions Checklist

**Before Adopting Software:**

```
Functionality
☐ Does it solve my exact problem?
☐ Can I reproduce published results?
☐ Are there known limitations I can live with?

Usability
☐ Is installation straightforward?
☐ Is documentation clear and complete?
☐ Are there working examples for my use case?
☐ How long is the learning curve?

Reliability
☐ Is it actively maintained?
☐ How responsive are developers to issues?
☐ Are there tests and CI?
☐ What's the track record (citations, longevity)?

Performance
☐ Will it run on my data/hardware?
☐ What are memory/time requirements?
☐ Have I tested on small data first?

License and Attribution
☐ Is there a clear license?
☐ Can I use it for my purpose?
☐ What's the citation requirement?

Support
☐ Active user community?
☐ Issues get responses?
☐ Forum or discussion list?
☐ Could I adapt if unmaintained?
```

### 2.4 Testing and Validating

**Before Using in Publication:**

**Phase 1: Smoke Test (1 hour)**
- Install successfully
- Run simple example
- Get reasonable output
- Decision: Keep exploring or try alternative

**Phase 2: Data Validation (1-2 days)**
- Run on small subset of your data
- Verify output format
- Check numerical ranges make sense
- Try known comparison (if available)

**Phase 3: Deep Testing (1-2 weeks)**
- Full run on all data
- Sensitivity analysis (vary parameters)
- Compare against alternative tools
- Document methods and choices

**Phase 4: Verification (ongoing)**
- Keep installation documented
- Note version used
- Save exact command used
- Document any modifications
- Plan for future reproduction

### 2.5 Red Flags and Deal-Breakers

**Deal-Breaker Red Flags:**
```
✗ No license specified
✗ No documentation at all
✗ Last update more than 5+ years ago (for maintained software)
✗ Cannot run your data
✗ Results don't match published validation
✗ Required closed-source component
✗ Requires proprietary software
```

**Caution Flags:**
```
⚠ Minimal documentation
⚠ Single maintainer
⚠ Few users or citations
⚠ No tests visible
⚠ Complex installation
⚠ Very recent (unproven)
⚠ Unclear or restrictive license
```

**Manageable Concerns:**
```
○ Steep learning curve (spend time learning)
○ Missing feature you need (fork/adapt or request)
○ Slow on large data (parallelize or optimize)
○ Needs old dependency (use container)
```

### Summary

Assessing research software requires systematic evaluation:
- **Discovery:** Use repositories and domain resources
- **Functionality:** Verify it solves your problem
- **Usability:** Good documentation and easy use
- **Reliability:** Active maintenance and responsive developers
- **Performance:** Can handle your data scale
- **Testing:** Always validate before publication
- **Red flags:** Know when to choose alternatives

:::{admonition} Activities for Lesson 2
:class: activity

Complete at least two of the following activities to practice finding and evaluating open software:

**Activity 2.1: Discover Research Software**
Search for software in your field using multiple discovery methods:
- Method 1: Search a package registry (PyPI, CRAN, npm)
- Method 2: Search GitHub by topic/language
- Method 3: Search domain-specific repositories or software lists
- Method 4: Ask colleagues or check papers for software recommendations

For each software found, document:
- Name and description
- Discovery method used
- Primary use case
- Developer/maintainer information

Write 150-200 words comparing the discovery experience across methods.

**Activity 2.2: Complete Software Assessment Checklist**
Select one research software tool you found in Activity 2.1. Complete a comprehensive assessment:
- **Functionality:** Does it solve your problem? How well?
- **Usability:** Is it easy to install? Clear documentation? Working examples?
- **Reliability:** Is it actively maintained? How responsive are developers?
- **Performance:** Does it handle your data scale? Any benchmarks available?
- **Quality:** Tests? CI/CD? Code coverage?
- **License:** Clear and permissive?
- **Community:** Active users? Support channels?

Write 300-400 words summarizing your assessment and recommending use/alternative.

**Activity 2.3: Test Software Before Using in Publication**
Set up and test a piece of research software:
- Install following documentation
- Run example/tutorial
- Test on your data (small subset first)
- Verify output makes sense
- Document installation issues (if any)
- Note version and dependencies used

Write a brief testing report (150-200 words) describing what you verified and any concerns.

**Deliverable:** Your choice of output from activities above (1-2 pages total).
:::

## Lesson 3: Writing and Documenting Research Code

### Overview
In this lesson, you learn principles of writing good research code, comprehensive documentation practices, making code reproducible and maintainable, testing strategies, and code quality best practices. You practice documentation standards and learn how to make your code accessible to others and to your future self.

### 3.1 Code Quality Principles

**FAIR Software Principles** (Similar to FAIR Data)

**Findable**
- Public repository (GitHub, GitLab)
- Discoverable (PyPI, CRAN registration)
- Named clearly
- Documented in README

**Accessible**
- Open license
- No paywalls
- Easy installation
- Clear dependencies

**Interoperable**
- Standard formats for input/output
- Follows conventions
- Integrates with other tools
- Uses standard libraries

**Reusable**
- Clear documentation
- Tests included
- Modular design
- Permissive license

### 3.2 Code Style and Readability

**Why Style Matters:**
- Code read 10x more than written
- Enables collaboration
- Reduces bugs
- Makes maintenance easier

**Language-Specific Style Guides:**

**Python:** PEP 8 (Python Enhancement Proposal 8)
```python
# Good: Clear names, proper spacing
def calculate_mean_intensity(image_array, threshold=0):
    """Calculate mean intensity above threshold."""
    valid_pixels = image_array[image_array > threshold]
    return valid_pixels.mean()

# Bad: Cryptic names, poor spacing
def cm(i):
    v=i[i>0]
    return v.mean()
```

**R:** tidyverse style guide
```r
# Good: Snake_case, clear names
calculate_gene_expression <- function(reads, min_count = 10) {
  expressed <- reads[rowSums(reads) > min_count, ]
  return(expressed)
}

# Bad: camelCase inconsistency
calculateGeneExpr <- function(r, m=10) {
  e = r[rowSums(r)>m,]
  return(e)
}
```

**Automated Tools:**
- **Python:** Black (formatter), Pylint (linter), Flake8
- **R:** styler (formatter), lintr (linter)
- **JavaScript:** Prettier (formatter), ESLint (linter)
- **Java:** Checkstyle, IntelliJ formatter

**Benefits of Consistent Style:**
- Easier code review
- Fewer style debates
- Automated checking (CI/CD)
- Professional appearance

### 3.3 Documentation Levels

**Level 1: Code Comments**

**Inline Comments** - Explain "why" not "what"
```python
# Bad: Explains what code does (obvious)
n = len(data)  # Get length

# Good: Explains why
# Window size chosen empirically; affects memory ~5GB per 1000
window_size = 1000
```

**Function Docstrings** - Interface documentation
```python
def align_sequences(seq1, seq2, gap_penalty=-2):
    """
    Perform Needleman-Wunsch global sequence alignment.
    
    Parameters
    ----------
    seq1 : str
        First DNA sequence
    seq2 : str
        Second DNA sequence
    gap_penalty : int, optional
        Cost of insertion/deletion (default: -2)
    
    Returns
    -------
    tuple
        (alignment1, alignment2, score)
    
    Notes
    -----
    Uses BLOSUM62 matrix for scoring.
    
    References
    ----------
    Needleman SB, Wunsch CD (1970). General method applicable...
    """
```

**Level 2: README Files**

**Essential README Contents:**
```markdown
# Project Name

## Description
One sentence explaining what it does.

## Installation
Quick installation instructions.

## Quick Start
Simplest possible example:
```

**Example of good README:**
```markdown
# Genomic Alignment Tool

Fast sequence alignment for genomics research.

## Installation
```bash
pip install genomic-align
```

## Quick Start
```python
from genomic_align import align
result = align('ATCG', 'ATGG')
print(result.score)  # 3
```

## Documentation

### 3.4 Complete Documentation Structure

**README.md** (Home page)
- Title and brief description
- Installation instructions
- Quick start example
- Links to documentation
- Citation information
- License

**INSTALLATION.md** (Detailed setup)
- System requirements (OS, Python version)
- Step-by-step instructions
- Troubleshooting common issues
- Verification steps

**GETTING_STARTED.md** (Tutorials)
- Basic example
- Common use cases
- Screenshots or output
- Links to advanced docs

**API_DOCUMENTATION.md or hosted docs**
- Function/class reference
- Parameter descriptions
- Return types and examples
- Common errors and solutions

**EXAMPLES/** (directory)
- Sample code files
- Expected output
- Real-world use cases
- Different problem sizes

**CONTRIBUTING.md** (For collaborators)
- How to report bugs
- How to suggest features
- Development setup
- Code style guidelines
- Testing requirements
- Pull request process

**CHANGELOG.md** (Version history)
- What changed in each version
- Breaking changes highlighted
- Migration guides
- Links to releases

### 3.5 Making Code Reproducible

**Reproducibility Checklist:**

**Data Input**
```
☐ Document data format (CSV, HDF5, NetCDF, etc.)
☐ Show example data structure
☐ Document expected values/ranges
☐ Handle missing values explicitly
☐ Validate input data
```

**Parameter Documentation**
```
☐ List all parameters with defaults
☐ Explain what each does
☐ Document valid ranges
☐ Show effect of parameter changes
☐ Note computational impact
```

**Output Documentation**
```
☐ Document output format
☐ Explain each output field
☐ Show example output
☐ Document expected ranges
☐ Explain what to expect with your data
```

**Environment Documentation**
```
☐ List all dependencies with versions
☐ Document OS requirements
☐ Note hardware requirements (RAM, GPU)
☐ Specify compiler versions if applicable
☐ Provide environment file (environment.yml or requirements.txt)
```

**Execution Documentation**
```
☐ Exact command line to reproduce example
☐ Expected runtime
☐ Expected output/error messages
☐ Machine specification (for benchmarking)
```

### 3.6 Code Testing

**Types of Tests:**

**Unit Tests** - Test individual functions
```python
import pytest

def calculate_gc_content(dna_sequence):
    return dna_sequence.count('GC') / len(dna_sequence)

def test_gc_content():
    assert calculate_gc_content('ATGC') == 0.5
    assert calculate_gc_content('GGCC') == 1.0
    assert calculate_gc_content('ATAT') == 0.0
```

**Integration Tests** - Test components together
```python
def test_alignment_pipeline():
    # Read sequences
    seq1 = read_fasta('test1.fasta')
    # Run alignment
    result = align(seq1, reference)
    # Check output format
    assert result.has_valid_format()
```

**Regression Tests** - Ensure consistency
```python
def test_known_results():
    """Verify against published benchmark."""
    result = analyze(published_data)
    expected_output = 42.5
    assert abs(result - expected_output) < 0.001
```

**How Much Testing?**
- Research code: 30-50% coverage (critical functions)
- Distributed packages: 70-80% coverage
- Tools: 80%+ coverage

### 3.7 Continuous Integration

**GitHub Actions Example:**
```yaml
name: Tests
on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-python@v2
        with:
          python-version: 3.9
      - run: pip install -r requirements.txt
      - run: pytest
      - run: flake8
```

**Benefits:**
- Code automatically tested on each push
- Catch bugs before merging
- Ensure code quality
- Multiple Python/OS versions

### Summary

Good code and documentation enable reuse:
- **Style:** Consistent, readable code
- **Comments:** Explain "why" not "what"
- **Docstrings:** Document functions and classes
- **README:** Clear overview and quick start
- **Complete docs:** Installation, tutorials, API reference
- **Testing:** Unit, integration, and regression tests
- **Automation:** CI/CD checks quality
- **Reproducibility:** Document data, parameters, outputs, environment

:::{admonition} Activities for Lesson 3
:class: activity

Complete at least two of the following activities to practice writing quality research code:

**Activity 3.1: Code Quality Assessment**
Select a piece of your research code (script, function, or small project). Assess it against quality standards:
- **Readability:** Would a colleague understand this code?
- **Style:** Does it follow language conventions (PEP 8, style guides)?
- **Comments:** Are complex sections explained?
- **Functions:** Is it well-organized into functions?
- **Testing:** Are there tests?
- **Documentation:** Is there a README? Function documentation?
- **Version control:** Is it in Git with meaningful commits?

Create an improvement plan addressing gaps. Implement at least 3 improvements.

**Activity 3.2: Write Comprehensive Documentation**
For a research script or small project, create complete documentation:
- **README:** Overview, quick start, installation
- **Docstrings:** Document all functions with inputs/outputs
- **Comments:** Explain non-obvious logic
- **Examples:** Usage examples showing typical workflows
- **Troubleshooting:** Common issues and solutions
- **Contributing:** How others can contribute (if applicable)

Make documentation clear enough that someone could use your code without asking.

**Activity 3.3: Create Tests for Your Code**
Write tests for a research function or script:
- **Unit tests:** Test individual functions
- **Integration tests:** Test functions working together
- **Known data tests:** Test against data with known outputs
- **Edge cases:** Test boundary conditions

Aim for at least 5 tests covering main functionality. Document what each test verifies.

**Deliverable:** Your choice of output from activities above (2-3 pages total).
:::

## Lesson 4: Licensing and Sharing Software

### Overview
In this lesson, you understand intellectual property rights for software, explore open source licenses, learn to choose appropriate licenses, practice licensing your software, and understand the implications for sharing and reuse.

### 4.1 Software Intellectual Property

**What is Protected?**

**Copyright (Automatic):** Copyright applies to original code automatically the moment you write it, protecting your written work without any registration required. However, copyright does NOT automatically imply permission for others to use your code—the default is "all rights reserved," meaning others cannot legally copy, modify, or redistribute your work without explicit permission. This is why licensing matters: without a license, your code is locked down by default, even if you intended it to be open.

**Patents (Registered):** Patents protect novel algorithms or methods but require formal registration and are expensive and time-consuming to obtain and defend. Patents are less common in academic research than copyright, but they can significantly restrict reuse if someone has patented a key algorithmic approach your code implements. This is why some researchers worry about using or creating certain types of software—hidden patents can create legal liability.

**Trade Secrets (Confidential):** Trade secrets protect proprietary information through secrecy and confidentiality agreements, requiring organizations to take active steps to keep information confidential. Trade secrets are fundamentally incompatible with open source, since sharing code publicly destroys the secrecy that protects the trade secret status. This protection mechanism only works in closed, proprietary environments.

**Licenses (Explicit Permission):** Licenses solve the copyright problem by explicitly granting specific permissions—telling others what they CAN do with your code. Licenses define conditions for use and can range from very permissive (allowing almost any use) to highly restrictive (limiting use to specific purposes). Licenses are absolutely essential for open source, as they transform code from "locked down by default" into "open with clear rules." Without a license, there is no legal framework for sharing; with a license, sharing becomes both possible and predictable.

### 4.2 Open Source Licenses Explained

**The Permission Problem:**
```
Without License:
You create code → It's copyrighted by you → 
Others cannot:
  ✗ Copy it
  ✗ Modify it
  ✗ Share it
  ✗ Use it

With License:
You create code → Apply license → 
Others can (as permitted):
  ✓ Use it
  ✓ Copy it
  ✓ Modify it
  ✓ Redistribute it
(As long as they follow license terms)
```

**Categories of Open Licenses:**

**Permissive Licenses** (Very open)
- Allow almost any use
- Minimal restrictions
- Popular in research
- Examples: MIT, Apache, BSD

**Copyleft Licenses** (Share-alike)
- Require modified versions be open too
- Ensure freedom propagates
- Stronger copyleft: Stronger requirement
- Examples: GPL, AGPL

**Proprietary Licenses** (Closed)
- Restrict use to specific purposes
- Not open source
- Common in commercial software

### 4.3 Common Licenses for Research

**MIT License** (Simplest, Most Popular)
```
Key Points:
✓ Very permissive
✓ Short and simple (3 paragraphs)
✓ Allows commercial use
✓ Allows modifications
✓ Only requires: Credit, copy license
✗ Provides no warranty
✗ Author not liable

Best for: Most research software

Famous MIT-licensed software:
- Rails, Node.js, jQuery, React
- Most scientific Python packages
```

**Apache License 2.0** (Permissive with Patent Protection)
```
Key Points:
✓ Permissive like MIT
✓ Explicit patent grant
✓ Slightly longer (more detailed)
✓ Allows commercial use
✗ Longer to understand
✗ More restrictive than MIT (slightly)

Best for: Tools where patent issues possible
Who uses: Google, Apache Foundation
```

**GPL v3** (Copyleft - Strong)
```
Key Points:
✓ Ensures freedom propagates
✓ Derivatives must be GPL
✓ Widespread in Linux world
✗ More restrictive
✗ Can complicate commercial use
✗ Longer and complex

Best for: When you want freedom guaranteed
Who uses: Linux, GNU tools, much bioinformatics
```

**LGPL** (Lesser GPL - Weak Copyleft)
```
Key Points:
✓ Copyleft for library itself
✓ Allows proprietary linking
✓ Middle ground between MIT and GPL

Best for: Libraries used in closed-source projects
Who uses: Some Qt libraries, some research packages
```

**CC0** (Public Domain)
```
Key Points:
✓ Waive all rights (public domain)
✓ No requirements at all
✓ Great for data (less for code)
✗ Unusual for software

Best for: Data, datasets, materials
```

### 4.4 Choosing Your License

**Decision Tree:**

```
1. Do you want to allow commercial use?
   NO → Not open source (proprietary)
   YES → Continue

2. Do you want modifications to stay open?
   NO → MIT, Apache, or BSD
   YES → Continue

3. How strong do you want copyleft?
   Weak → LGPL
   Strong → GPL v3
```

**Practical Recommendations:**

**For Most Research Software:**
→ **MIT License**
- Simplest, most liberal
- Widely understood
- No patent issues
- Most popular in Python/R

**If Worried About Patents:**
→ **Apache 2.0**
- Explicit patent protection
- Still permissive
- More formal

**If You Want Freedom Guaranteed:**
→ **GPL v3**
- Ensures derivatives open
- Philosophical choice
- Less popular in research

**For Data (Not Code):**
→ **CC BY** or **CC0**
- Designed for data
- Not software licenses
- Clear data sharing terms

### 4.5 Applying a License

**Step 1: Choose License**
- Visit choosealicense.com or creativecommons.org
- Select license
- Copy full license text

**Step 2: Create LICENSE File**
```
Your project/
├── LICENSE.txt         ← Full license text
├── README.md
└── src/
    └── main.py
```

**Step 3: Add Header to Source Files**
```python
# Copyright (C) 2024 Your Name
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the MIT License.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY...
```

**Step 4: Document in README**
```markdown
## License

This project is licensed under the MIT License - see LICENSE.txt

## Citation

If you use this software, please cite:
Author, A., Year. Software name. https://doi.org/...
```

**Step 5: Add to Package Metadata**

Python (setup.py):
```python
setup(
    name='mypackage',
    license='MIT',
    ...
)
```

R (DESCRIPTION):
```
License: MIT + file LICENSE
```

### 4.6 License Compatibility

**Mixing Licenses (Complex):**

**Compatible Combinations:**
- MIT code + MIT code = MIT ✓
- Apache + Apache = Apache ✓
- MIT + Apache = Apache (more restrictive) ✓
- GPL + GPL = GPL ✓

**Problematic Combinations:**
- GPL + Proprietary = NOT ALLOWED ✗
- AGPL + MIT = AGPL (stronger applies) ⚠
- GPL v2 + GPL v3 = Complex ⚠

**When Using Others' Code:**
1. Check their license
2. Ensure compatibility with yours
3. Include LICENSE file from dependency
4. Document original authors
5. Note modifications

### 4.7 Sharing and Distributing Software

**Where to Share Your Code:**

**Source Code Hosting:**
- **GitHub:** Most popular, free, large community
- **GitLab:** Alternative, good institutional support
- **Bitbucket:** Good for private repos, less used

**Package Registries:**
- **PyPI:** Python packages (pip install)
- **CRAN:** R packages (install.packages())
- **npm:** JavaScript packages
- **Maven Central:** Java packages
- **Conda-Forge:** Conda packages (cross-language)

**Research Software Registries:**
- **Zenodo:** Archive with DOI (recommended)
- **Figshare:** Data and code archival
- **F1000Research:** Software publication
- **Journal supplements:** Often required by publishers

**Best Practice Workflow:**
```
1. Develop on GitHub (collaborative)
2. Release on GitHub (tag versions)
3. Register on PyPI/CRAN (distribution)
4. Archive in Zenodo (long-term + DOI)
5. Publish paper (describe and cite)
```

### 4.8 Copyright and Attribution

**Ensuring Credit:**

**CITATION.cff File** (Standard format)
```yaml
# CITATION.cff format
cff-version: 1.2.0
title: "My Software Title"
authors:
  - family-names: Smith
    given-names: John
version: 1.0.0
date-released: 2024-01-15
url: "https://github.com/..."
license: MIT
```

**Requesting Citation:**
```markdown
## Citation

If you use this software in your research, please cite:

Smith, J., & Jones, B. (2024). Software name (v1.0). 
Zenodo. https://doi.org/10.5281/zenodo.1234567
```

**BibTeX Format:**
```bibtex
@software{smith2024software,
  title = {Software Name},
  author = {Smith, John and Jones, Bob},
  year = {2024},
  url = {https://zenodo.org/...},
  doi = {10.5281/zenodo.1234567}
}
```

### Summary

Licensing and sharing enable sustainable research software:
- **License:** Permission framework for reuse
- **Choose MIT:** Usually best for research
- **Apply properly:** License file + headers + metadata
- **Check compatibility:** If using others' code
- **Share widely:** GitHub → PyPI/CRAN → Zenodo → Paper
- **Enable citation:** Clear contribution recognition
- **Ensure sustainability:** Will others maintain it?

:::{admonition} Activities for Lesson 4
:class: activity

Complete at least two of the following activities to practice licensing and sharing software:

**Activity 4.1: License Selection and Application**
For a research software project (real or hypothetical):
- Determine which license best fits your goals (MIT, Apache 2.0, GPL, other)
- Justify your choice considering:
  - Do you want commercial use allowed?
  - Do you want derivative works to remain open?
  - How important is patent protection?
  - What licenses do your dependencies use?

Apply the license to code:
- Add LICENSE file to repository
- Add license header to source files
- Document license in README
- Add license field to package metadata

Document your choices and implementation.

**Activity 4.2: Prepare Software for Sharing**
Take one of your research software projects and prepare it for sharing:
- **Repository:** Create or update GitHub repository
- **Documentation:** Complete README, contributing guide, examples
- **License:** Apply open license (Activity 4.1)
- **Tests:** Add test suite with CI/CD
- **Metadata:** Complete setup.py/pyproject.toml/pubspec.yaml (or equivalent)
- **Citation:** Add CITATION.cff or suggest citation in README
- **Archive:** Create release and submit to Zenodo for DOI

Document the sharing workflow from GitHub to Zenodo.

**Activity 4.3: Create Software Sharing Strategy**
Design a comprehensive sharing strategy for a research software project:
- **Initial development:** Where will you host code? (GitHub, GitLab, other)
- **Package distribution:** Will you publish to PyPI/CRAN/other registry?
- **Archival:** Where/how will you archive for long-term preservation?
- **Documentation:** How will you maintain documentation?
- **Community:** How will you engage with users?
- **Maintenance:** Realistic timeline for maintenance?
- **Citation:** How will users cite your software?

Write a 1-2 page sharing strategy document.

**Deliverable:** Your choice of output from activities above (2-3 pages total).
:::

## Lesson 5: Building Sustainable Research Software

### Overview
In this final lesson, you bring together all the elements of good research software development: planning, coding, documenting, testing, and sharing. You develop a strategy for sustainable software development, learn from successful examples, understand long-term maintenance, and create your software development plan.

### 5.1 From Script to Sustainable Software

**Evolution Path:**

**Stage 1: Quick Script (Week 1)**
```python
# quick_analysis.py
import numpy as np
data = np.loadtxt('data.csv')
result = np.mean(data)
print(result)
```
**Characteristics:** Fast, specific, disposable
**Next step:** If useful, evolve to Stage 2

**Stage 2: Reusable Tool (Week 2-4)**
```python
# analysis_tool.py - Can be imported
import numpy as np

def analyze(filename):
    """Load data and compute mean."""
    data = np.loadtxt(filename)
    return np.mean(data)

if __name__ == '__main__':
    result = analyze('data.csv')
    print(result)
```
**Improvements:** Function, docstring, modularity
**Next step:** If widely useful, evolve to Stage 3

**Stage 3: Documented Package (Month 2)**
```
project/
├── README.md
├── LICENSE.txt
├── setup.py
├── requirements.txt
├── analysis/
│   ├── __init__.py
│   └── tools.py
├── tests/
│   └── test_tools.py
└── examples/
    └── example.py
```
**Improvements:** Package structure, tests, docs
**Next step:** Register on PyPI

**Stage 4: Professional Package (Month 3-6)**
```
+ GitHub repository
+ Continuous Integration
+ Full documentation
+ Multiple versions
+ Active maintenance
+ Community support
```
**Improvements:** Professional practices
**Result:** Sustainable, widely-used tool

### 5.2 Software Development Workflow

**Minimal Viable Development** (Research Scripts)
```
1. Code implementation
2. Manual testing
3. Share (maybe)
4. Iterate based on feedback
```

**Standard Development** (Research Tools)
```
1. Design (how to structure)
2. Implementation (write code)
3. Testing (unit + manual)
4. Documentation (README + docstrings)
5. Version control (Git commits)
6. Sharing (GitHub, maybe PyPI)
7. Maintenance (respond to issues)
```

**Professional Development** (Packages)
```
1. Requirements specification
2. Architecture design
3. Implementation with TDD
4. Comprehensive testing
5. Code review (pull requests)
6. Complete documentation
7. Version control with branching
8. CI/CD pipeline
9. Release management
10. Continuous maintenance
```

### 5.3 Maintenance and Sustainability

**Common Failure Patterns:**

**Abandoned After Publication**
- Develop, publish, abandon
- No maintenance, bugs accumulate
- Dependencies break
- Result: Unusable after 2 years

**Sustainable Alternative:**
- Small regular maintenance time
- Quick bug fixes
- Dependency updates quarterly
- Community engagement
- Long-term usefulness

**Maintenance Time Estimates:**

**Small research project** (< 1000 lines)
- Initial development: 2-4 weeks
- Maintenance: 1-2 hours/month
- Commitment: 2-3 years minimum

**Medium-sized tool** (1,000-10,000 lines)
- Initial development: 2-3 months
- Maintenance: 5-10 hours/month
- Commitment: 5+ years

**Large package** (10,000+ lines)
- Initial development: 6-12 months
- Maintenance: 20+ hours/month
- Commitment: Ongoing (consider team)

**Sustainability Strategies:**

**Individual Maintenance**
- Feasible for small projects
- Works 2-5 years
- Requires passion and interest
- Risk: Burnout if unpaid

**Team Maintenance**
- Distributes load
- Sustainable longer
- Requires organization
- Risk: Coordination complexity

**Grant Funding**
- Sustainable indefinitely
- Requires grant success
- Good for large projects
- Example: rOpenSci, NumFOCUS

**Institutional Support**
- University computing center
- Research institute support
- Most sustainable
- Growing trend

**Community Support**
- Crowdfunding (Patreon, GitHub Sponsors)
- Community contributions
- Donations and sponsorship
- Works for popular projects

### 5.4 Growing and Engaging Community

**Starting Small (Just You)**
```
✓ Publish on GitHub
✓ Share in relevant communities
✓ Write blog post about tool
✓ Cite your own software in papers
```

**Building Community (Early Users)**
```
✓ Respond quickly to issues
✓ Add features users request
✓ Recognize contributors
✓ Build contributor guide
✓ Create discussion forum/Slack
✓ Hold quarterly community calls
```

**Mature Project (Many Users)**
```
✓ Governance structure
✓ Code review process
✓ Release schedule
✓ Roadmap (transparent)
✓ Code of conduct
✓ Multiple maintainers
✓ Annual conference/workshop
```

### 5.5 Documentation for Sustainability

**Critical Documentation:**

**For Users:**
- README (quick start)
- Installation guide
- Tutorials
- API reference

**For Contributors:**
- CONTRIBUTING.md
- Development setup
- Architecture overview
- Code style guide
- Testing procedures

**For Maintainers:**
- Release process
- Deployment procedures
- Known issues and workarounds
- Future roadmap
- Maintenance timeline

**Documentation Tools:**
- **Sphinx (Python):** Industry standard
- **Roxygen (R):** Auto-generate from comments
- **MkDocs:** Simple website docs
- **GitHub Pages:** Free documentation hosting
- **ReadTheDocs:** Automated documentation with versioning

### 5.6 Examples of Sustainable Research Software

**Small, Sustainable Project: R's [ggplot2](https://ggplot2.tidyverse.org/)**
- Created: 2007
- Lines: ~15,000
- Users: Millions
- Maintenance: Hadley Wickham ([RStudio](https://www.rstudio.com/) support)
- Key: Simple, solves one problem well

**Medium, Sustainable: [Bioconductor](https://www.bioconductor.org/)**
- Created: 2002
- Projects: 2,000+ packages
- Users: Tens of thousands
- Maintenance: Organized project
- Key: Community structure, annual conference

**Large, Sustainable: [NumPy](https://numpy.org/)/[SciPy](https://scipy.org/)**
- Created: 2000s
- Lines: 100,000+
- Users: Millions
- Maintenance: [NumFOCUS](https://numfocus.org/) funding, multiple maintainers
- Key: Funding, governance, institutional support

**Success Factors Across Projects:**
1. Solve a real problem well
2. Clear documentation
3. Respond to users
4. Sustainable commitment
5. Organized governance
6. Multiple maintainers
7. Institutional/funder support

### 5.7 Your Software Development Plan

**Plan Template:**

**Project Description:**
- What problem does it solve?
- Who are users?
- Why open source?

**Development Scope:**
- Initial scope (MVP - minimum viable product)
- Future vision (long-term goals)
- Success metrics

**Development Timeline:**
- Month 1-2: Core functionality
- Month 2-3: Documentation and tests
- Month 3+: Share and gather feedback
- Year 1+: Maintenance plan

**Maintenance Commitment:**
- Who will maintain?
- How much time per month?
- For how long?
- What if you can't continue?

**Resources Needed:**
- Computing infrastructure (GitHub, server)
- Documentation platform (ReadTheDocs, GitHub Pages)
- CI/CD (GitHub Actions, Travis CI)
- Communication (Slack, Discord, email list)

**Community Engagement:**
- How will users contribute?
- Code review process?
- Release schedule?
- Conference/workshop plans?

**Sustainability Strategy:**
- Individual maintenance or team?
- Grant funding plans?
- Institutional support?
- Contingency if you leave?

### 5.8 Checklist: Before Releasing Software

**Code Quality:**
- ☐ Code follows style guidelines
- ☐ Clear function/variable names
- ☐ No debug code or prints left
- ☐ Handles errors gracefully
- ☐ Performance acceptable

**Testing:**
- ☐ Unit tests written (70%+ coverage)
- ☐ All tests pass
- ☐ Integration tests pass
- ☐ Tested on different systems
- ☐ Edge cases tested

**Documentation:**
- ☐ README clear and complete
- ☐ Installation instructions work
- ☐ Quick start example works
- ☐ Full API documentation complete
- ☐ Code comments explain logic
- ☐ Examples/tutorials included

**Reproducibility:**
- ☐ Requirements.txt/environment.yml
- ☐ Version numbers documented
- ☐ OS dependencies listed
- ☐ Hardware requirements clear
- ☐ Reproducible example provided

**Licensing:**
- ☐ LICENSE.txt file included
- ☐ Headers in source files
- ☐ License in metadata (setup.py, etc.)
- ☐ Compatible with dependencies

**Version Control:**
- ☐ On GitHub/GitLab
- ☐ Clean commit history
- ☐ Tagged version release
- ☐ CHANGELOG.md updated

**Distribution:**
- ☐ Registered on PyPI/CRAN (if applicable)
- ☐ Archived in Zenodo with DOI
- ☐ CITATION.cff file created
- ☐ Citation example in README

**Community:**
- ☐ CONTRIBUTING.md written
- ☐ Code of conduct established
- ☐ Issue tracking enabled
- ☐ Communication channels open
- ☐ Maintenance plan documented

### 5.9 Measuring Success

**Metrics:**

**Usage Metrics:**
- GitHub stars/forks
- Downloads (PyPI, CRAN)
- Citations in papers
- Altmetric score

**Community Metrics:**
- Contributors
- Issues/PRs per month
- Response time to issues
- Discord/Slack membership

**Quality Metrics:**
- Test coverage
- Number of bugs reported
- Time to fix bugs
- Documentation completeness

**Impact Metrics:**
- Citations in downstream projects
- Awards/recognition
- Funding obtained
- Institutional adoption

### Summary

Sustainable research software requires:
- **Planning:** Clear vision and scope
- **Development:** Quality code and testing
- **Documentation:** Complete and maintained
- **Community:** Engagement and contribution
- **Maintenance:** Realistic commitment
- **Sustainability:** Planning for long-term
- **Impact:** Measurement and improvement

:::{admonition} Activities for Lesson 5
:class: activity

Complete at least one of the following activities to build sustainable software:

**Activity 5.1: Create a Sustainable Software Plan**
Develop a comprehensive plan for a research software project (real or hypothetical):
- **Vision:** What problem does it solve? What is the long-term vision?
- **Scope:** What features are core? What is nice-to-have?
- **Development:** How will you manage development? (Git workflow, version control)
- **Documentation:** What will you document? Maintenance plan?
- **Testing:** What quality standards? How will you test?
- **Community:** How will you engage users? Contribution guidelines?
- **Maintenance:** Realistic timeline? Who will maintain?
- **Funding:** How will you sustain development? (personal time, funding, community)
- **Success metrics:** How will you measure impact and usage?

Aim for 2-3 pages covering these elements.

**Activity 5.2: Develop Contribution Guidelines**
Create comprehensive contribution guidelines for a research software project:
- **Code of conduct:** Expected behavior for contributors
- **Contributing guide:** How to contribute (reporting issues, pull requests)
- **Development setup:** How to set up development environment
- **Coding standards:** Style guide, testing requirements
- **Commit messages:** Standards for git commits
- **Pull request process:** Steps for merging contributions
- **Recognition:** How contributors will be credited
- **Support channels:** Where to ask questions

Write clear documentation that invites and guides contributions.

**Activity 5.3: Design Long-Term Maintenance Strategy**
Create a sustainability and maintenance plan:
- **Short-term (1 year):** Active development, feature additions
- **Medium-term (2-5 years):** Maintenance mode, critical fixes
- **Long-term (5+ years):** Archival, preservation, potential successor projects
- **Succession planning:** What if you can't maintain it?
- **Community support:** How to grow volunteer maintainers?
- **Funding strategy:** Potential sources for sustained funding
- **Documentation preservation:** How will docs survive long-term?

Write a 1-2 page strategy addressing these elements.

**Deliverable:** Your choice of output from activities above (2-3 pages total).
:::

**Remember:**
- ✓ Start small, grow gradually
- ✓ Focus on solving real problems
- ✓ Invest in documentation
- ✓ Engage your community
- ✓ Plan for maintenance
- ✓ Don't try to do everything
- ✓ Ask for help
- ✓ Your software can change science

**Your Next Steps:**
1. Identify a problem to solve
2. Start with a simple script
3. Add tests and documentation
4. Share on GitHub
5. Gather feedback
6. Iterate with community
7. Plan for long-term maintenance
8. Watch it grow

**Welcome to the open software community. Let's build better tools together.**
