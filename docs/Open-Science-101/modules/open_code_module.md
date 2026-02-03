# Module 4: Open Code

This module focuses on the practice and application of open code as part of the open science workflow. It provides a 'how to' process that follows the code development lifecycle and "Use, Make, Share" framework. Some of the key topics discussed include: benefits and limitations of open code, how to discover and assess code, considerations and methods for programming following open principles, and finally when and how to share your code.

## Learning Objectives

After completing this module, you should be able to:
- Explain what open-source software means, including the software development cycle, the benefits, some common limitations, and how they are addressed.
- Assess open-source software for reuse by evaluating provided documentation, including README files and licensing details, and then cite the software appropriately.
- Create an open-source software management plan that includes the strategy for selecting open software dependencies and open repositories such as GIT, and how open elements including metadata, README files and version control, will be included to make the software reusable and findable.
- Evaluate whether your open-source software can be shared and the best options for sharing to increase visibility.
- List the responsibilities a software developer has once the open-source software is shared including managing legal requirements and ensuring the software is maintained.

### Lesson 1: Introduction to Open Code

#### Overview
This lesson defines the key terms, core principles, benefits, and challenges of open code. The practice of making code openly available to the public occurs within a spectrum from more to less protected. Ethical and legal conditions can limit the degree of openness that researchers can permit. This lesson will introduce the critical questions to consider when determining the appropriate accessibility of code to external users along with best practices to overcome common constraints to maximize availability. The lesson concludes with a discussion on the software lifecycle and how it fits with the "Use, Make, Share" framework and its relationship to a management plan.

#### 1.1 Key Terms and Definitions

**Open Code (Open-Source Software)**
Open code, also referred to as open-source software (OSS), is software whose source code is made freely available for anyone to view, use, modify, and distribute. The code is typically accompanied by a license that specifies the terms under which it can be used and shared.

**Source Code**
The human-readable instructions written by programmers that define how software operates. Source code is written in programming languages such as Python, R, C++, Java, or JavaScript.

**Example:**
```python
# Simple Python function to calculate the mean of a dataset
def calculate_mean(data):
    """Calculate the arithmetic mean of a list of numbers."""
    if not data:
        return None
    return sum(data) / len(data)

# Usage
temperatures = [72.5, 68.3, 75.1, 70.8]
average_temp = calculate_mean(temperatures)
print(f"Average temperature: {average_temp}°F")
```

**Repository**
A centralized location where code is stored, managed, and version-controlled. Common repository platforms include GitHub, GitLab, and Bitbucket.

**Version Control**
A system that tracks changes to code over time, allowing multiple contributors to work collaboratively and maintain a history of modifications. Git is the most widely used version control system.

**License**
A legal document that specifies how software can be used, modified, and distributed. Common open-source licenses include MIT, Apache 2.0, GPL, and BSD.

#### 1.2 Core Principles of Open Code

Open code is built on several fundamental principles:

**Transparency**
The complete source code is visible and accessible, allowing anyone to understand how the software works. This transparency enables peer review, validation of methods, and identification of potential issues.

**Collaboration**
Open code encourages collaborative development where individuals and organizations can contribute improvements, fix bugs, and add new features.

**Reproducibility**
By making code openly available, researchers enable others to reproduce their computational analyses and verify results, which is essential for scientific integrity.

**Reusability**
Open code can be adapted and reused in different contexts, preventing duplication of effort and accelerating scientific progress.

**Community-Driven Development**
Open-source projects often benefit from community contributions, testing, and feedback, leading to more robust and well-tested software.

#### 1.3 The Spectrum of Openness

Code accessibility exists on a spectrum, not as a binary open/closed choice:

**Fully Open**
- Source code publicly available without restrictions
- Permissive license (e.g., MIT, Apache 2.0)
- No registration or approval required to access
- Example: Python's NumPy library on GitHub

**Open with Registration**
- Source code available but requires user registration
- May include export control considerations
- Example: Software with controlled access due to security concerns

**Open to Collaborators**
- Shared within a defined research group or consortium
- Private repository with specified collaborators
- Example: Code shared among institutional partners during active research

**Embargoed Open**
- Will become open after a specified period
- Common in competitive research environments
- Example: Code released upon publication of associated research paper

**Closed with Available Binaries**
- Compiled software is available but not source code
- Users can run the software but cannot modify it
- Example: Some commercial scientific software packages

#### 1.4 Benefits of Open Code

**For Individual Researchers:**
- **Enhanced Visibility:** Open code increases the discoverability and citation of your work
- **Career Advancement:** Demonstrates technical skills and collaborative abilities
- **Learning Opportunities:** Feedback from the community improves coding skills
- **Reduced Maintenance Burden:** Community contributions help maintain and improve code

**Example:** A postdoctoral researcher shared their data analysis pipeline on GitHub. The code received contributions from researchers at other institutions, fixing bugs and adding features. This collaboration led to a co-authored methods paper and established valuable research connections.

**For the Research Community:**
- **Accelerated Discovery:** Researchers build upon existing work rather than starting from scratch
- **Improved Reproducibility:** Others can verify computational results
- **Quality Improvement:** Peer review and community testing identify and fix issues
- **Educational Value:** Students learn from well-documented, real-world code examples

**Example:** The Astropy project, an open-source Python library for astronomy, has enabled thousands of researchers to perform standardized astronomical calculations, greatly accelerating research in the field.

**For Science and Society:**
- **Transparency:** Public investment in research yields publicly accessible tools
- **Innovation:** Open code can be adapted for new applications beyond original intent
- **Reduced Costs:** Eliminates redundant development efforts
- **Equity:** Researchers at less-resourced institutions gain access to advanced tools

#### 1.5 Challenges and Limitations of Open Code

**Challenge 1: Time and Effort Required**
Making code truly reusable requires documentation, testing, and cleanup, which takes additional time beyond getting code to work for your own purposes.

**Best Practice:**
- Document as you code rather than as a final step
- Use consistent coding standards from the start
- Allocate time in project planning for code preparation

**Example:** Budget 20-30% additional time for documentation, testing, and preparing code for release.

**Challenge 2: Intellectual Property and Competitive Concerns**
Researchers may worry about others using their code before they publish their findings, or institutions may have policies about protecting intellectual property.

**Best Practice:**
- Use embargoed release (share code upon paper publication)
- Choose appropriate licenses that require attribution
- Understand your institution's IP policies early in the project

**Challenge 3: Quality and Sustainability Concerns**
Releasing code publicly raises concerns about code quality, and maintaining code after release requires ongoing effort.

**Best Practice:**
- Start with clear documentation of what the code does and its limitations
- Use a LICENSE file and README to set expectations
- Consider archiving stable versions in repositories like Zenodo for long-term preservation

**Example:** Include a statement like: "This code is provided as-is to support the findings in [paper citation]. While we welcome issues and feedback, active development has concluded."

**Challenge 4: Privacy and Security**
Code may contain sensitive information, access credentials, or work with protected data.

**Best Practice:**
- Use environment variables or configuration files for sensitive information
- Review code for hardcoded passwords, API keys, or file paths
- Separate data processing code from the data itself
- Use `.gitignore` files to prevent accidental commits of sensitive files

**Example:**
```python
# Instead of:
api_key = "abc123xyz789"  # DON'T DO THIS

# Use environment variables:
import os
api_key = os.environ.get('API_KEY')
```

**Challenge 5: Ethical and Legal Constraints**
Some research involves export-controlled technologies, proprietary data sources, or software subject to institutional restrictions.

**Best Practice:**
- Consult with your institution's technology transfer office
- Understand export control regulations if applicable
- Consider sharing algorithms/methods even if specific implementations cannot be released
- Document why code cannot be shared when relevant

#### 1.6 Critical Questions for Determining Code Accessibility

Before sharing code, consider these essential questions:

**Legal and Ethical Questions:**
1. Are there any legal restrictions on sharing this code (e.g., export controls, institutional IP agreements)?
2. Does the code contain or process sensitive, private, or protected data?
3. Have all contributors agreed to the code being released under an open license?
4. Does the code use proprietary dependencies that cannot be redistributed?

**Practical Questions:**
5. Is the code in a state that others could reasonably understand and use it?
6. Have security vulnerabilities been addressed?
7. Are there dependencies that others may not have access to?
8. Is there adequate documentation for others to understand the code's purpose and usage?

**Strategic Questions:**
9. What is the appropriate timing for release (now, at publication, after a certain date)?
10. What level of support can be committed to after release?
11. Which license best aligns with the intended use and reuse of the code?
12. Where should the code be shared to reach the intended audience?

#### 1.7 The Software Development Lifecycle

Understanding where openness fits in the development process is crucial:

**1. Planning and Design Phase**
- Decide on open vs. closed approach
- Select appropriate licenses
- Plan for documentation and testing
- Choose version control and repository platform

**2. Development Phase**
- Write code following best practices and style guides
- Document as you develop
- Use version control for all changes
- Write tests to verify functionality

**3. Testing and Quality Assurance Phase**
- Conduct peer code review
- Run automated tests
- Check for security vulnerabilities
- Validate against requirements

**4. Release Phase**
- Finalize documentation (README, installation instructions, examples)
- Choose and apply appropriate license
- Tag stable version
- Publish to repository or registry

**5. Maintenance Phase**
- Address bug reports and issues
- Incorporate community contributions
- Release updates and patches
- Archive when no longer maintained

**Example Workflow:**
A climate scientist develops a Python package for analyzing temperature data:
1. **Planning:** Chooses GitHub for version control, decides on MIT license
2. **Development:** Writes code with inline comments, commits regularly to GitHub
3. **Testing:** Creates test suite with sample data, runs continuous integration
4. **Release:** Writes comprehensive README, publishes to PyPI for easy installation
5. **Maintenance:** Responds to GitHub issues, accepts pull requests from users

#### 1.8 The "Use, Make, Share" Framework

Open code development fits within the broader "Use, Make, Share" framework for open science:

**USE Existing Open Code**
- Search for existing solutions before writing new code
- Evaluate quality, documentation, and licensing of existing tools
- Properly cite and acknowledge code you use
- Contribute back improvements when possible

**MAKE Your Code Open**
- Follow best practices for code development
- Document thoroughly for future users (including future you)
- Choose appropriate open-source license
- Prepare code for sharing throughout development, not just at the end

**SHARE Your Code**
- Select appropriate platforms (GitHub, GitLab, institutional repositories)
- Include comprehensive documentation and examples
- Make code discoverable with metadata and keywords
- Register with software registries (PyPI, CRAN, conda-forge)
- Archive stable versions for long-term preservation (Zenodo, Software Heritage)

**Integration Example:**
A researcher studying ocean microplastics:
1. **Uses** existing image analysis libraries (OpenCV, scikit-image)
2. **Makes** custom analysis scripts following open practices with documentation
3. **Shares** the complete analysis pipeline on GitHub with sample data
4. Archives the exact version used in the paper on Zenodo with a DOI
5. Other researchers can now reproduce the analysis and apply it to their own data

#### 1.9 Software Management Plans

A Software Management Plan (SMP) is a document that outlines how software will be developed, maintained, and shared throughout a project.

**Key Components of an SMP:**

1. **Project Description**
   - Purpose and scope of the software
   - Intended users and use cases
   - Expected lifetime of the software

2. **Development Approach**
   - Programming languages and frameworks
   - Development environment and tools
   - Coding standards and best practices
   - Version control strategy

3. **Documentation Strategy**
   - Types of documentation (README, API docs, tutorials)
   - Documentation tools and formats
   - Maintenance plan for documentation

4. **Testing and Quality Assurance**
   - Testing approach (unit tests, integration tests)
   - Continuous integration setup
   - Code review process

5. **Licensing and Legal Considerations**
   - Chosen open-source license and justification
   - Intellectual property considerations
   - Export control or security reviews if needed

6. **Sharing and Dissemination**
   - Where code will be shared (GitHub, GitLab, institutional repository)
   - When code will be released (immediately, at publication, embargo period)
   - How code will be made discoverable (registries, publications, presentations)

7. **Sustainability and Maintenance**
   - Maintenance plan and timeline
   - Community engagement strategy
   - Succession planning if development team changes

**Example SMP Excerpt:**

> **Project:** Atmospheric CO2 Analysis Toolkit
> 
> **Development Approach:** Python-based package using NumPy, Pandas, and Matplotlib. Code will follow PEP 8 style guidelines and be hosted on GitHub with Git version control. Development will use feature branches with code review before merging to main branch.
>
> **Licensing:** MIT License chosen to maximize reusability and allow commercial applications while maintaining attribution.
>
> **Sharing Plan:** Code will be released publicly on GitHub upon submission of the first paper using the toolkit. The package will be submitted to PyPI for easy installation via pip. A DOI will be obtained through Zenodo for citation purposes.
>
> **Maintenance:** The development team commits to maintaining the package for a minimum of 3 years, including bug fixes and compatibility updates. After this period, the repository will be archived with clear documentation of its status.

#### 1.10 Best Practices to Maximize Code Openness

**Start with Open as the Default**
Plan for openness from the beginning rather than trying to make code open after development is complete.

**Use Clear Documentation**
Include README files explaining what the code does, how to install and use it, and how to contribute.

**Choose Appropriate Licenses**
Select licenses that align with your goals for reuse and provide legal clarity for users.

**Follow Coding Standards**
Use established style guides and conventions for your programming language to make code more readable.

**Include Examples and Tutorials**
Provide worked examples showing how to use the code for common tasks.

**Make Code Citable**
Obtain a DOI for your code through services like Zenodo or institutional repositories.

**Engage with the Community**
Be responsive to issues and questions, and welcome contributions from others.

**Plan for Longevity**
Archive stable versions in persistent repositories to ensure long-term availability.

#### Summary

Open code is a fundamental component of open science that promotes transparency, reproducibility, and collaboration. While there are challenges to making code openly available, following best practices and planning for openness from the start of a project can help overcome these obstacles. The software development lifecycle, when integrated with the "Use, Make, Share" framework and guided by a software management plan, provides a structured approach to creating and disseminating open code that benefits individual researchers, the scientific community, and society at large.

### Lesson 2: Using Open Code

#### Overview
In this lesson, you learn the steps for using existing open code in your work. These steps include discovering, assessing, reusing, citing, and acknowledging. Leveraging existing open-source software is a cornerstone of efficient and collaborative research. By building upon well-tested, documented code, researchers can focus on novel aspects of their work rather than reinventing solutions to common problems.

#### 2.1 Discovering Open Code

Finding the right open-source software for your needs requires knowing where to look and how to search effectively.

**Primary Discovery Platforms:**

**General Code Repositories**
- **GitHub** (github.com): The largest platform for open-source projects, with over 100 million repositories
- **GitLab** (gitlab.com): Offers both cloud-hosted and self-hosted repositories
- **Bitbucket** (bitbucket.org): Supports both Git and Mercurial version control

**Language-Specific Package Registries**
- **Python:** PyPI (Python Package Index) - pypi.org
- **R:** CRAN (Comprehensive R Archive Network) - cran.r-project.org
- **JavaScript/Node.js:** npm (Node Package Manager) - npmjs.com
- **Julia:** JuliaHub and General Registry - juliahub.com
- **MATLAB:** File Exchange - mathworks.com/matlabcentral/fileexchange

**Scientific Software Registries**
- **SciCrunch Research Resource Identifiers (RRIDs):** scicrunch.org
- **bio.tools:** Registry of bioinformatics tools
- **Astrophysics Source Code Library (ASCL):** ascl.net
- **Zenodo:** zenodo.org (includes archived software with DOIs)

**Search Strategies:**

1. **Keyword Search**
   - Use descriptive terms related to your task
   - Include domain-specific terminology
   - Example: "phylogenetic tree visualization python"

2. **Topic-Based Discovery**
   - GitHub Topics: Browse curated topics like "machine-learning," "climate-science," "genomics"
   - Tags in package registries

3. **Citation Tracking**
   - Look for code citations in papers related to your work
   - Use Google Scholar to find papers that cite specific software

4. **Community Recommendations**
   - Ask colleagues and collaborators
   - Consult domain-specific forums and mailing lists
   - Check recommendations in online courses and tutorials

**Example Discovery Process:**

A marine biologist needs software to analyze satellite ocean color data:

1. Searches GitHub for "ocean color satellite python"
2. Finds several repositories; narrows by checking stars, recent activity, and documentation
3. Searches PyPI for "ocean color" to find installable packages
4. Checks recent papers in their field for software citations
5. Asks colleagues on an oceanography mailing list
6. Discovers `seaborn-oceanography` and NASA's `SeaDAS` as top candidates

#### 2.2 Assessing Open Code Quality and Suitability

Not all open code is created equal. Careful assessment ensures you choose software that is reliable, maintainable, and appropriate for your needs.

**Assessment Criteria:**

**1. Documentation Quality**

Good documentation is essential for understanding and using software effectively.

**What to Look For:**
- **README file:** Clear description of what the software does, installation instructions, basic usage examples
- **User guides/tutorials:** Step-by-step instructions for common use cases
- **API documentation:** Detailed descriptions of functions, classes, and parameters
- **Code comments:** Inline explanations of complex logic
- **Examples:** Working code samples demonstrating functionality

**Red Flags:**
- No README or minimal information
- Instructions that don't work or are outdated
- Lack of examples
- Poorly written or missing comments

**Example of Good Documentation:**
```markdown
# Climate Data Analyzer

## Description
A Python package for analyzing historical climate data from NOAA sources.

## Installation
```bash
pip install climate-data-analyzer
```

## Quick Start
```python
import climate_analyzer as ca

# Load temperature data
data = ca.load_noaa_data('temperature', '2010-2020')

# Calculate annual means
annual_means = ca.calculate_annual_means(data)

# Plot results
ca.plot_timeseries(annual_means)
```

## Requirements
- Python 3.8+
- NumPy >= 1.20
- Pandas >= 1.3
- Matplotlib >= 3.3
```

**2. Licensing**

Understanding the license is crucial for legal compliance.

**Common Open-Source Licenses:**

- **Permissive Licenses (Most Freedom):**
  - **MIT License:** Very permissive, allows commercial use, modification, and distribution with minimal restrictions
  - **Apache 2.0:** Similar to MIT but includes patent grants and trademark protections
  - **BSD Licenses (2-Clause, 3-Clause):** Simple permissive licenses with few restrictions

- **Copyleft Licenses (Share-Alike):**
  - **GPL (General Public License):** Requires derivative works to be distributed under the same license
  - **LGPL (Lesser GPL):** More permissive than GPL, allows linking to proprietary software
  - **AGPL (Affero GPL):** Like GPL but also applies to software accessed over a network

- **Creative Commons:**
  - Often used for documentation, data, or educational materials
  - Not recommended for software code

**License Compatibility Example:**

You're developing proprietary software for your institution:
- ✅ **Can use:** MIT, Apache 2.0, BSD licensed libraries
- ⚠️ **Use with caution:** LGPL libraries (can link dynamically)
- ❌ **Cannot use:** GPL, AGPL licensed code (would require your code to also be GPL)

**Where to Find License Information:**
- LICENSE or LICENSE.txt file in the repository root
- README file with license badge or statement
- Package metadata (e.g., in setup.py for Python)
- Repository settings page (e.g., GitHub shows license in "About" section)

**3. Activity and Maintenance**

**Indicators of Active Maintenance:**
- Recent commits (within last 3-6 months)
- Open issues are being addressed
- Pull requests are reviewed and merged
- Regular releases/version updates
- Active discussion in issues or forums

**Indicators of Abandoned Projects:**
- No commits for over a year
- Many unaddressed issues
- Pull requests ignored
- Documentation mentions outdated dependencies
- No response to recent issues

**Note:** A lack of recent activity isn't always bad if:
- Software is mature and stable
- Repository is explicitly archived with statement of completion
- Scope was limited and goals have been achieved

**4. Code Quality Indicators**

- **Tests:** Presence of test suite with good coverage
- **Continuous Integration:** Automated testing (badges showing "build passing")
- **Code Style:** Consistent formatting and style
- **Structure:** Well-organized directory structure
- **Dependencies:** Reasonable number of dependencies, preferably well-maintained ones

**5. Community and Support**

- **GitHub Stars/Forks:** Indicates popularity and community interest
- **Contributors:** Multiple contributors suggests collaborative development
- **Issue Response Time:** How quickly maintainers respond to questions
- **Discussion Forums:** Active community forum, chat channel, or mailing list
- **Citations:** Number of papers citing the software

**6. Functionality and Performance**

- **Feature Completeness:** Does it do what you need?
- **Scalability:** Can it handle your data size/complexity?
- **Speed:** Is performance adequate for your use case?
- **Platform Compatibility:** Does it work on your operating system?
- **Dependencies:** Are dependencies available and compatible with your environment?

**Assessment Checklist Example:**

Evaluating a Python package for genomic analysis:

| Criterion | Status | Notes |
|-----------|--------|-------|
| README present | ✅ | Clear, comprehensive |
| Installation docs | ✅ | Works on first try |
| Usage examples | ✅ | Multiple examples provided |
| License | ✅ | MIT License - very permissive |
| Recent commits | ✅ | Last commit 2 weeks ago |
| Issue response | ✅ | Most issues answered within days |
| Test suite | ✅ | 85% code coverage |
| Citations | ✅ | 150+ papers cite this tool |
| Dependencies | ⚠️ | One dependency is deprecated |
| Performance | ✅ | Tested with our data size |

**Decision:** Proceed with use, but monitor the deprecated dependency issue.

#### 2.3 Reusing Open Code

Once you've found and assessed suitable software, follow best practices for integration into your work.

**Installation and Setup**

**Use Package Managers When Possible:**
```bash
# Python
pip install package-name
# or for conda
conda install -c conda-forge package-name

# R
install.packages("packagename")

# Node.js
npm install package-name
```

**Version Pinning for Reproducibility:**

Specify exact versions in your requirements:

```python
# requirements.txt
numpy==1.21.2
pandas==1.3.3
scipy==1.7.1
```

**Use Virtual Environments:**

```bash
# Python virtual environment
python -m venv myproject_env
source myproject_env/bin/activate  # On macOS/Linux
# myproject_env\Scripts\activate  # On Windows

pip install -r requirements.txt
```

This isolates dependencies and ensures reproducibility.

**Integration Best Practices**

**1. Start Simple**

Begin with basic examples from documentation before attempting complex usage.

```python
# Start with simple example from docs
import awesome_library as al

# Test basic functionality
result = al.basic_function(simple_input)
print(result)  # Verify it works

# Then build up to your use case
```

**2. Wrapper Functions**

Create wrapper functions around external code to:
- Simplify usage for your specific needs
- Make it easier to swap libraries later if needed
- Add domain-specific error handling

```python
import external_library as ext

def analyze_my_data(data_path, parameters):
    """Wrapper around external_library for our specific workflow."""
    # Load data in our format
    data = load_our_format(data_path)
    
    # Convert to format expected by external library
    ext_format = convert_to_ext_format(data)
    
    # Call external library
    result = ext.analyze(ext_format, **parameters)
    
    # Convert result back to our format
    our_result = convert_from_ext_format(result)
    
    return our_result
```

**3. Error Handling**

Add appropriate error handling, especially for external dependencies:

```python
try:
    import optional_library
    HAS_OPTIONAL = True
except ImportError:
    HAS_OPTIONAL = False
    warnings.warn("Optional library not found. Some features disabled.")

def advanced_analysis(data):
    if not HAS_OPTIONAL:
        raise ImportError("This function requires optional_library. "
                         "Install with: pip install optional_library")
    return optional_library.analyze(data)
```

**4. Testing Your Integration**

Verify that the external code works as expected in your environment:

```python
import pytest
import your_module as ym

def test_external_integration():
    """Test that external library integration works."""
    # Use known test case
    test_data = ym.load_test_data()
    result = ym.analyze_my_data(test_data, {'param': 1.0})
    
    # Verify expected output
    assert result.shape == (100, 3)
    assert result.mean() > 0
```

**Version Compatibility Management**

Libraries change over time. Plan for this:

```python
import package
import warnings

# Check version and warn if unexpected
if package.__version__ < '2.0.0':
    warnings.warn(f"This code was tested with package >= 2.0.0. "
                  f"You have {package.__version__}. Results may differ.")
```

**Documentation of Dependencies**

Document all external dependencies clearly:

```markdown
# Dependencies

This analysis requires the following software:

- Python >= 3.8
- NumPy >= 1.20 (data manipulation)
- SciPy >= 1.6 (statistical tests)
- climate-analyzer == 2.3.1 (climate data processing)
  - Available at: https://github.com/climate/analyzer
  - License: MIT
  - Citation: Smith et al. (2020)

## Installation

```bash
pip install numpy scipy
pip install climate-analyzer==2.3.1
```
```

#### 2.4 Citing Open Code

Proper citation of software is essential for:
- Giving credit to developers
- Enabling reproducibility
- Helping others find useful tools
- Supporting the case for funding open-source development

**Finding Citation Information**

**1. CITATION File**

Many repositories include a CITATION or CITATION.cff file:

```yaml
# CITATION.cff
cff-version: 1.2.0
message: "If you use this software, please cite it as below."
authors:
  - family-names: Smith
    given-names: Jane
    orcid: https://orcid.org/0000-0002-1234-5678
title: "Climate Data Analyzer"
version: 2.3.1
doi: 10.5281/zenodo.1234567
date-released: 2024-01-15
url: https://github.com/climate/analyzer
```

**2. README or Documentation**

Look for a "How to Cite" or "Citation" section.

**3. Software Paper**

Many projects publish a paper specifically about the software (often in journals like JOSS - Journal of Open Source Software, or SoftwareX).

**4. GitHub Citation Feature**

GitHub has a "Cite this repository" feature in the sidebar that generates formatted citations.

**5. DOI (Digital Object Identifier)**

Software archived on Zenodo or Figshare receives a DOI that can be cited.

**Citation Formats**

**In-Text Citation (Paper):**
```
We analyzed climate data using the Climate Data Analyzer package (Smith, 2024).

All statistical analyses were performed using SciPy version 1.7.1 (Virtanen et al., 2020).
```

**Reference List Formats:**

**Software with DOI:**
```
Smith, J. (2024). Climate Data Analyzer (Version 2.3.1) [Computer software]. 
https://doi.org/10.5281/zenodo.1234567
```

**Software Paper:**
```
Smith, J., Jones, A., & Brown, B. (2024). Climate Data Analyzer: An open-source 
Python package for climate data analysis. Journal of Open Source Software, 9(95), 1234. 
https://doi.org/10.21105/joss.01234
```

**Software without DOI:**
```
Smith, J. (2024). Climate Data Analyzer (Version 2.3.1) [Computer software]. 
GitHub. https://github.com/climate/analyzer
```

**BibTeX Format:**
```bibtex
@software{smith2024climate,
  author = {Smith, Jane},
  title = {Climate Data Analyzer},
  version = {2.3.1},
  year = {2024},
  url = {https://github.com/climate/analyzer},
  doi = {10.5281/zenodo.1234567}
}
```

**Citation in Code Comments:**

```python
# Analysis uses Climate Data Analyzer v2.3.1
# Citation: Smith, J. (2024). Climate Data Analyzer. 
#           https://doi.org/10.5281/zenodo.1234567
import climate_analyzer as ca

results = ca.analyze_trends(data)
```

**Software Management Plans and Documentation:**

Include a software dependency list in your documentation:

```markdown
## Software Dependencies

This analysis relies on the following open-source software:

| Package | Version | Purpose | Citation |
|---------|---------|---------|----------|
| NumPy | 1.21.2 | Array operations | Harris et al. (2020) |
| Pandas | 1.3.3 | Data manipulation | McKinney (2010) |
| Climate Analyzer | 2.3.1 | Climate data processing | Smith (2024) |

### Full Citations

Harris, C. R., Millman, K. J., van der Walt, S. J., et al. (2020). 
Array programming with NumPy. Nature, 585, 357-362. 
https://doi.org/10.1038/s41586-020-2649-2

McKinney, W. (2010). Data structures for statistical computing in Python. 
Proceedings of the 9th Python in Science Conference, 51-56.

Smith, J. (2024). Climate Data Analyzer (Version 2.3.1). 
https://doi.org/10.5281/zenodo.1234567
```

#### 2.5 Acknowledging Open Code Contributions

Beyond formal citation, there are other ways to acknowledge and support open-source software:

**In Publications:**
- List software in an acknowledgments section
- Include version numbers for all software used
- Mention key contributors by name when appropriate

**Example Acknowledgments Section:**
```
We thank the developers of the Climate Data Analyzer (Smith et al., 2024), 
particularly Jane Smith and the community contributors, for creating and 
maintaining this valuable tool. Data analysis was performed using Python 3.9 
and the following packages: NumPy 1.21.2, Pandas 1.3.3, and Matplotlib 3.4.3.
```

**Contributing Back:**

**Report Bugs:**
- If you find a bug, report it through the project's issue tracker
- Include:
  - Clear description of the problem
  - Steps to reproduce
  - Your environment (OS, software versions)
  - Minimal code example demonstrating the issue

**Example Bug Report:**
```markdown
## Bug: Incorrect calculation for negative values

**Environment:**
- climate_analyzer version: 2.3.1
- Python version: 3.9.7
- OS: Ubuntu 20.04

**Description:**
The `calculate_anomaly` function returns incorrect results when input 
contains negative temperature values.

**Steps to Reproduce:**
```python
import climate_analyzer as ca
data = [-5.0, -3.0, -1.0, 2.0]
result = ca.calculate_anomaly(data)
print(result)  # Expected: [some values], Got: [NaN, NaN, NaN, NaN]
```

**Expected behavior:**
Function should handle negative values correctly.
```

**Suggest Improvements:**
- Feature requests are welcome in most projects
- Check if feature has already been requested
- Explain the use case and benefit

**Submit Documentation Fixes:**
- Fix typos or unclear explanations
- Add examples for underdocumented features
- Often the easiest way to start contributing

**Contribute Code:**
- Fix bugs you've found
- Implement requested features
- Follow the project's contribution guidelines

**Share Your Experience:**
- Write blog posts about using the software
- Present about it at conferences
- Recommend it to colleagues
- Star/favorite the repository

**Financial Support:**
- Some projects accept donations or sponsorships
- Platforms like GitHub Sponsors, Open Collective, or Patreon
- Grants and funding acknowledgments

**Example: Complete Workflow of Using Open Code**

A researcher needs to analyze genomic sequences:

1. **Discovery:** Searches GitHub and bio.tools, finds BioPython
2. **Assessment:** 
   - Reads documentation (excellent)
   - Checks license (BSD - permissive)
   - Sees active maintenance (recent commits, responsive issues)
   - Highly cited (thousands of papers)
3. **Installation:** 
   ```bash
   conda install -c conda-forge biopython
   ```
4. **Integration:**
   ```python
   from Bio import SeqIO
   from Bio.Seq import Seq
   
   # Parse sequence file
   for record in SeqIO.parse("sequences.fasta", "fasta"):
       print(f"ID: {record.id}")
       print(f"Length: {len(record.seq)}")
   ```
5. **Documentation:** Adds BioPython to requirements.txt with version number
6. **Citation:** Includes citation in paper:
   ```
   Cock, P. J. A., et al. (2009). Biopython: freely available Python tools 
   for computational molecular biology and bioinformatics. Bioinformatics, 
   25(11), 1422-1423.
   ```
7. **Acknowledgment:** Thanks developers in acknowledgments section
8. **Contribution:** Reports a minor documentation typo via GitHub issue

#### Summary

Using existing open code effectively involves:
1. **Discovering** relevant software through repositories, registries, and community recommendations
2. **Assessing** code quality by evaluating documentation, licensing, activity, and community support
3. **Reusing** code responsibly with proper version management, testing, and integration practices
4. **Citing** software appropriately to give credit and enable reproducibility
5. **Acknowledging** and supporting developers through various contributions and recognition

By following these practices, researchers can leverage the power of open-source software while contributing to a sustainable and collaborative scientific ecosystem.

### Lesson 3: Making Open Code

#### Overview
In this lesson, you will learn about the practical steps to make code openly accessible. Large volume and well-established software have different needs than an incipient project. For example, a script written to create a simple plot has different requirements than a software package that models the Earth's climate. The size of a research team can also determine the steps required to make code open access. This lesson covers the process to make code usable to other researchers through documentation, considerations around licenses, and software development best practices.

#### 3.1 Levels of Open Code Projects

Different projects require different levels of formality and infrastructure. Understanding where your project fits helps determine appropriate practices.

**Level 1: Personal Scripts and Analysis Code**

**Characteristics:**
- Single researcher or small team
- Specific to one analysis or paper
- May not be intended for reuse by others
- Often one-time or infrequently updated

**Minimum Requirements:**
- Clear file naming and organization
- Comments explaining key steps
- README with basic description
- Requirements/dependencies listed
- License file

**Example:**
```
my-analysis/
├── README.md
├── LICENSE
├── requirements.txt
├── data/
│   └── README.md (explains data sources)
├── scripts/
│   ├── 01_data_preparation.py
│   ├── 02_analysis.py
│   └── 03_visualization.py
├── results/
│   └── figures/
└── notebooks/
    └── exploratory_analysis.ipynb
```

**Level 2: Research Software Tool**

**Characteristics:**
- Intended for use by others
- May have multiple collaborators
- Updated periodically with new features
- Associated with publications

**Additional Requirements:**
- Installation instructions
- Usage examples and tutorials
- Documented functions/classes
- Basic test suite
- Version control best practices
- Issue tracking

**Example Structure:**
```
research-tool/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── setup.py or pyproject.toml
├── requirements.txt
├── docs/
│   ├── installation.md
│   ├── quickstart.md
│   ├── tutorial.md
│   └── api.md
├── src/
│   └── research_tool/
│       ├── __init__.py
│       ├── core.py
│       ├── utils.py
│       └── visualize.py
├── tests/
│   ├── test_core.py
│   └── test_utils.py
└── examples/
    ├── basic_usage.py
    └── advanced_example.py
```

**Level 3: Community Software Package**

**Characteristics:**
- Many users and contributors
- Ongoing development
- Part of research infrastructure
- May have funding or institutional support

**Additional Requirements:**
- Comprehensive documentation
- Automated testing and CI/CD
- Code review process
- Governance model
- Release management
- Community guidelines
- Security policies

**Example: Well-Established Project Structure:**
```
large-project/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── GOVERNANCE.md
├── setup.py
├── pyproject.toml
├── .github/
│   ├── workflows/  (CI/CD)
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
├── docs/
│   ├── (full documentation site)
├── src/
├── tests/
├── benchmarks/
└── examples/
```

#### 3.2 Code Documentation

Good documentation is the key to making code usable by others (and your future self).

**3.2.1 README Files**

The README is the first thing people see. It should answer:
- What does this code do?
- Why would I use it?
- How do I install it?
- How do I use it?
- Who maintains it?
- How can I contribute?

**Essential README Sections:**

```markdown
# Project Title

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)

Brief one-paragraph description of what this code does and why it exists.

## Features

- Key feature 1
- Key feature 2
- Key feature 3

## Installation

```bash
pip install your-package-name
```

Or from source:
```bash
git clone https://github.com/username/project.git
cd project
pip install -e .
```

## Quick Start

```python
import your_package as yp

# Simple example showing basic usage
data = yp.load_data('example.csv')
results = yp.analyze(data)
yp.plot(results)
```

## Documentation

Full documentation is available at [link to documentation].

## Requirements

- Python >= 3.8
- NumPy >= 1.20
- Pandas >= 1.3

## Citation

If you use this software, please cite:

```bibtex
@software{yourname2024,
  author = {Your Name},
  title = {Project Title},
  year = {2024},
  url = {https://github.com/username/project},
  doi = {10.5281/zenodo.xxxxx}
}
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) 
for guidelines.

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) 
for details.

## Contact

- Author: Your Name (email@institution.edu)
- Issues: https://github.com/username/project/issues
```

**3.2.2 Code Comments**

Comments should explain **why**, not what. The code shows what; comments explain reasoning.

**Bad Comments:**
```python
# Add 1 to x
x = x + 1

# Loop through items
for item in items:
    # Print item
    print(item)
```

**Good Comments:**
```python
# Adjust for 1-based indexing used in the source dataset
x = x + 1

# Process each sample separately due to memory constraints
# with large datasets (>10GB)
for item in items:
    process_item(item)
```

**Function Documentation (Docstrings):**

Python example using NumPy style:

```python
def calculate_species_diversity(abundance_data, method='shannon'):
    """
    Calculate species diversity index from abundance data.
    
    This function computes diversity indices commonly used in ecology
    to quantify biodiversity in a community.
    
    Parameters
    ----------
    abundance_data : array-like, shape (n_species,)
        Number of individuals observed for each species.
        Must contain non-negative integers.
    method : {'shannon', 'simpson', 'richness'}, default='shannon'
        The diversity index to calculate:
        - 'shannon': Shannon-Wiener diversity index (entropy-based)
        - 'simpson': Simpson's diversity index (probability-based)
        - 'richness': Species richness (simple count)
    
    Returns
    -------
    diversity : float
        The calculated diversity index value.
        Higher values indicate greater diversity.
    
    Raises
    ------
    ValueError
        If abundance_data contains negative values or if method is invalid.
    
    Examples
    --------
    >>> abundance = [50, 30, 20, 15, 10]
    >>> calculate_species_diversity(abundance, method='shannon')
    1.4854752972273344
    
    >>> calculate_species_diversity(abundance, method='richness')
    5.0
    
    Notes
    -----
    The Shannon diversity index is calculated as:
    
    .. math:: H' = -\sum_{i=1}^{S} p_i \ln(p_i)
    
    where S is the number of species and p_i is the proportion of 
    individuals belonging to species i.
    
    References
    ----------
    .. [1] Shannon, C. E. (1948). A mathematical theory of communication.
           Bell System Technical Journal, 27(3), 379-423.
    """
    abundance_data = np.asarray(abundance_data)
    
    if np.any(abundance_data < 0):
        raise ValueError("Abundance data cannot contain negative values")
    
    if method == 'shannon':
        # Remove zeros to avoid log(0)
        nonzero = abundance_data[abundance_data > 0]
        proportions = nonzero / nonzero.sum()
        return -np.sum(proportions * np.log(proportions))
    elif method == 'simpson':
        proportions = abundance_data / abundance_data.sum()
        return 1 - np.sum(proportions ** 2)
    elif method == 'richness':
        return np.count_nonzero(abundance_data)
    else:
        raise ValueError(f"Unknown method: {method}")
```

**3.2.3 External Documentation**

**Types of Documentation:**

1. **Installation Guide**
   - System requirements
   - Step-by-step installation
   - Common issues and solutions
   - Verification steps

2. **Quick Start Tutorial**
   - Minimal working example
   - 5-10 minutes to complete
   - Covers most common use case

3. **User Guide**
   - Comprehensive usage instructions
   - Organized by task or feature
   - Multiple examples

4. **API Reference**
   - Complete list of all functions/classes
   - Generated from docstrings
   - Searchable

5. **Developer Guide**
   - How to contribute
   - Code architecture
   - Development workflow

**Documentation Tools:**

- **Python:** Sphinx, MkDocs, pdoc
- **R:** pkgdown, roxygen2
- **Hosting:** Read the Docs, GitHub Pages

**Example: Using Sphinx for Python Documentation**

```bash
# Install Sphinx
pip install sphinx

# Create docs directory and initialize
mkdir docs
cd docs
sphinx-quickstart

# Build HTML documentation
make html
```

#### 3.3 Choosing and Applying Licenses

Licensing is a critical legal aspect of open code. Without a license, code is technically copyrighted and others cannot legally use it.

**Why Licensing Matters:**
- Provides legal clarity for users
- Specifies permitted uses
- Protects developers from liability
- Ensures proper attribution
- Enables reproducibility

**Common Open-Source Licenses Compared:**

| License | Type | Commercial Use | Modification | Distribution | Share-Alike Required | Patent Grant |
|---------|------|----------------|--------------|--------------|---------------------|-------------|
| MIT | Permissive | ✅ | ✅ | ✅ | ❌ | ❌ |
| Apache 2.0 | Permissive | ✅ | ✅ | ✅ | ❌ | ✅ |
| BSD 3-Clause | Permissive | ✅ | ✅ | ✅ | ❌ | ❌ |
| GPL 3.0 | Copyleft | ✅ | ✅ | ✅ | ✅ | ✅ |
| LGPL 3.0 | Weak Copyleft | ✅ | ✅ | ✅ | ⚠️ (for library itself) | ✅ |
| AGPL 3.0 | Strong Copyleft | ✅ | ✅ | ✅ | ✅ (even for network use) | ✅ |

**Choosing a License: Decision Tree**

1. **Do you want to require that derivatives also be open source?**
   - YES → Consider GPL, LGPL, or AGPL (Copyleft)
   - NO → Consider MIT, Apache 2.0, or BSD (Permissive)

2. **Is patent protection important?**
   - YES → Consider Apache 2.0 or GPL 3.0
   - NO → MIT or BSD may be sufficient

3. **Will the code be used as a library or web service?**
   - Library → Consider LGPL (allows use in proprietary software)
   - Web service → Consider AGPL (copyleft applies to network use)
   - Standalone → GPL or permissive licenses

4. **Do you need compatibility with specific ecosystems?**
   - Some projects require specific licenses
   - Check requirements of dependencies

**License Recommendations by Field:**

- **Academic Research:** MIT or Apache 2.0 (maximize reusability)
- **Community Projects:** GPL 3.0 (ensure derivatives stay open)
- **Libraries:** MIT, Apache 2.0, or LGPL (enable broad adoption)
- **Data Analysis Scripts:** MIT (simple and permissive)

**How to Apply a License:**

**Step 1: Add LICENSE file to repository root**

```bash
# Download license text
curl -o LICENSE https://opensource.org/licenses/MIT

# Or use GitHub's interface when creating repository
```

**Step 2: Update LICENSE file with your information**

```
MIT License

Copyright (c) 2024 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

**Step 3: Add license header to source files (optional but recommended)**

```python
# Copyright (c) 2024 Your Name
# Licensed under the MIT License
# See LICENSE file in the project root for full license information.

import numpy as np
...
```

**Step 4: Mention license in README**

```markdown
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) 
file for details.
```

**Multiple Licenses:**

Some projects use different licenses for different components:

```
project/
├── LICENSE (code: MIT)
├── LICENSE-DATA (data: CC BY 4.0)
└── LICENSE-DOCS (documentation: CC BY 4.0)
```

**License Compatibility:**

When using code from multiple sources, ensure licenses are compatible:

✅ **Compatible:**
- MIT + Apache 2.0
- BSD + MIT
- MIT → GPL (can incorporate MIT code into GPL project)

❌ **Incompatible:**
- GPL ← MIT (cannot incorporate GPL code into MIT project without changing to GPL)
- GPL + Apache 2.0 (GPLv2 specifically)

#### 3.4 Software Development Best Practices

Following established best practices makes code more maintainable, reliable, and reusable.

**3.4.1 Code Style and Formatting**

Consistent style improves readability.

**Use Style Guides:**
- **Python:** PEP 8
- **R:** Tidyverse style guide
- **JavaScript:** Airbnb style guide
- **C++:** Google C++ style guide

**Automated Formatting Tools:**

```bash
# Python: black
pip install black
black your_code.py

# Python: autopep8
pip install autopep8
autopep8 --in-place --aggressive your_code.py

# R: styler
install.packages("styler")
styler::style_file("your_code.R")
```

**Example: Before and After Formatting**

**Before:**
```python
def calculate(x,y,z):
    result=x+y*z
    if result>100:
        return result
    else:
        return 0
```

**After:**
```python
def calculate(x, y, z):
    """Calculate x + y * z with threshold."""
    result = x + y * z
    
    if result > 100:
        return result
    else:
        return 0
```

**3.4.2 Version Control Best Practices**

**Commit Messages:**

Write clear, descriptive commit messages:

**Bad:**
```
fixed bug
updated code
changes
```

**Good:**
```
Fix: Correct calculation error in diversity index

The Shannon diversity calculation was using log2 instead of natural log,
resulting in incorrect values. Updated to use np.log() and added test
case to prevent regression.

Closes #42
```

**Commit Message Format:**
```
<type>: <short summary> (max 50 characters)

<detailed description explaining what and why> (wrap at 72 characters)

<references to issues/PRs>
```

**Types:** `Fix`, `Feature`, `Docs`, `Style`, `Refactor`, `Test`, `Chore`

**Branching Strategy:**

```
main (or master) - production-ready code
├── develop - integration branch
│   ├── feature/new-analysis
│   ├── feature/add-plots
│   └── bugfix/issue-42
└── release/v1.2
```

**Workflow:**
```bash
# Create feature branch
git checkout -b feature/new-analysis

# Make changes and commit
git add .
git commit -m "Feature: Add new analysis method"

# Push to remote
git push origin feature/new-analysis

# Create pull request on GitHub/GitLab
# After review and approval, merge to develop
```

**3.4.3 Testing**

Tests verify that code works correctly and prevent regressions.

**Types of Tests:**

**1. Unit Tests** - Test individual functions

```python
import pytest
import numpy as np
from mypackage import calculate_mean

def test_calculate_mean_basic():
    """Test mean calculation with simple data."""
    data = [1, 2, 3, 4, 5]
    result = calculate_mean(data)
    assert result == 3.0

def test_calculate_mean_empty():
    """Test that empty data returns None."""
    data = []
    result = calculate_mean(data)
    assert result is None

def test_calculate_mean_float():
    """Test mean with floating point data."""
    data = [1.5, 2.5, 3.5]
    result = calculate_mean(data)
    assert np.isclose(result, 2.5)

def test_calculate_mean_negative():
    """Test mean with negative values."""
    data = [-2, -1, 0, 1, 2]
    result = calculate_mean(data)
    assert result == 0.0
```

**2. Integration Tests** - Test multiple components together

```python
def test_full_analysis_pipeline():
    """Test complete analysis from data loading to output."""
    # Load test data
    data = load_data('tests/data/test_input.csv')
    
    # Run preprocessing
    cleaned = preprocess(data)
    
    # Run analysis
    results = analyze(cleaned)
    
    # Verify output format and values
    assert 'mean' in results
    assert 'std' in results
    assert results['mean'] > 0
```

**3. Regression Tests** - Ensure bugs don't reappear

```python
def test_issue_42_negative_value_bug():
    """Regression test for Issue #42: negative values caused crash."""
    # This used to crash, ensure it's fixed
    data = [-5, -3, -1, 0, 1]
    result = calculate_diversity(data)  # Should not raise error
    assert result is not None
```

**Running Tests:**

```bash
# Install pytest
pip install pytest pytest-cov

# Run all tests
pytest

# Run with coverage report
pytest --cov=mypackage tests/

# Run specific test file
pytest tests/test_analysis.py

# Run tests matching pattern
pytest -k "test_mean"
```

**Test Coverage:**

Aim for >80% code coverage for critical code:

```bash
pytest --cov=mypackage --cov-report=html
# Opens coverage report showing which lines are tested
```

**3.4.4 Continuous Integration (CI)**

Automatically run tests when code is pushed.

**GitHub Actions Example:**

`.github/workflows/tests.yml`:

```yaml
name: Tests

on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main, develop ]

jobs:
  test:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: [3.8, 3.9, '3.10', 3.11]
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Python ${{ matrix.python-version }}
      uses: actions/setup-python@v4
      with:
        python-version: ${{ matrix.python-version }}
    
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt
        pip install pytest pytest-cov
    
    - name: Run tests
      run: |
        pytest --cov=mypackage tests/
    
    - name: Upload coverage
      uses: codecov/codecov-action@v3
```

**3.4.5 Code Review**

Peer review improves code quality and shares knowledge.

**Pull Request Template:**

`.github/PULL_REQUEST_TEMPLATE.md`:

```markdown
## Description

Briefly describe the changes in this PR.

## Type of Change

- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Code refactoring

## Checklist

- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added to complex code
- [ ] Documentation updated
- [ ] Tests added/updated
- [ ] All tests pass locally
- [ ] No new warnings generated

## Testing

Describe the tests you ran and how to reproduce.

## Related Issues

Closes #(issue number)
```

**Code Review Best Practices:**

**For Authors:**
- Keep PRs small and focused
- Write clear descriptions
- Respond to feedback constructively
- Add reviewers who know the code

**For Reviewers:**
- Be respectful and constructive
- Focus on substantive issues, not just style
- Suggest improvements with examples
- Approve when satisfied, don't nitpick

**Example Review Comment:**
```markdown
Consider using numpy's built-in function here for better performance:

```python
# Instead of:
result = sum([x**2 for x in data]) / len(data)

# Consider:
result = np.mean(np.square(data))
```

This is both more readable and about 10x faster for large arrays.
```

#### 3.5 Project Organization and Structure

**Organizing Files:**

A well-organized project structure makes code easier to navigate and maintain.

**Standard Python Project Structure:**

```
my-project/
├── README.md              # Project overview
├── LICENSE                # License file
├── setup.py              # Installation script
├── pyproject.toml        # Modern Python config
├── requirements.txt       # Dependencies
├── .gitignore            # Git ignore patterns
├── .github/              # GitHub-specific files
│   ├── workflows/        # CI/CD workflows
│   └── ISSUE_TEMPLATE/   # Issue templates
├── docs/                 # Documentation
│   ├── conf.py          # Sphinx configuration
│   ├── index.rst        # Documentation home
│   └── tutorials/       # Tutorial files
├── src/                  # Source code
│   └── myproject/
│       ├── __init__.py
│       ├── core.py       # Core functionality
│       ├── utils.py      # Utility functions
│       └── data/        # Package data
├── tests/                # Test files
│   ├── __init__.py
│   ├── test_core.py
│   └── test_utils.py
├── examples/             # Example scripts
│   ├── basic_usage.py
│   └── advanced.py
└── scripts/              # Utility scripts
    └── prepare_data.sh
```

**File Naming Conventions:**
- Use lowercase with underscores: `data_processing.py`
- Be descriptive: `calculate_diversity.py` not `calc.py`
- Group related files in directories
- Use consistent naming across project

**Configuration Files:**

**setup.py** for Python packages:

```python
from setuptools import setup, find_packages

with open("README.md", "r", encoding="utf-8") as fh:
    long_description = fh.read()

setup(
    name="my-analysis-package",
    version="1.0.0",
    author="Your Name",
    author_email="your.email@institution.edu",
    description="A package for analyzing climate data",
    long_description=long_description,
    long_description_content_type="text/markdown",
    url="https://github.com/yourusername/my-analysis-package",
    project_urls={
        "Bug Tracker": "https://github.com/yourusername/my-analysis-package/issues",
        "Documentation": "https://my-analysis-package.readthedocs.io",
    },
    classifiers=[
        "Development Status :: 4 - Beta",
        "Intended Audience :: Science/Research",
        "Topic :: Scientific/Engineering :: Atmospheric Science",
        "License :: OSI Approved :: MIT License",
        "Programming Language :: Python :: 3",
        "Programming Language :: Python :: 3.8",
        "Programming Language :: Python :: 3.9",
        "Programming Language :: Python :: 3.10",
    ],
    packages=find_packages(where="src"),
    package_dir={"" : "src"},
    python_requires=">=3.8",
    install_requires=[
        "numpy>=1.20",
        "pandas>=1.3",
        "matplotlib>=3.3",
    ],
    extras_require={
        "dev": ["pytest>=6.0", "sphinx>=4.0", "black>=22.0"],
        "test": ["pytest>=6.0", "pytest-cov>=2.0"],
    },
)
```

**.gitignore** - What not to commit:

```
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/
*.egg-info/
dist/
build/

# IDEs
.vscode/
.idea/
*.swp

# Data (unless small test data)
data/*.csv
data/*.nc

# Results
results/
figures/*.png
*.log

# Secrets
.env
secrets.json
config_local.py

# OS
.DS_Store
Thumbs.db
```

#### 3.6 From Script to Package

Turning analysis scripts into an installable package makes code more reusable.

**Evolution Example:**

**Stage 1: Single Script**
```python
# analysis.py
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv('data.csv')
mean_val = data['temperature'].mean()
print(f"Mean: {mean_val}")
plt.plot(data['temperature'])
plt.show()
```

**Stage 2: Organized Scripts**
```python
# load_data.py
import pandas as pd

def load_temperature_data(filepath):
    return pd.read_csv(filepath)

# analyze.py
import numpy as np

def calculate_statistics(data):
    return {
        'mean': np.mean(data),
        'std': np.std(data),
        'min': np.min(data),
        'max': np.max(data)
    }

# main.py
from load_data import load_temperature_data
from analyze import calculate_statistics
import plot

data = load_temperature_data('data.csv')
stats = calculate_statistics(data['temperature'])
print(stats)
plot.plot_timeseries(data)
```

**Stage 3: Package Structure**
```
climate_analysis/
├── setup.py
├── README.md
├── LICENSE
├── src/
│   └── climate_analysis/
│       ├── __init__.py
│       ├── io.py          # Data loading
│       ├── stats.py       # Statistical functions
│       ├── plotting.py    # Visualization
│       └── utils.py       # Utilities
├── tests/
│   └── test_stats.py
└── examples/
    └── basic_analysis.py
```

**__init__.py** - Package interface:
```python
"""Climate data analysis package."""

__version__ = "1.0.0"

from .io import load_temperature_data, load_precipitation_data
from .stats import calculate_statistics, calculate_trends
from .plotting import plot_timeseries, plot_spatial

__all__ = [
    'load_temperature_data',
    'load_precipitation_data', 
    'calculate_statistics',
    'calculate_trends',
    'plot_timeseries',
    'plot_spatial',
]
```

**Using the package:**
```python
# After: pip install climate_analysis
import climate_analysis as ca

data = ca.load_temperature_data('mydata.csv')
stats = ca.calculate_statistics(data)
ca.plot_timeseries(data)
```

#### Summary

Making code open and reusable requires:

1. **Understanding project scale** - Different projects need different levels of formality
2. **Comprehensive documentation** - README, comments, docstrings, and external docs
3. **Appropriate licensing** - Choose a license that matches your goals and apply it correctly
4. **Best practices** - Follow style guides, use version control effectively, write tests, and implement CI
5. **Good organization** - Structure projects logically with clear file organization
6. **Progression** - Start simple and add complexity as needed, potentially evolving scripts into packages

By following these practices, you make your code accessible, understandable, and reusable by the broader research community.

### Lesson 4: Sharing Open Code

#### Overview
In this lesson you learn the steps for sharing the software that you developed. These steps include determining if, when, and where software should be shared, which roles are needed, and how to enable others to use the code. Sharing is the final critical step that makes your code available to the broader research community and ensures its long-term preservation.

#### 4.1 Determining If Code Should Be Shared

Not all code can or should be shared publicly, but the default should be openness whenever possible.

**When Code SHOULD Be Shared:**

✅ **Code supporting published research**
- Essential for reproducibility
- Often required by journals and funders
- Benefits the scientific community

✅ **General-purpose tools**
- Useful beyond your specific project
- Can benefit multiple researchers
- Reduces redundant development

✅ **Educational code**
- Tutorials and teaching materials
- Example implementations
- Learning resources

✅ **Community-requested tools**
- Fills a gap in available software
- Addresses common problems

**When Code MAY NOT Be Shareable:**

⚠️ **Security-sensitive code**
- Contains encryption or security mechanisms
- Could reveal vulnerabilities
- **Solution:** Share algorithms/methods without sensitive implementation details

⚠️ **Export-controlled technology**
- Subject to government export restrictions
- Contains controlled cryptography
- **Solution:** Consult institution's export control office; may need licensing

⚠️ **Proprietary dependencies**
- Relies on commercial software that can't be redistributed
- Uses proprietary APIs or libraries
- **Solution:** Share code with clear documentation of proprietary requirements, or create open alternatives

⚠️ **Protected data concerns**
- Code contains embedded private/sensitive data
- **Solution:** Separate data from code; share code with synthetic/example data

⚠️ **Intellectual property restrictions**
- Institution has filed patent or plans to commercialize
- Industry partnership has confidentiality agreements
- **Solution:** Work with tech transfer office; may allow sharing after embargo or with certain license restrictions

⚠️ **Code quality concerns**
- "It's too messy to share"
- **Response:** This is rarely a valid reason not to share. Imperfect code is better than no code. Add a disclaimer about code status.

**Decision Framework:**

```
Start: Should I share this code?
    |
    ├─→ Is it required for published research? ──YES→ MUST SHARE
    |
    ├─→ Are there legal/security restrictions? ──YES→ Consult compliance office
    │                                             |
    │                                             ├─→ Approved with conditions
    │                                             │   └→ SHARE with appropriate license/restrictions
    │                                             └─→ Cannot share
    │                                                 └→ Document why + share what you can
    |
    ├─→ Does it contain sensitive data/credentials? ──YES→ Clean and sanitize
    │                                                  └→ Then SHARE
    |
    └─→ No major blockers? ──YES→ SHARE
```

**Example Scenarios:**

**Scenario 1: Analysis script for published paper**
- **Decision:** Share immediately upon publication
- **Action:** Upload to GitHub, archive on Zenodo, cite in paper

**Scenario 2: Tool using proprietary software**
- **Decision:** Share with clear documentation
- **Action:** Share code on GitHub with README noting: "Requires MATLAB license" or "Requires ArcGIS Pro"

**Scenario 3: Code with embedded passwords**
- **Decision:** Share after cleaning
- **Action:** Remove credentials, add config file template, share cleaned version

**Scenario 4: Patent pending**
- **Decision:** Embargoed sharing
- **Action:** Work with tech transfer to share after patent filing or with appropriate license

#### 4.2 Determining When to Share

**Timing Options:**

**1. Immediate/Continuous Sharing (Open from Start)**

**When appropriate:**
- No competitive concerns
- Collaborative projects
- Community-driven development
- Educational projects

**Advantages:**
- Maximum transparency
- Early feedback
- Build community from start
- Easier than retrofitting openness

**Disadvantages:**
- Development process visible (including mistakes)
- May receive premature criticism

**Example:** A research group developing climate analysis tools shares code on GitHub from day one, accepts community contributions throughout development.

**2. Share at Publication**

**When appropriate:**
- Competitive research environment
- Want to publish findings first
- Need time to clean and document
- Standard practice in field

**Advantages:**
- Protects competitive advantage
- Time to prepare code properly
- Aligns with paper publication
- Common expectation

**Disadvantages:**
- Delayed community benefit
- Requires more work at end
- Less community testing

**Example:** Researchers upload code to GitHub and archive on Zenodo upon paper acceptance, including DOI in final manuscript.

**3. Embargoed Release**

**When appropriate:**
- Funder or institution requires embargo period
- Patent application pending
- Multi-paper project

**Advantages:**
- Balances openness with protection
- Clear timeline

**Disadvantages:**
- Delayed access
- Must maintain private repository

**Example:** Code marked for public release 6 months after paper publication or upon patent filing.

**4. Staged Release**

**When appropriate:**
- Large, complex projects
- Need to clean components separately
- Multiple collaborators with different timelines

**Advantages:**
- Share what's ready when it's ready
- Manageable workload

**Disadvantages:**
- Incomplete initially
- May confuse users

**Example:** Release core analysis package first, add visualization tools three months later, add data processing utilities after that.

**Best Practice Recommendations:**

- **Default to early sharing** when possible
- **At minimum, share at publication** - this is increasingly required
- **Communicate timeline** - If embargo planned, state when code will be available
- **Archive specific versions** - When publishing paper, archive the exact version used

#### 4.3 Determining Where to Share

Choosing the right platform(s) depends on your goals, audience, and resources.

**Platform Comparison:**

**Version Control Repositories**

**GitHub (github.com)**
- **Pros:** Largest community, excellent tools, free for open source, CI/CD integration, discoverability
- **Cons:** Owned by Microsoft, requires git knowledge
- **Best for:** Active development, collaboration, community projects
- **Features:** Issues, pull requests, Actions (CI/CD), GitHub Pages, releases

**GitLab (gitlab.com)**
- **Pros:** Similar to GitHub, can self-host, integrated CI/CD, free private repos
- **Cons:** Smaller community than GitHub
- **Best for:** Projects needing self-hosting, institutional use

**Bitbucket (bitbucket.org)**
- **Pros:** Free private repos, good for teams, Jira integration
- **Cons:** Smaller community, less discovery
- **Best for:** Private team projects, Atlassian ecosystem users

**Archival Repositories**

**Zenodo (zenodo.org)**
- **Pros:** Free DOIs, permanent storage, versioning, CERN infrastructure, integrates with GitHub
- **Cons:** Not for active development
- **Best for:** Archiving releases, citable versions
- **Example DOI:** 10.5281/zenodo.1234567

**Software Heritage (softwareheritage.org)**
- **Pros:** Preserves all public code, free, comprehensive archive
- **Cons:** Automatic archiving (not manual submission)
- **Best for:** Long-term preservation

**Figshare (figshare.com)**
- **Pros:** Free DOIs, various data types, institutional instances
- **Cons:** Less code-specific than Zenodo
- **Best for:** Mixed outputs (code + data + papers)

**Package Registries**

**PyPI - Python Package Index (pypi.org)**
- **Pros:** Standard Python distribution, pip installable, searchable
- **Cons:** Requires proper package structure
- **Best for:** Python packages intended for widespread use
- **Installation:** `pip install your-package`

**CRAN - Comprehensive R Archive Network (cran.r-project.org)**
- **Pros:** Standard R distribution, quality control, trusted
- **Cons:** Strict requirements, review process
- **Best for:** Mature R packages
- **Installation:** `install.packages("yourpackage")`

**Conda-forge (conda-forge.org)**
- **Pros:** Cross-platform, handles non-Python dependencies, popular in data science
- **Cons:** Requires conda recipe
- **Best for:** Scientific Python packages
- **Installation:** `conda install -c conda-forge your-package`

**npm (npmjs.com)**
- **Pros:** Standard JavaScript distribution
- **Cons:** JavaScript ecosystem only
- **Best for:** JavaScript/Node.js packages

**Domain-Specific Repositories**

**Astrophysics Source Code Library (ASCL - ascl.net)**
- Astronomy-specific software
- Indexed, citable

**bio.tools**
- Bioinformatics tools registry
- Standardized descriptions

**CoMSES Net (comses.net)**
- Computational modeling in social and ecological sciences

**Recommended Multi-Platform Strategy:**

**Typical Workflow:**

1. **Development:** GitHub/GitLab
   - Active code development
   - Issue tracking
   - Community contributions

2. **Distribution:** Package Registry (PyPI, CRAN, etc.)
   - Easy installation
   - Version management
   - Dependency handling

3. **Archival:** Zenodo
   - Permanent DOI
   - Specific version used in paper
   - Long-term preservation

4. **Discovery:** Domain-specific registry
   - Field-specific visibility
   - Specialized metadata

**Example: Python Package Sharing Strategy**

```bash
# 1. Develop on GitHub
git push origin main

# 2. Create release on GitHub
git tag -a v1.0.0 -m "First release"
git push origin v1.0.0

# 3. Publish to PyPI
python -m build
twine upload dist/*

# 4. Archive on Zenodo (automatic via GitHub integration)
# Zenodo creates DOI for the release

# 5. Submit to domain registry
# Fill out form on bio.tools or other relevant registry
```

**Institutional Repositories**

Many universities have institutional repositories:
- **Pros:** Institutional support, preservation, meets funder requirements
- **Cons:** Less discoverable, limited functionality
- **Best for:** Meeting institutional requirements, supplementing other platforms

**Personal/Lab Websites**
- **Pros:** Full control, can include context
- **Cons:** Not sustainable, not discoverable, no preservation
- **Recommendation:** Use as supplement, not primary location

#### 4.4 Roles in Open Code Projects

Clear roles and responsibilities help projects run smoothly.

**Role Definitions:**

**1. Lead Developer / Principal Investigator**
- Sets project vision and direction
- Makes final decisions on major changes
- Secures funding and resources
- Represents project in academic contexts

**2. Core Developer / Maintainer**
- Writes and reviews code
- Manages releases
- Responds to issues and pull requests
- Maintains code quality
- Updates documentation

**Typical commitment:** 5-20 hours/week for active projects

**3. Contributor**
- Submits bug fixes or features
- Reports issues
- Improves documentation
- No ongoing commitment required

**4. Reviewer**
- Reviews pull requests
- Provides feedback on code quality
- Tests proposed changes

**5. Community Manager**
- Moderates discussions
- Welcomes new contributors
- Maintains code of conduct
- Organizes community events

**6. Documentation Lead**
- Maintains documentation
- Writes tutorials
- Ensures docs stay current

**7. User / Tester**
- Uses the software
- Reports bugs
- Provides feedback
- No technical contribution required

**Governance Models:**

**Single Maintainer**
- One person makes all decisions
- Common for small projects
- Simple but not sustainable long-term

**Core Team**
- Small group of trusted maintainers
- Decisions by consensus or voting
- Common for medium projects

**Meritocracy**
- Contributors gain privileges over time
- Based on contributions and trust
- Common in large open-source projects

**Benevolent Dictator for Life (BDFL)**
- One person has final say
- Delegates day-to-day decisions
- Examples: Python (Guido van Rossum, historically), Linux (Linus Torvalds)

**Example GOVERNANCE.md:**

```markdown
# Project Governance

## Roles

### Project Lead
- Jane Smith (@jsmith)
- Final decision authority
- Long-term vision

### Core Maintainers
- Jane Smith (@jsmith)
- John Doe (@jdoe)
- Alice Johnson (@ajohnson)

Core maintainers can:
- Merge pull requests
- Make releases
- Manage issues
- Modify core functionality

### Contributors
Anyone who submits accepted contributions.

## Decision Making

- Minor changes: Any core maintainer can approve
- Major changes: Require approval from 2+ core maintainers
- Breaking changes: Require approval from project lead

## Becoming a Core Maintainer

Criteria:
- Consistent high-quality contributions over 6+ months
- Domain expertise
- Community engagement
- Invited by existing core team

## Code of Conduct

All participants must follow our [Code of Conduct](CODE_OF_CONDUCT.md).
```

**Succession Planning:**

Plan for long-term sustainability:
- Document processes and decisions
- Train additional maintainers
- Share knowledge broadly
- Plan for transitions
- Consider archiving if maintenance ends

#### 4.5 Enabling Others to Use Your Code

Making code accessible goes beyond just uploading it to a platform.

**4.5.1 Installation and Setup**

**Make Installation Easy:**

**Bad:**
```
Download files, edit config.py with your paths, install dependencies 
manually, run setup script, pray it works.
```

**Good:**
```bash
pip install my-package
```

or

```bash
conda install -c conda-forge my-package
```

**Provide Multiple Installation Methods:**

```markdown
## Installation

### Option 1: Install from PyPI (recommended)
```bash
pip install climate-analyzer
```

### Option 2: Install from conda-forge
```bash
conda install -c conda-forge climate-analyzer
```

### Option 3: Install from source
```bash
git clone https://github.com/user/climate-analyzer.git
cd climate-analyzer
pip install -e .
```

### Verify Installation
```bash
python -c "import climate_analyzer; print(climate_analyzer.__version__)"
```
```

**4.5.2 Quick Start Guide**

Get users to a working example in 5 minutes:

```markdown
## Quick Start

After installation, try this minimal example:

```python
import climate_analyzer as ca

# Load example data (included with package)
data = ca.load_example_data()

# Calculate basic statistics
stats = ca.calculate_stats(data)
print(stats)

# Create visualization
ca.plot_temperature_trend(data)
```

This should produce a plot showing temperature trends over time.
```

**4.5.3 Examples and Tutorials**

**Provide Progressive Examples:**

1. **Basic Example:** Simplest possible use case (5-10 lines)
2. **Intermediate Example:** More realistic scenario (20-50 lines)
3. **Advanced Example:** Complex workflow (100+ lines)
4. **Tutorial:** Step-by-step walkthrough with explanation

**Example Structure:**

```
examples/
├── 01_basic_usage.py
├── 02_data_loading.py
├── 03_analysis_workflow.py
├── 04_custom_visualization.py
├── 05_advanced_integration.py
└── README.md  # Describes what each example demonstrates
```

**Jupyter Notebooks for Tutorials:**

```markdown
tutorials/
├── 01_getting_started.ipynb
├── 02_data_preparation.ipynb
├── 03_statistical_analysis.ipynb
└── 04_reproducible_workflow.ipynb
```

Notebooks should:
- Run from top to bottom without errors
- Include explanatory text
- Show expected output
- Use small example datasets

**4.5.4 Documentation Website**

For larger projects, create a documentation website:

**Structure:**
```
docs/
├── index.md                 # Home page
├── installation.md          # Installation guide
├── quickstart.md           # Quick start tutorial
├── user_guide/
│   ├── basic_concepts.md
│   ├── data_loading.md
│   ├── analysis.md
│   └── visualization.md
├── api/
│   ├── core.md
│   ├── io.md
│   └── plotting.md
├── tutorials/
│   ├── tutorial_01.md
│   └── tutorial_02.md
├── faq.md
└── contributing.md
```

**Hosting Options:**
- Read the Docs (readthedocs.org) - Free for open source
- GitHub Pages - Free, integrated with GitHub
- GitLab Pages - Similar to GitHub Pages

**4.5.5 Support Channels**

**Provide Clear Support Options:**

```markdown
## Getting Help

- **Documentation:** https://climate-analyzer.readthedocs.io
- **FAQ:** See our [Frequently Asked Questions](FAQ.md)
- **Issues:** Report bugs or request features at 
  https://github.com/user/climate-analyzer/issues
- **Discussions:** Ask questions at 
  https://github.com/user/climate-analyzer/discussions
- **Email:** For private inquiries: climate-help@institution.edu
- **Chat:** Join our Slack channel [link]
```

**Setting Expectations:**

```markdown
## Support Policy

- **Bug reports:** We aim to respond within 1 week
- **Feature requests:** Reviewed monthly, implemented based on priority
- **Questions:** Community-supported via discussions
- **Security issues:** Report privately to security@institution.edu

**Maintenance Status:** Actively maintained (as of 2024)
```

**4.5.6 Contributing Guidelines**

Help potential contributors get started:

**CONTRIBUTING.md:**

```markdown
# Contributing to Climate Analyzer

Thank you for your interest in contributing!

## Ways to Contribute

- Report bugs
- Suggest features
- Fix typos in documentation
- Submit bug fixes
- Add new features

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/yourusername/climate-analyzer.git`
3. Create a branch: `git checkout -b my-feature`
4. Make your changes
5. Run tests: `pytest`
6. Commit: `git commit -am "Add new feature"`
7. Push: `git push origin my-feature`
8. Create Pull Request on GitHub

## Code Style

- Follow PEP 8
- Run `black` before committing
- Add docstrings to all functions
- Include type hints where appropriate

## Testing

- Add tests for new features
- Ensure all tests pass
- Maintain >80% code coverage

## Questions?

Open an issue or discussion if you need help!
```

**4.5.7 Metadata and Discoverability**

**Make Your Code Findable:**

**GitHub Topics:**
Add relevant topics to your GitHub repository:
- climate-science
- data-analysis
- python
- temperature-analysis

**codemeta.json:**
Machine-readable metadata:

```json
{
  "@context": "https://doi.org/10.5063/schema/codemeta-2.0",
  "@type": "SoftwareSourceCode",
  "name": "Climate Analyzer",
  "description": "Python package for analyzing climate data",
  "author": [{
    "@type": "Person",
    "givenName": "Jane",
    "familyName": "Smith",
    "@id": "https://orcid.org/0000-0002-1234-5678"
  }],
  "programmingLanguage": "Python",
  "keywords": ["climate", "data analysis", "temperature"],
  "license": "https://spdx.org/licenses/MIT",
  "version": "1.0.0",
  "codeRepository": "https://github.com/user/climate-analyzer"
}
```

**CITATION.cff:**
Citation file format for easy citation:

```yaml
cff-version: 1.2.0
message: "If you use this software, please cite it as below."
authors:
  - family-names: Smith
    given-names: Jane
    orcid: https://orcid.org/0000-0002-1234-5678
title: "Climate Analyzer"
version: 1.0.0
doi: 10.5281/zenodo.1234567
date-released: 2024-01-15
url: https://github.com/user/climate-analyzer
```

**Setup.py classifiers** (for Python):

```python
classifiers=[
    "Development Status :: 4 - Beta",
    "Intended Audience :: Science/Research",
    "Topic :: Scientific/Engineering :: Atmospheric Science",
    "License :: OSI Approved :: MIT License",
    "Programming Language :: Python :: 3",
]
```

#### 4.6 Complete Sharing Workflow Example

A researcher completes analysis for a paper and wants to share the code:

**Step 1: Prepare Code (2-3 weeks before submission)**
- Clean up code, remove sensitive data
- Add docstrings and comments
- Create README with installation and usage
- Add LICENSE file (MIT chosen)
- Write tests, ensure they pass
- Create example dataset

**Step 2: Set Up GitHub Repository (1 week before submission)**
- Create public repository: `github.com/jsmith/ocean-analysis`
- Push code
- Add topics: oceanography, data-analysis, python
- Create releases page
- Set up GitHub Actions for CI

**Step 3: Create Release (at paper submission)**
- Tag version: `v1.0.0`
- Create GitHub release
- Write release notes

**Step 4: Archive on Zenodo (at paper submission)**
- Enable Zenodo integration on GitHub
- Zenodo automatically creates archive
- Receive DOI: 10.5281/zenodo.1234567

**Step 5: Update Paper (during revision)**
- Add "Code Availability" section to paper:
  ```
  Code Availability: Analysis code is available at 
  https://github.com/jsmith/ocean-analysis and archived at 
  https://doi.org/10.5281/zenodo.1234567
  ```
- Cite code in references

**Step 6: Publish to PyPI (optional, after paper acceptance)**
- Create distribution: `python -m build`
- Upload: `twine upload dist/*`
- Now installable: `pip install ocean-analysis`

**Step 7: Announce (after paper publication)**
- Tweet about release
- Post on relevant forums/mailing lists
- Add to domain-specific registries
- Update personal/lab website

**Step 8: Maintain (ongoing)**
- Respond to issues within 1-2 weeks
- Accept pull requests after review
- Release bug fixes as needed
- Update documentation

#### Summary

Sharing open code effectively requires:

1. **Decision making** - Determine if, when, and where to share based on legal, ethical, and practical considerations
2. **Platform selection** - Choose appropriate platforms for development, distribution, archival, and discovery
3. **Clear roles** - Define responsibilities and governance for project sustainability
4. **User enablement** - Provide documentation, examples, support, and contribution guidelines
5. **Discoverability** - Use metadata, registries, and announcements to make code findable
6. **Maintenance** - Plan for ongoing support and eventual archival

By following these practices, you ensure your code reaches and benefits the widest possible audience while maintaining quality and sustainability.

### Lesson 5: From Theory to Practice

#### Overview
This lesson ties the concepts of open access software development to the operation of a software management plan. The lesson also introduces you to the community aspect of open software. It begins with a discussion on writing software management plans, then continues with information on how to connect with open software communities. This information is contextualized with an introduction to the benefits of a software community and the roles involved in these groups. A list of communities is also presented, and you are asked to explore and engage with some of them. The lesson wraps up with helpful suggestions to contribute to open software and additional resources.

#### 5.1 Writing Software Management Plans

A Software Management Plan (SMP) is a living document that guides how software will be developed, maintained, and shared throughout a project's lifecycle.

**Why Write an SMP?**

- **Funder Requirements:** Many funding agencies now require SMPs (NIH, NSF, EU, etc.)
- **Planning Tool:** Helps think through technical decisions early
- **Communication:** Clarifies expectations for team members
- **Documentation:** Records decisions and rationale
- **Reproducibility:** Ensures others can understand and use your software

**When to Write an SMP:**

- **Ideal:** During project planning, before writing code
- **Acceptable:** Early in development, as soon as substantial coding begins
- **Still Useful:** Mid-project to document existing practices and plan improvements

**5.1.1 SMP Structure and Content**

**Core Components:**

**1. Project Overview**

```markdown
## Project Overview

**Project Title:** Marine Microplastic Analysis Toolkit

**Principal Investigator:** Dr. Jane Smith, Oceanography Department, 
University of Marine Sciences

**Project Duration:** January 2024 - December 2026

**Funding:** NSF Grant OCE-1234567

**Purpose:** Develop open-source Python toolkit for automated detection 
and analysis of microplastics in marine samples using microscopy images.

**Target Users:** 
- Marine scientists studying plastic pollution
- Environmental monitoring labs
- Graduate students learning microplastic analysis

**Expected Outputs:**
- Python package for microplastic detection
- Dataset of annotated microplastic images
- Analysis workflows for common use cases
- Publication in Marine Pollution Bulletin
```

**2. Software Description**

```markdown
## Software Description

**Software Name:** MarinePlasticsToolkit

**Programming Language:** Python 3.9+

**Key Dependencies:**
- NumPy (array operations)
- scikit-image (image processing)
- TensorFlow (machine learning)
- Pandas (data management)
- Matplotlib (visualization)

**Platform:** Cross-platform (Windows, macOS, Linux)

**Expected Scale:**
- ~5,000 lines of code
- 10-15 core functions
- Processing images from 1MB to 1GB
- Single-user desktop application

**Novelty:** First open-source tool combining deep learning with 
traditional image processing for microplastic detection.
```

**3. Development Plan**

```markdown
## Development Plan

**Development Timeline:**

- **Months 1-3:** Core image processing functions
- **Months 4-9:** Machine learning model development
- **Months 10-15:** Integration and testing
- **Months 16-24:** Documentation and publication
- **Months 24-36:** Community support and maintenance

**Development Environment:**
- Version control: Git + GitHub
- IDE: VS Code or PyCharm
- Testing: pytest
- CI/CD: GitHub Actions
- Documentation: Sphinx + Read the Docs

**Coding Standards:**
- Follow PEP 8 style guide
- Use type hints (Python 3.9+)
- Maximum function length: 50 lines
- Minimum code coverage: 80%

**Development Workflow:**
1. Create feature branch from `develop`
2. Implement feature with tests
3. Run tests locally
4. Push and create pull request
5. Peer review (minimum 1 reviewer)
6. Merge to `develop` after approval
7. Periodic releases to `main`
```

**4. Testing and Quality Assurance**

```markdown
## Testing and Quality Assurance

**Testing Strategy:**

- **Unit Tests:** All core functions (target: 85% coverage)
- **Integration Tests:** Complete workflows
- **Validation:** Compare results with manual annotations
- **Performance Tests:** Process time for standard images

**Test Data:**
- 100 manually annotated images for training
- 25 reserved images for testing (never used in training)
- Synthetic test images for edge cases

**Quality Checks:**
- Automated testing on every commit (GitHub Actions)
- Code review for all changes
- Monthly security scans (Dependabot)
- Annual dependency updates

**Validation Plan:**
- Compare automated detection with expert manual counts
- Target accuracy: >90% detection rate, <5% false positives
- Validation paper to be published
```

**5. Documentation Plan**

```markdown
## Documentation Plan

**User Documentation:**

- **README:** Installation, quick start, citation
- **Installation Guide:** Detailed setup for all platforms
- **User Guide:** Comprehensive usage instructions
- **Tutorials:** 3 progressive tutorials (basic, intermediate, advanced)
- **API Reference:** Auto-generated from docstrings
- **FAQ:** Common questions and troubleshooting

**Developer Documentation:**

- **Contributing Guide:** How to contribute
- **Architecture Overview:** System design
- **Development Setup:** Setting up dev environment
- **Release Process:** How to make releases

**Documentation Tools:**
- Sphinx for generation
- Read the Docs for hosting
- Jupyter notebooks for tutorials

**Maintenance:**
- Update documentation with each feature
- Review for accuracy quarterly
- Accept community documentation improvements
```

**6. License and Legal Considerations**

```markdown
## Licensing

**Software License:** MIT License

**Rationale:** 
- Maximizes reusability in research community
- Allows commercial use (environmental monitoring companies)
- Simple and well-understood
- Compatible with dependencies

**Data License:** Creative Commons Attribution 4.0 (CC BY 4.0)

**Rationale:**
- Standard for research data
- Requires attribution
- Allows reuse and modification

**Intellectual Property:**
- No patent applications planned
- University IP policy reviewed and approved
- All contributors will sign contributor agreement

**Third-Party Components:**
- All dependencies are open source (MIT, Apache 2.0, BSD)
- No proprietary dependencies
- License compatibility verified

**Export Control:** Not applicable (standard image processing)
```

**7. Sharing and Dissemination**

```markdown
## Sharing and Dissemination Plan

**Repository:**
- **Primary:** GitHub (github.com/marinelab/plastictoolkit)
- **Visibility:** Public from start
- **Organization:** Under lab GitHub organization

**Distribution:**
- **PyPI:** For easy installation via pip
- **conda-forge:** For conda users
- **Timeline:** Publish to registries upon v1.0 release (Month 16)

**Archival:**
- **Zenodo:** Automatic archiving of GitHub releases
- **DOI:** Obtained for each major version
- **Institutional Repository:** Copy archived at university repository

**Announcement:**
- Publication in Marine Pollution Bulletin (with code availability statement)
- Presentation at Ocean Sciences Meeting
- Blog post on lab website
- Social media (Twitter, Mastodon)
- Relevant mailing lists (marine-ecology-discuss)

**Discovery:**
- Register with bio.tools
- Add to awesome-ocean-science list
- Include in Marine Microplastics Network directory
- Submit to Journal of Open Source Software
```

**8. Maintenance and Sustainability**

```markdown
## Maintenance and Sustainability

**Maintenance Plan:**

**Years 1-3 (Active Development):**
- PI commitment: 2 hours/week
- Postdoc commitment: 10 hours/week
- Graduate student: 5 hours/week
- Response time for issues: <1 week
- Bug fixes released within 2 weeks
- Feature releases quarterly

**Years 4-5 (Maintenance Mode):**
- PI commitment: 1 hour/week
- Response time for issues: <2 weeks
- Bug fixes as needed
- Security updates prioritized
- No new features unless community-contributed

**Year 6+ (Archive or Handoff):**
- Option 1: Transition to community maintenance
  - Identify 2-3 community maintainers
  - Transfer knowledge over 6 months
- Option 2: Archive repository
  - Mark as archived with clear status
  - Preserve on Zenodo
  - Document successor projects if any

**Sustainability Strategies:**
- Build community early through good documentation
- Welcome and mentor contributors
- Present at conferences to build user base
- Apply for continued funding if successful
- Consider industry partnerships for long-term support

**Success Metrics:**
- GitHub stars: Target >100 in year 1
- Citations: Target >10 in year 2
- Contributors: Target >5 external contributors by year 3
- Issues/month: Target <5 open issues on average
```

**9. Community Engagement**

```markdown
## Community Engagement

**Target Community:**
- Marine scientists studying microplastics
- Environmental monitoring professionals
- Python scientific computing community
- Open science advocates

**Engagement Strategies:**

**Communication Channels:**
- GitHub Discussions for Q&A
- Issue tracker for bug reports
- Email list for announcements
- Monthly virtual office hours (video call)

**Community Guidelines:**
- Code of Conduct (Contributor Covenant)
- Contributing guidelines
- Pull request template
- Issue templates

**Community Building:**
- Acknowledge contributors in release notes
- Highlight community contributions on website
- Present community-contributed features at conferences
- Annual community survey for feedback

**Training:**
- Workshop at Ocean Sciences Meeting (Year 2)
- Online tutorial videos on YouTube
- Collaborate with Software Carpentry for lessons
```

**10. Data Management**

```markdown
## Data Management

**Training Data:**
- 100 annotated microplastic images
- Stored in GitHub repository (<100 MB total)
- License: CC BY 4.0
- Format: PNG images + JSON annotations

**Test Data:**
- 25 reserved test images
- Not included in repository (avoid overfitting)
- Available on request for validation
- Will be published with validation paper

**Example Data:**
- 10 small example images included in package
- For demonstration and testing
- Synthetic and real samples

**User Data:**
- Software processes user's own data locally
- No data collected or transmitted
- Privacy policy: We do not collect user data
```

**5.1.2 SMP Templates and Examples**

**Where to Find Templates:**

- **NSF:** Provides SMP guidance in grant proposals
- **NIH:** Software Management and Sharing Plans for data management plans
- **SSI (Software Sustainability Institute):** software.ac.uk provides templates
- **RDA (Research Data Alliance):** Example SMPs
- **Your Institution:** May have local templates

**Adapting Templates:**

Start with a template but customize for your project:
- Small project: Simplify, focus on essentials
- Large project: Add detail, include governance
- Collaborative project: Emphasize communication and roles
- Sensitive project: Expand legal and security sections

#### 5.2 Open Software Communities

Open-source software thrives through community participation. Understanding and engaging with communities is key to success.

**5.2.1 Benefits of Software Communities**

**For Users:**
- **Support:** Get help from experienced users and developers
- **Learning:** See how others solve similar problems
- **Influence:** Request features and report bugs
- **Networking:** Connect with others in your field
- **Trust:** Active community indicates maintained, reliable software

**For Contributors:**
- **Skill Development:** Improve coding through code review
- **Portfolio:** Build public track record of contributions
- **Recognition:** Gain visibility in research community
- **Collaboration:** Work with diverse, talented people
- **Impact:** Directly improve tools used by many

**For Maintainers:**
- **Sustainability:** Distributed maintenance burden
- **Quality:** More eyes find more bugs
- **Innovation:** Community contributes new ideas and features
- **Validation:** Community use validates research tool
- **Funding:** Strong community helps justify continued funding

**For Science:**
- **Acceleration:** Reduces duplicated effort
- **Quality:** Peer review and testing
- **Standardization:** Common tools enable comparison across studies
- **Accessibility:** Tools available to all researchers
- **Education:** Learning resource for students

**5.2.2 Types of Open Software Communities**

**Project-Specific Communities**

Communities centered on specific software packages:

**Examples:**
- **NumPy/SciPy:** Fundamental scientific computing in Python
- **R Bioconductor:** Bioinformatics tools
- **Astropy:** Astronomy Python tools
- **QGIS:** Geographic information system

**Characteristics:**
- Focused on one tool or ecosystem
- Users, contributors, and maintainers
- Communication via issues, forums, chat
- Regular releases and roadmaps

**Domain-Specific Communities**

Communities around scientific domains:

**Examples:**
- **PyOpenSci:** Python tools for open science
- **rOpenSci:** R tools for open science
- **INCF (Int'l Neuroinformatics Coordinating Facility):** Neuroscience tools
- **MolSSI (Molecular Sciences Software Institute):** Molecular sciences

**Characteristics:**
- Multiple related projects
- Domain expertise and standards
- Training and best practices
- Community review and endorsement

**Language/Technology Communities**

Communities around programming languages or technologies:

**Examples:**
- **Python Software Foundation:** Python language and ecosystem
- **R Consortium:** R language and ecosystem
- **Julia Community:** Julia language
- **Jupyter:** Interactive computing

**Characteristics:**
- Broad scope across domains
- Language development and governance
- Conferences and events
- Standards and best practices

**Open Science Communities**

Communities promoting open science practices:

**Examples:**
- **Software Carpentry/Data Carpentry:** Training in research computing
- **The Carpentries:** Broader training organization
- **Open Science Framework (OSF):** Open research platform
- **FORCE11:** Community for scholarly communication

**Characteristics:**
- Cross-disciplinary
- Focus on practices and culture
- Education and advocacy
- Policy development

**Institutional Communities**

Local communities at universities or research institutions:

**Examples:**
- University research computing groups
- Lab or department coding clubs
- Institutional GitHub organizations
- Local user groups (R Users Group, Python Users Group)

**Characteristics:**
- Local, face-to-face interaction
- Institution-specific resources
- Mixed skill levels
- Social and educational

**5.2.3 Finding and Joining Communities**

**Discovery:**

**Online:**
- GitHub: Explore projects, read discussions
- Mailing lists: Subscribe to relevant lists
- Forums: Discourse, Stack Exchange
- Chat: Slack, Discord, Gitter, Matrix
- Social media: Follow projects and developers
- Conferences: Check out workshop/BoF schedules

**Questions to Ask:**
1. Is this community active? (Recent posts/commits)
2. Is it welcoming? (Code of conduct, friendly responses)
3. Are my interests represented? (Relevant projects/topics)
4. Can I contribute at my level? ("Good first issue" labels)
5. How do people communicate? (Synchronous chat vs. asynchronous forum)

**Starting Engagement:**

**Lurk First:**
- Read documentation
- Browse issues and discussions
- Observe community norms
- Understand governance

**Start Small:**
- Introduce yourself
- Ask a thoughtful question
- Comment on an issue
- Fix a typo in documentation

**Be a Good Community Member:**
- Read and follow code of conduct
- Be respectful and constructive
- Search before asking (avoid duplicates)
- Show appreciation for help received
- Help others when you can

#### 5.3 Roles in Open Software Communities

**Community Role Spectrum:**

**1. User**
- Uses software for research
- Reads documentation
- May ask questions
- No contribution required

**2. Active User**
- Regular user
- Provides feedback
- Reports bugs
- Answers others' questions

**3. Contributor**
- Fixes bugs
- Adds features
- Improves documentation
- Reviews others' contributions
- Irregular participation

**4. Core Contributor**
- Regular contributions
- Trusted community member
- May have commit access
- Helps triage issues
- Mentors new contributors

**5. Maintainer**
- Ongoing responsibility
- Makes releases
- Sets direction
- Manages community
- May be paid or volunteer

**6. Governance**
- Steering committee member
- Sets long-term strategy
- Makes policy decisions
- Represents community
- Usually elected or appointed

**Progression Path:**

User → Active User → Contributor → Core Contributor → Maintainer → Governance

**Not linear:** Can skip steps or contribute at any level

**Time commitment examples:**
- User: 0-1 hour/month
- Active User: 1-5 hours/month
- Contributor: Variable, when interested
- Core Contributor: 5-20 hours/month
- Maintainer: 10-40 hours/month
- Governance: 5-10 hours/month

**Recognition:**

Communities recognize contributions in various ways:
- Listed in contributors file
- Acknowledged in release notes
- Co-authorship on software papers
- Speaking opportunities at conferences
- Formal titles (maintainer, core developer)
- Swag (t-shirts, stickers)

#### 5.4 List of Open Science Software Communities

**General Scientific Computing:**

1. **NumFOCUS** (numfocus.org)
   - Umbrella organization for scientific computing projects
   - Projects: NumPy, Pandas, Jupyter, Matplotlib, etc.
   - Conferences: PyData, JupyterCon

2. **The Carpentries** (carpentries.org)
   - Teaching foundational coding and data science skills
   - Software Carpentry, Data Carpentry, Library Carpentry
   - Worldwide instructor community

3. **PyOpenSci** (pyopensci.org)
   - Promotes open source Python tools for science
   - Peer review for Python packages
   - Training and resources

4. **rOpenSci** (ropensci.org)
   - Open science tools in R
   - Package peer review
   - Community calls and training

**Domain-Specific:**

5. **Astropy** (astropy.org)
   - Python astronomy tools
   - Large, active community
   - Annual meetings and workshops

6. **Bioconductor** (bioconductor.org)
   - R packages for genomics
   - Annual conferences
   - Active support forum

7. **Neuroinformatics (INCF)** (incf.org)
   - Neuroscience software and data
   - Training and standards

8. **MolSSI** (molssi.org)
   - Molecular sciences software
   - Education and best practices
   - Software fellowships

9. **Pangeo** (pangeo.io)
   - Big data geoscience
   - Cloud computing tools
   - Weekly community meetings

10. **ImageJ/Fiji** (imagej.net)
    - Microscopy image analysis
    - Active forum
    - Extensive plugins

**Language Communities:**

11. **Python Software Foundation** (python.org)
    - Python language development
    - PyCon conferences worldwide

12. **R Consortium** (r-consortium.org)
    - Supports R ecosystem
    - useR! conferences

13. **Julia Community** (julialang.org/community)
    - Julia language for scientific computing
    - JuliaCon conference
    - Active Discourse forum

**Open Science Organizations:**

14. **Center for Open Science** (cos.io)
    - Open Science Framework
    - Promotes open practices

15. **Software Sustainability Institute** (software.ac.uk)
    - UK-based, international reach
    - Training and advocacy
    - Fellowships

16. **FORCE11** (force11.org)
    - Scholarly communication innovation
    - Software citation principles
    - Annual conference

17. **Research Software Alliance (ReSA)** (researchsoft.org)
    - Connects research software communities
    - Policy and best practices

18. **US Research Software Engineer Association (US-RSE)** (us-rse.org)
    - Community for research software engineers
    - Annual conference
    - Career development

**Journals:**

19. **Journal of Open Source Software (JOSS)** (joss.theoj.org)
    - Publishes papers about research software
    - Open review process
    - Free to publish and read

20. **SoftwareX** (journals.elsevier.com/softwarex)
    - Software publication venue

**Platform Communities:**

21. **GitHub** (github.com)
    - Explore trending repositories
    - GitHub Discussions
    - GitHub Community Forum

22. **Stack Overflow** (stackoverflow.com)
    - Q&A for programming
    - Tags for specific languages/tools

23. **Research Software Engineers (RSE) Groups**
    - Many countries have RSE associations
    - UK-RSE, US-RSE, DE-RSE, Nordic-RSE, etc.

#### 5.5 Contributing to Open Software

Practical advice for making meaningful contributions.

**5.5.1 Types of Contributions**

**Beyond Code:**

Many valuable contributions don't involve coding:

1. **Documentation**
   - Fix typos and unclear explanations
   - Add missing examples
   - Translate documentation
   - Create tutorials

2. **Testing**
   - Test new releases
   - Report bugs with clear reproduction steps
   - Verify bug fixes
   - Test on different platforms

3. **Triage**
   - Reproduce reported bugs
   - Ask for clarification on vague issues
   - Tag issues appropriately
   - Close duplicate or resolved issues

4. **Community Support**
   - Answer questions in forums
   - Help newcomers
   - Moderate discussions

5. **Design**
   - Improve UI/UX
   - Create logos or graphics
   - Design website

6. **Outreach**
   - Write blog posts
   - Give presentations
   - Create video tutorials
   - Social media promotion

**Code Contributions:**

7. **Bug Fixes**
   - Fix reported bugs
   - Start with "good first issue" labels

8. **Features**
   - Implement requested features
   - Propose and implement new ideas
   - Check roadmap for planned work

9. **Performance**
   - Optimize slow code
   - Reduce memory usage
   - Add benchmarks

10. **Maintenance**
    - Update dependencies
    - Fix deprecation warnings
    - Improve CI/CD

**5.5.2 Contribution Workflow**

**Step-by-Step Process:**

**1. Choose a Project and Issue**
```markdown
- Look for "good first issue" or "help wanted" labels
- Read the issue carefully
- Comment: "I'd like to work on this"
- Wait for maintainer response/assignment
```

**2. Set Up Development Environment**
```bash
# Fork the repository on GitHub
# Clone your fork
git clone https://github.com/yourusername/project.git
cd project

# Add upstream remote
git remote add upstream https://github.com/original/project.git

# Install in development mode
pip install -e ".[dev]"

# Run tests to ensure everything works
pytest
```

**3. Create a Branch**
```bash
# Update your fork
git fetch upstream
git checkout main
git merge upstream/main

# Create feature branch
git checkout -b fix-issue-123
```

**4. Make Changes**
```markdown
- Implement the fix or feature
- Follow project's coding style
- Add/update tests
- Add/update documentation
- Commit with clear messages
```

**5. Test Your Changes**
```bash
# Run tests
pytest

# Check code style
black .
flake8 .

# Run any other required checks
```

**6. Push and Create Pull Request**
```bash
# Push to your fork
git push origin fix-issue-123

# Go to GitHub and create Pull Request
# Fill out PR template
# Link to related issue: "Fixes #123"
```

**7. Respond to Review**
```markdown
- Maintainers will review your PR
- Address feedback constructively
- Make requested changes
- Push updates (automatically updates PR)
- Engage in discussion if you disagree
```

**8. Celebrate!**
```markdown
- Once merged, your contribution is part of the project
- You'll be listed as a contributor
- You've made science better!
```

**5.5.3 Best Practices for Contributors**

**Before Contributing:**
- ✅ Read CONTRIBUTING.md
- ✅ Check if issue already exists
- ✅ Discuss major changes before implementing
- ✅ Ensure you can commit time to complete it

**While Contributing:**
- ✅ Keep pull requests focused (one issue per PR)
- ✅ Write clear commit messages
- ✅ Test thoroughly
- ✅ Document your changes
- ✅ Be patient with review process

**Communication:**
- ✅ Be respectful and professional
- ✅ Assume good intentions
- ✅ Ask for help if stuck
- ✅ Respond to feedback promptly
- ✅ Thank reviewers for their time

**Handling Rejection:**

Not all contributions will be accepted:
- Feature may not fit project scope
- Implementation may need different approach
- Timing may not be right

**If your PR is rejected:**
- Ask for clarification on why
- Learn from feedback
- Don't take it personally
- Consider alternative projects or approaches

#### 5.6 Building Your Own Community

If you're creating a new open-source project, building a community is essential for sustainability.

**Community Building Strategies:**

**1. Make It Easy to Get Started**
- Clear README
- Simple installation
- Good documentation
- Welcoming tone

**2. Lower Barriers to Contribution**
- CONTRIBUTING.md file
- "Good first issue" labels
- Response to questions
- PR templates

**3. Be Responsive**
- Acknowledge issues quickly (even if can't fix immediately)
- Provide constructive feedback
- Thank contributors
- Merge PRs promptly

**4. Foster Inclusive Environment**
- Code of Conduct
- Enforce CoC consistently
- Use inclusive language
- Welcome diverse perspectives

**5. Communicate Regularly**
- Roadmap and plans
- Release notes
- Blog posts or newsletters
- Community calls or meetings

**6. Recognize Contributors**
- Acknowledge in release notes
- Contributors file
- Highlight contributions
- Co-authorship on papers when appropriate

**7. Provide Multiple Engagement Paths**
- Code contributions
- Documentation
- Support/Q&A
- Testing
- Feedback

**Example Community Building Timeline:**

**Month 0-3: Foundation**
- Create excellent documentation
- Add Code of Conduct
- Set up contribution guidelines
- Create issue templates
- Establish communication channels

**Month 3-6: Initial Outreach**
- Present at conference/lab meeting
- Write blog post
- Post on social media
- Reach out to potential users
- Respond enthusiastically to first users

**Month 6-12: Growth**
- Welcome first contributors
- Create "good first issue" labels
- Run a workshop or tutorial
- Publish software paper
- Start community calls

**Month 12+: Sustainability**
- Identify potential maintainers
- Establish governance
- Regular releases
- Active community engagement
- Consider funding opportunities

#### 5.7 Additional Resources

**Books:**

1. **"Working in Public: The Making and Maintenance of Open Source Software"** by Nadia Eghbal
   - Modern perspective on open-source sustainability

2. **"The Turing Way"** (the-turing-way.netlify.app)
   - Handbook for reproducible, ethical, collaborative data science
   - Open source, collaborative book

3. **"Software Carpentry Lessons"** (software-carpentry.org/lessons)
   - Git, Python, R, shell - all open and free

**Online Courses:**

4. **"Reproducible Research" (Coursera)**
   - Johns Hopkins University

5. **"Version Control with Git" (Coursera)**
   - Atlassian

6. **"Open Science MOOC"** (opensciencemooc.eu)
   - Free course on open science principles

**Guidelines and Best Practices:**

7. **FAIR4RS Principles** (fair-software.eu)
   - FAIR principles for Research Software

8. **Software Citation Principles** (force11.org/software-citation-principles)
   - How to cite software properly

9. **chooseалicense.com**
   - Simple license selection guide

10. **opensource.guide**
    - GitHub's open-source guides
    - Starting and maintaining projects

**Organizations and Resources:**

11. **Software Sustainability Institute** (software.ac.uk)
    - Guides, training, fellowships

12. **Better Scientific Software** (bssw.io)
    - Curated resources for scientific software

13. **Research Software Engineers** (society-rse.org)
    - Professional development for RSEs

14. **CodeMeta** (codemeta.github.io)
    - Metadata standards for software

**Checklists:**

15. **Software Checklist** (software.ac.uk/resources/guides/software-checklist)
    - Comprehensive checklist for research software

16. **Contributor Covenant** (contributor-covenant.org)
    - Standard Code of Conduct

**Communities to Join:**

17. **Your Domain's Specific Community**
    - Search for "[your field] open source" or "[your field] software"
    - Many domains have active communities

18. **Local Research Software Engineering Groups**
    - Check if your institution has RSE group
    - Join local coding clubs or user groups

**Conferences:**

19. **Research Software Engineers Conference**
    - Annual conferences in multiple countries

20. **SciPy, PyData, useR!, JuliaCon**
    - Language-specific scientific computing conferences

21. **Domain-Specific Conferences**
    - Most scientific conferences now have software sessions/workshops

#### 5.8 Practical Exercises

To reinforce learning, try these hands-on activities:

**Exercise 1: Explore a Community**
- Choose an open-source project relevant to your field
- Read the documentation and README
- Browse open issues
- Read contribution guidelines
- Observe a few discussion threads
- Reflect: Is this community welcoming? Active? Well-organized?

**Exercise 2: Make a Small Contribution**
- Find a project with "good first issue" label
- Choose a documentation fix or simple bug
- Fork, fix, and submit a pull request
- Experience the contribution workflow

**Exercise 3: Draft an SMP**
- For your current or planned project, write an SMP
- Include at minimum: description, license, sharing plan, maintenance plan
- Share with advisor or colleague for feedback

**Exercise 4: Review Code**
- Find an open pull request in a project you use
- Read the code and proposed changes
- Provide constructive feedback (even if just "looks good")
- Practice collaborative review

**Exercise 5: Share Your Code**
- Take a script or analysis you've written
- Clean it up, add a README and LICENSE
- Upload to GitHub
- Share with one colleague
- Get feedback on usability

#### Summary

This lesson connected theory to practice by:

1. **Software Management Plans** - Providing structure and templates for planning open software projects from inception through sustainability

2. **Community Benefits** - Explaining the value of communities for users, contributors, maintainers, and science as a whole

3. **Community Types** - Describing project-specific, domain, language, open science, and institutional communities

4. **Roles and Participation** - Outlining the spectrum from user to maintainer and how to engage at any level

5. **Community Directory** - Listing specific communities to explore and join across domains and technologies

6. **Contributing Practices** - Providing concrete steps and best practices for contributing to open software

7. **Building Communities** - Offering strategies for maintainers to foster welcoming, sustainable communities

8. **Resources** - Curating books, courses, guidelines, and tools for continued learning

By engaging with open-source communities and following best practices for software management, researchers can create, share, and sustain high-quality research software that benefits the entire scientific community. The open-source ecosystem thrives on participation at all levels - from using and citing software to contributing fixes and building new tools. Every researcher can find a role that fits their interests, skills, and time commitment, ultimately advancing open science for all.

## Additional Resources

In addition to the TOPS module training, the community resources below are excellent information sources about open science.
- Ince et al. (2012). The case for open computer programs. [The case for open computer programs \| Nature](https://www.nature.com/articles/nature10836)
- Iskoujina and Roberts (2015). Knowledge sharing in open source software communities: motivations and management. [PDF](https://pdfs.semanticscholar.org/f2a2/c5129cf5656af7acc7ffaf84c9c9bafe72c5.pdf)
- Shamir et al. (2013). Practices in source code sharing in astrophysics. [arXiv:1304.6780v1](https://arxiv.org/abs/1304.6780)