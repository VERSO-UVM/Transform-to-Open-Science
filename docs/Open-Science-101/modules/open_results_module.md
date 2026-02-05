# MModule 4 - Open Results

Welcome to Open Results! This module focuses on giving you the tools you need to kick-start a scientific collaboration by creating contributor guidelines that ensure ethical contributorship. It starts out with a use case of open science in action, then a review of how to discover and assess open results. Next, the focus is on how to publish results which includes a task checklist. The module wraps up with specific guidance for writing the sharing results section of the Open Science and Data Management Plans (OSDMP). We will also reflect on how our society and technology are constantly evolving in the way we do science.

## Learning Objectives

After completing this module, you should be able to:
- Describe what constitutes an open result.
- Explain what the reproducibility crisis is and how open science can help combat it.
- Use a process to discover, assess and cite open results for reuse.
- List the responsibilities of the following participants that are creating open results: open results user, project leader, collaborator, contributor and author.
- List the tasks for creating reproducible results and the items to include in a manuscript to ensure reproducible results.
- Define a strategy for sharing your results including selecting publishers, interpreting journal policies and licenses, and determining when to share your data or software with your manuscript.

### Lesson 1: Introduction to Open Results

#### Overview
This lesson aims to broaden your perspective regarding what shareable research outputs are produced throughout the research lifecycle. We will first consider what constitutes an open result. To do so, we will read an example of a forward-thinking research project that utilizes open result best practices. The perspectives gained from this example will ultimately get us thinking about how we can work towards creating reproducible research.

#### 1.1 What Are Open Results?

**Definition:**
Open results are research outputs—including manuscripts, figures, datasets, code, protocols, and findings—that are made freely available and accessible to anyone for reuse, verification, and building upon, with appropriate attribution.

**Characteristics of Open Results:**

1. **Accessible:** Freely available without paywalls or registration
2. **Transparent:** Methods and data fully documented
3. **Reproducible:** Others can verify findings with original data and code
4. **Reusable:** Licensed for reuse with clear permissions
5. **Citable:** Have persistent identifiers (DOIs) enabling proper attribution
6. **Traceable:** Include provenance and version history
7. **Interoperable:** Use standard formats enabling integration with other work

**Types of Research Outputs:**

Research outputs take many forms throughout the research lifecycle. The most fundamental outputs are primary research results, which include peer-reviewed journal articles published as open access, preprints that share findings rapidly, conference papers that disseminate work to specialized audiences, technical reports that document detailed findings, raw and processed datasets that form the foundation of analysis, and code or software tools that enable reproducibility and reuse.

Beyond these primary outputs, supporting materials are equally important for enabling reproducibility and extending the work. These include supplementary figures and tables that provide additional detail, comprehensive protocols and detailed methods that allow others to replicate procedures, raw data that preserves the original observations, analysis code that documents computational workflows, and reproducible workflows that integrate all components into executable documents.

Research findings must also be communicated to broader audiences through diverse formats. Communication outputs encompass blog posts and commentary that interpret results for general audiences, tutorials and guides that teach methods to practitioners, educational materials that integrate findings into curricula, data visualizations that reveal patterns and relationships, and interactive tools that allow exploration and discovery.

Finally, professional outputs represent the culmination of research work and engagement with the scientific community. These include presentations and slides from conferences and seminars, posters that summarize key findings for visual communication, open educational resources that share knowledge freely, and review articles that synthesize and advance understanding of research areas. Together, these diverse output types create a comprehensive research ecosystem that maximizes impact and enables collaboration.

#### 1.2 The Reproducibility Crisis and Open Science

**What Is the Reproducibility Crisis?**

A significant portion of published research findings cannot be reliably reproduced or replicated by other scientists, raising fundamental concerns about the integrity and reliability of the scientific record. Multiple surveys have documented this troubling pattern: research by Baker (2016)[^1] found that 70% of researchers have failed to reproduce the results of other scientists, while 50% have even failed to reproduce their own earlier results. This reproducibility crisis spans virtually all scientific disciplines, though it has proven particularly severe in psychology, biology, and medicine—fields where the consequences of irreproducible findings can directly impact human health and wellbeing. High-profile failures in psychology, such as the inability to replicate well-known effects, have been especially jarring and have catalyzed broader conversations about research practices. The problem is not merely a statistical artifact or an occasional oversight; rather, it reflects systemic issues in how research is conducted, reported, and evaluated that create perverse incentives for producing results that are more likely to be novel and statistically significant than accurately representative of underlying phenomena.

**Causes of Irreproducibility:**

1. **Data Unavailability**
   - Researchers don't share raw data
   - Others can't verify calculations
   - Makes independent analyses impossible

2. **Method Opacity**
   - Insufficient methodological detail in papers
   - "Methods available upon request" (often denied)
   - Missing parameters or procedures

3. **Code Unavailability**
   - Analysis code not shared
   - Computation cannot be verified
   - Errors in analysis go undetected

4. **Publication Bias**
   - Only positive/significant results published
   - Negative or null results disappear
   - Field develops skewed understanding

5. **Statistical Issues**
   - P-hacking/multiple comparisons
   - HARKing (Hypothesizing After Results are Known)
   - Underpowered studies

6. **Inadequate Peer Review**
   - Reviewers lack access to data/code
   - Limited statistical expertise
   - No time to fully verify claims

7. **Incentive Misalignment**
   - Publish-or-perish pressure
   - Novel/positive results prioritized
   - Limited reward for replication

**Example: The Replication Crisis in Psychology**

Many famous psychology findings failed replication:
- Power posing: Original finding didn't replicate with larger sample
- Ego depletion: Effect largely disappears with proper controls
- Implicit associations: Effects smaller than originally reported

**Impact:** Wasted resources, misleading theories, loss of public trust in science

**How Open Science Addresses Reproducibility:**

Open science practices directly counter the systemic problems that create irreproducible research. By implementing complementary strategies that increase transparency, accountability, and verification at every stage of research, open science makes it substantially harder for false findings to survive unchallenged and easier for errors and inflated effects to be discovered and corrected. The following practices work together to create a research ecosystem where the incentives, infrastructure, and norms all support reproducibility rather than undermining it:

**1. Open Data**
- All data available for independent analysis
- Others can check calculations
- Errors in original analysis discovered
- Enables meta-analyses

**2. Open Code**
- Analysis code transparent and auditable
- Computation fully verifiable
- Bugs identified and fixed
- Methods can be adapted for new data

**3. Open Methods**
- Complete protocol documentation
- Allows exact replication
- Enables adaptation for new contexts
- Builds on previous work

**4. Preregistration**
- Declare hypotheses and methods before data analysis
- Separates confirmatory from exploratory research
- Prevents p-hacking and HARKing
- Builds confidence in positive findings

**5. Open Access**
- Results freely available to all researchers
- Increases citations and impact
- Speeds scientific progress
- Reduces redundant research

**6. Open Review**
- Peer review transparent
- Increases accountability
- Can improve review quality
- Enables post-publication discussion
- Enables post-publication discussion

#### 1.3 Case Study: Open Results in Action

**Example: Forest Biodiversity and Climate Change Study**

**Background:**
A research group studies how forest species composition is changing in response to climate change.

**Open Results Practices:**

**Step 1: Planning (Preregistration)**
- Register hypotheses and analysis plan before data collection
- Specify which analyses are confirmatory vs. exploratory
- Anticipate alternative explanations
- Plan for multiple testing corrections

**Step 2: Data Collection**
- Document protocols in detail
- Share field methods openly
- Train students using open protocols
- Record all metadata comprehensively

**Step 3: Analysis**
- Write analysis code in reproducible format (R Markdown, Jupyter)
- Include all data cleaning steps
- Document all decisions and assumptions
- Save intermediate results
- Use version control (Git)

**Step 4: Sharing During Research**
- Post preprints early (bioRxiv)
- Share preliminary code on GitHub
- Openly discuss methods and findings
- Invite feedback from community

**Step 5: Publication**
- Submit to open access journal or use hybrid option
- Ensure peer review focuses on verification
- Include supplementary materials with full methods
- Publish accepted version in institutional repository

**Step 6: Data and Code Release**
- Share raw data with full documentation
- Release analysis code on GitHub with DOI
- Archive data in disciplinary repository
- Publish data descriptor paper
- Obtain DOIs for all outputs

**Step 7: Transparency and Engagement**
- Share supplementary analyses openly
- Respond to post-publication critique
- Acknowledge limitations clearly
- Share derived datasets
- Update analysis as new methods emerge

**Results of Open Approach:**
- 5x more citations than average
- 20+ follow-up studies building on their methods
- Community identified data quality improvements
- Methods adopted by other research groups
- Media attention and public engagement
- Career advancement for team members
- Funding for follow-up research

#### 1.4 Open Results Across the Research Lifecycle

**Where Open Results Fit:**

```
Research Lifecycle with Open Results Integration

┌─────────────────────────────────────────────────────────────────┐
│ 1. RESEARCH DESIGN & PLANNING                                   │
│    - Register protocol/hypotheses (OSF, AsPredicted)            │
│    - Share research plan openly                                 │
│    - Discuss methods with community                             │
└─────────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────────┐
│ 2. RESEARCH EXECUTION                                           │
│    - Document methods thoroughly                                │
│    - Share protocols openly                                     │
│    - Version control analysis code                              │
│    - Regular progress updates                                   │
└─────────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────────┐
│ 3. ANALYSIS & VERIFICATION                                      │
│    - Reproducible code with documentation                       │
│    - Data availability statements                               │
│    - Sensitivity analyses                                       │
│    - Limitations discussion                                     │
└─────────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────────┐
│ 4. PREPRINT SHARING (Optional)                                  │
│    - Rapid dissemination                                        │
│    - Early feedback                                             │
│    - Community engagement                                       │
│    - Establishes precedence                                     │
└─────────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────────┐
│ 5. PEER REVIEW & PUBLICATION                                    │
│    - Open access journals                                       │
│    - Transparent review (optional)                              │
│    - Revise with open methods                                   │
│    - Include methods in supplementary                           │
└─────────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────────┐
│ 6. DATA & CODE RELEASE                                          │
│    - Publish data with paper                                    │
│    - Release analysis code                                      │
│    - Obtain DOIs                                                │
│    - Archive in repositories                                    │
└─────────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────────┐
│ 7. POST-PUBLICATION ENGAGEMENT                                  │
│    - Respond to critiques                                       │
│    - Share additional analyses                                  │
│    - Support replication efforts                                │
│    - Contribute to meta-analyses                                │
└─────────────────────────────────────────────────────────────────┘
```

#### 1.5 Open Results Principles

**Core Principles:**

1. **Transparency**
   - Methods fully documented
   - Analysis decisions justified
   - Limitations acknowledged
   - Assumptions stated

2. **Reproducibility**
   - Others can replicate your analysis
   - Code and data available
   - Results are verifiable
   - Methods are detailed

3. **Accessibility**
   - Results freely available
   - No paywalls or registration required
   - Multiple formats for different audiences
   - Inclusive language

4. **Reusability**
   - Clear licensing
   - Metadata enabling discovery
   - Interoperable formats
   - Building blocks for others

5. **Accountability**
   - Clear authorship and contributions
   - Conflicts of interest disclosed
   - Funding sources stated
   - Errors corrected promptly

#### Summary

Open results are essential for addressing the reproducibility crisis by making research transparent, verifiable, and reusable. By adopting open results practices—sharing data, code, methods, and publications openly—researchers can:
- Build trust in science
- Accelerate discovery through reuse
- Improve research quality
- Advance their careers
- Serve the public good

The shift toward open results requires changes in incentives, culture, and practices, but the benefits for science and society are substantial.

### Lesson 2: Using Open Results

#### Overview
By the end of this lesson, you will be familiar with resources for open results utilization, how and when to cite the sources of the open results that you use, how to provide feedback to open results providers, and how to determine when it is appropriate to invite authors of the open results materials to be formal collaborators versus simply citing those resources in your work.

#### 2.1 Discovering Open Results

**Where to Find Open Results:**

**Preprint Servers:**

**ArXiv** (arxiv.org)
- Physics, mathematics, computer science, and more
- Established 1991, highly trusted
- Permanent archive
- ~14,000 new papers daily
- No peer review, but highly cited

**bioRxiv** (biorxiv.org)
- Biology and life sciences preprints
- ~6,000 new papers daily
- Often precedes journal publication by months
- Growing influence in biology

**medRxiv** (medrxiv.org)
- Medical and clinical research
- Growing importance for health research
- Enables rapid dissemination of timely findings

**PsyArXiv** (psyarxiv.org)
- Psychology and cognitive sciences
- ~500 papers posted monthly

**OSF Preprints** (osf.io/preprints)
- Multidisciplinary
- Integrates with Open Science Framework
- ~1,000 papers monthly across disciplines

**Open Access Journals:**

**Directory of Open Access Journals (DOAJ)** (doaj.org)
- 20,000+ open access journals
- Browse by subject
- Check for quality (has DOAJ seal)

**PLOS** (plos.org)
- Pioneering open access publisher
- PLOS ONE, PLOS Biology, PLOS Medicine, etc.
- High quality, peer-reviewed

**eLife** (elifesciences.org)
- Open access life sciences journal
- Innovation in peer review and publishing
- Early-career researcher friendly

**Frontiers** (frontiersin.org)
- Open access across disciplines
- ~2,000 journals
- Rapid publishing

**Other Open Access Publishers:**
- Nature Communications, Scientific Reports, npj series
- MDPI journals
- Hindawi journals

**Repositories for Full Papers:**

**PubMed Central** (pmc.ncbi.nlm.nih.gov)
- Full text of biomedical/life science articles
- Free access
- NIH-funded research included

**Google Scholar** (scholar.google.com)
- Search academic papers
- Often links to free PDFs
- Google Scholar Profiles show author's work

**ResearchGate** (researchgate.net)
- Researchers share papers
- Can request from authors
- Often has PDFs available

**Academia.edu** (academia.edu)
- Similar to ResearchGate
- Author profiles
- Ease of sharing

**Institutional Repositories**
- Most universities maintain repositories
- Often freely accessible
- Search by institution

**Author Websites/Lab Pages**
- Researchers often post preprints
- May have dataset repositories
- Email authors for copies

**Search Strategies:**

**1. Keyword Search**

Better: "forest biodiversity climate change species richness"
- Find prolific authors in your area
- Follow their work

:::{admonition} Activities for Lesson 1
:class: activity

Complete at least two of the following activities to solidify your understanding of open results concepts:

**Activity 1.1: Evaluate an Open Result**
Find a published open result in your field (paper with openly available data, code, or both). Using the assessment checklist from Lesson 2 (section 2.2), evaluate:
- How transparent are the methods?
- Are data and code truly accessible?
- Would you be able to replicate this work?
- What additional information would improve reproducibility?

Write 200-300 words reflecting on your assessment.

**Activity 1.2: Register a Study on OSF**
Visit the Open Science Framework (osf.io) and create an account if you don't have one. Register a study you're planning or currently conducting:
- Create a project
- Add project information and hypotheses
- Specify your analysis plan
- Set permissions for who can see different components
- Take a screenshot of your registered project and reflect on how this commitment to transparency might change your research practices

**Activity 1.3: Create an Open Results Checklist for Your Lab**
Develop a practical checklist that your research group could use to ensure open results. Include:
- What constitutes open results for your field
- Key decisions to make before starting data collection
- Specific tools and platforms you'll use
- Timeline for sharing results
- Roles and responsibilities

Share this draft with a colleague and get feedback.

**Activity 1.4: Explore the Reproducibility Crisis in Your Field**
Research one documented reproducibility failure in your discipline (e.g., a failed replication study, retracted paper, or contested findings). Write a 300-400 word analysis that includes:
- What was the original finding?
- Why did it fail to replicate?
- How could open results practices have prevented or mitigated this problem?
- What specific open science practices would have helped?
:::

### Lesson 2: Using Open Results
- Subscribe to their updates

**3. Citation Tracking**
- Read papers in your field
- Look at their references
- Check who cites those papers

**4. Journal Browsing**
- Subscribe to tables of contents
- Follow specific journals
- Set up alerts

**5. Archive/Repository Browsing**
- ArXiv has topic categories
- DOAJ lets you browse by subject
- Watch for new papers in category

#### 2.2 Assessing Open Results Quality

**What to Evaluate:**

**1. Source Credibility**

**Peer-Reviewed Journal Articles**
- ✅ Advantage: Vetted by experts
- ✅ Advantage: Often high quality
- ⚠️ Note: Not all peer review is rigorous
- ⚠️ Note: Publication bias exists

**Preprints**
- ✅ Advantage: Rapid dissemination
- ✅ Advantage: Early access to findings
- ⚠️ Caution: Not peer-reviewed
- ⚠️ Caution: May contain errors
- ⚠️ Caution: Quality varies widely

**Gray Literature (theses, reports)**
- ✅ Advantage: Often detailed
- ✅ Advantage: May have data others lack
- ⚠️ Caution: Limited audience review
- ⚠️ Caution: May be incomplete

**2. Methodology Assessment**

Ask yourself:
- Are methods clearly described?
- Can I understand what they did?
- Are sample sizes adequate?
- Are there obvious limitations?
- Was methodology appropriate for question?
- Did they use accepted procedures?

**3. Results Interpretation**

Consider:
- Are conclusions supported by data?
- Do they acknowledge limitations?
- Are alternative explanations considered?
- How novel/surprising are findings?
- Is effect size reported (not just p-values)?
- Are confidence intervals provided?

**4. Transparency Check**

Look for:
- ✅ Open data availability
- ✅ Code availability
- ✅ Protocol registration
- ✅ Conflict of interest disclosure
- ✅ Funding transparency
- ✅ Clear authorship statements

**5. Reproducibility Indicators**

- ✅ Detailed methods section
- ✅ Data and code available
- ✅ Materials/reagents specified
- ✅ Statistical code shown
- ✅ Supplementary materials comprehensive
- ✅ DOIs for data/code

**Assessment Checklist:**

| Question | Yes | No | Notes |
|----------|-----|-----|--------|
| Can I understand the research question? | | | |
| Are methods clearly described? | | | |
| Are methods appropriate for question? | | | |
| Is sample size/power adequate? | | | |
| Are results presented clearly? | | | |
| Are conclusions supported? | | | |
| Are limitations acknowledged? | | | |
| Is data/code available? | | | |
| Are there conflicts of interest? | | | |
| Has this been peer-reviewed? | | | |
| How many citations does it have? | | | |
| Do other studies support findings? | | | |

#### 2.3 Reusing Open Results

**Building on Others' Work:**

**1. Using Datasets**

```python
# Example: Using published forest biodiversity data
import pandas as pd

# Load publicly available dataset
species_data = pd.read_csv(
    'https://doi.org/10.5061/dryad.xxxxx/species_observations.csv'
)

# Analyze with their data
richness = species_data.groupby('site_id')['species'].nunique()

# Compare with your new data
my_data = pd.read_csv('my_observations.csv')
comparison = richness.merge(my_data, on='site_id')
```

**2. Using Analysis Code**

```r
# Load and adapt published analysis
source('https://github.com/example/forest-analysis/blob/main/diversity_analysis.R')

# Run on new dataset
results <- calculate_diversity(my_new_data)
```

**3. Using Methods and Protocols**

- Adapt published protocols for your samples
- Reference exact protocol version
- Note any modifications
- Build on established procedures

**4. Using Frameworks and Tools**

- Use software tools from open results
- Build new tools based on published ones
- Extend published analyses
- Apply methods in new contexts

#### 2.4 Citing Open Results

**Why Citation Matters:**

- Gives credit to original authors
- Enables verification and traceability
- Supports impact metrics
- Builds research transparency
- Enables future researchers to find sources

**Citation Formats:**

**For Published Papers:**

```
Harvard Style:
Smith, J., Johnson, A., & Brown, B. (2024). Forest biodiversity 
and climate change. Nature Climate Change, 14(3), 234-241. 
https://doi.org/10.1038/s41558-024-XXXXX

APA Style:
Smith, J., Johnson, A., & Brown, B. (2024). Forest biodiversity 
and climate change. Nature Climate Change, 14(3), 234-241. 
https://doi.org/10.1038/s41558-024-XXXXX

Chicago Style:
Smith, Jane, Alice Johnson, and Bob Brown. "Forest Biodiversity 
and Climate Change." Nature Climate Change 14, no. 3 (2024): 234-241. 
https://doi.org/10.1038/s41558-024-XXXXX
```

**For Preprints:**

```
Smith, J., Johnson, A., & Brown, B. (2024). Forest biodiversity 
and climate change. bioRxiv. 
https://doi.org/10.1101/2024.01.15.XXXXX

Note: Include "preprint" in citation to indicate pre-peer-review status
```

**For Data and Code:**

```
Smith, J., Johnson, A., & Brown, B. (2024). Forest biodiversity 
data 1980-2023 [Data set]. Zenodo. 
https://doi.org/10.5281/zenodo.XXXXX

Smith, J., Johnson, A., & Brown, B. (2024). Forest biodiversity 
analysis code (v1.2) [Computer software]. GitHub. 
https://doi.org/10.5281/zenodo.XXXXX
```

**For Protocols:**

```
Smith, J. (2024). Forest soil sampling protocol (v3.1). Protocols.io. 
https://doi.org/10.17504/protocols.io.XXXXX
```

#### 2.5 Providing Feedback and Contributing

**Engaging with Open Results:**

**1. Post-Publication Discussion**

**Via Comments/Responses:**
- Many journals allow published comments
- Open peer review platforms encourage discussion
- Blog posts discussing findings
- Social media engagement

**Example Comment:**
```
Smith et al.'s findings are valuable, but I have a concern about 
the statistical analysis. The t-test assumes normality, but their 
data appear skewed. Have they checked this assumption? Their raw 
data are publicly available, so I verified this by analyzing the 
residuals myself. A Mann-Whitney U test would be more appropriate 
and changes the p-value from 0.03 to 0.08.
```

**2. Reporting Errors**

**Contact authors with:**
- Specific error location (table, figure, page)
- Why you think it's an error
- Evidence (calculation, code, reference)
- Suggested correction
- Constructive tone

**3. Building on the Work**

**Ways to acknowledge others:**
- Cite their papers
- Reference their data
- Acknowledge code use
- Thank them in acknowledgments
- Collaborate formally (if appropriate)

**4. Replicating Studies**

**Replication steps:**
1. Obtain original data and code
2. Follow analysis exactly
3. Report success or discrepancies
4. Share your replication openly
5. Contact original authors
6. Work together to resolve differences

#### 2.6 Collaboration vs. Citation

**When to Cite vs. Collaborate:**

**Cite When:**
- Using published methods
- Building on published datasets
- Referencing published analyses
- Using open source software
- Testing published hypotheses
- No direct interaction needed

**Example:**
```
"We used the forest biodiversity dataset from Smith et al. (2024) 
to conduct new analyses examining temporal trends..."
```

**Collaborate When:**
- Extending their work significantly
- Working closely together
- Building new datasets/tools together
- Co-authoring new papers
- Combining expertise and resources
- Sustained interaction

**Steps to Propose Collaboration:**

1. **Research their work thoroughly**
   - Understand their interests
   - Know their recent publications
   - Identify complementary strengths

2. **Craft personalized email**
   - Be specific about mutual interests
   - Explain how collaboration benefits both
   - Propose concrete next steps
   - Keep it brief initially

**Example Email:**
```
Dear Dr. Smith,

I greatly appreciate your recent paper on forest biodiversity and 
climate change. I'm working on similar research in tropical forests 
and would like to apply your analysis methods to my dataset.

I'm wondering if you'd be interested in collaborating on a paper 
comparing temperate and tropical forest responses to climate change? 
I have 15 years of data from 20 tropical sites that would provide 
an interesting complement to your global analysis.

Would you be open to discussing this? I'd be happy to visit your lab 
to work through the details.

Best regards,
Alice Johnson
```

3. **Make it easy for them**
   - Provide data/code
   - Handle initial analyses
   - Write first draft
   - Respect their time

4. **Formalize collaboration**
   - Write collaboration agreement
   - Clarify authorship criteria
   - Establish timelines
   - Define roles

#### Summary

Effectively using open results requires:
1. **Discovery:** Knowing where to find and search for open results
2. **Assessment:** Evaluating quality and suitability for your work
3. **Integration:** Properly building on and citing others' work
4. **Engagement:** Providing feedback and contributing to improvement
5. **Collaboration:** Deciding when collaboration is appropriate

By mastering these skills, you become an active participant in the open science ecosystem, building on others' work while advancing your own research.

### Lesson 3: Making Open Results

:::{admonition} Activities for Lesson 2
:class: activity

Complete at least two of the following activities to practice using open results:

**Activity 2.1: Search and Evaluate Open Results**
Conduct a comprehensive search for open results relevant to your research question:
- Use at least 3 different discovery resources (preprint servers, open journals, repositories)
- Identify 5-10 potentially useful open results
- Assess each using the quality checklist from section 2.2
- Create a summary table showing source, accessibility, quality assessment, and reusability potential
- Write a reflection on which results are most useful and why

**Activity 2.2: Practice Citation of Open Results**
Take three open results from Activity 2.1 and practice citing them in different formats:
- Write a full citation for each in APA, Chicago, and Harvard styles
- Note any differences between citing published papers, preprints, and datasets
- Create a brief annotated bibliography (50 words per entry) explaining how you would use each result
- Reflect on how proper citation strengthens your own credibility and supports open science

**Activity 2.3: Plan a Collaboration**
Identify a researcher whose open results are directly relevant to your work. Draft a professional email proposing collaboration that includes:
- Specific reference to their published work
- Concrete ideas for how your work could complement theirs
- Specific, time-bound next steps
- Clear indication of the value to both parties

Don't send it yet, but have a colleague review it for tone and clarity. Reflect on what made it effective.

**Activity 2.4: Provide Feedback to an Open Results Provider**
Identify a published dataset or software tool that you use or are interested in. Provide constructive feedback by:
- Creating an issue on their GitHub repository or contacting the authors
- Pointing out something helpful you found about the resource
- Noting any unclear documentation or areas for improvement
- Suggesting enhancements in a constructive, appreciative tone
- Reflect on how this engagement contributes to improving open science

**Activity 2.5: Build on an Open Result**
Select one open result (preferably with publicly available data/code) and create something new from it:
- Conduct a secondary analysis using their data
- Adapt their code for a new dataset
- Create a visualization of their findings
- Test their analysis with different parameters
- Write up your work with proper attribution and share it openly (on GitHub, OSF, or preprint server)
:::

### Lesson 3: Making Open Results

#### Overview
In this lesson, we focus on making open results. We will start by discussing what it means to make reproducible results. Having earlier in the course discussed the computational reproducibility practices in open software, in this lesson, we specifically emphasize the importance of collaborations in making those results open and reproducible. This begins with acknowledging that scientific results are not made by single individuals. We will then teach how to ensure equitable, fair, and successful collaborations when making your open results that acknowledge all contributions. Once you've planned the rules of engagement, we will provide you with ways to ensure that your reporting and publication abide by open results principles and combat the reproducibility crisis.

#### 3.1 Computational Reproducibility

**What Makes Results Reproducible?**

Reproducible results allow others to:
1. Understand exactly what you did
2. Obtain the same results from the same data
3. Verify your analyses
4. Adapt methods for new data
5. Build on your work

**The Reproducibility Spectrum:**

```
Not Reproducible ─────────────────────────────────────────► Fully Reproducible
|
No code/methods             Partial documentation        Complete code/data/methods
No data available           Some code available          All materials published
Unpublished results         Selective sharing            Full transparency
```

**Key Elements of Reproducible Research:**

**1. Complete Methodology Documentation**

✅ **Include:**
- Specific software versions
- Hardware specifications
- Random seeds for simulations
- Hyperparameters for algorithms
- All preprocessing steps
- Decision rules for outliers
- Rounding and precision details

**Example:**
```markdown
## Methods

### Software Environment
- R version 4.2.1
- Packages: dplyr 1.0.9, ggplot2 3.4.0, rstan 2.26.0
- Stan version 2.31.0
- Analysis run on macOS 13.2 with 16GB RAM

### Preprocessing
- Temperature values below -50°C removed as instrument errors (n=3)
- Missing values: 0.2% imputed using predictive mean matching
- Outliers >3 SD from mean flagged and noted in results

### Statistical Analysis
- Random seed: 12345 (set for reproducibility)
- Bayesian model with Stan
  - Chains: 4
  - Iterations: 2000 per chain (1000 warmup)
  - Priors: Normal(0,10) for regression coefficients
  - Convergence: R̂ < 1.01 for all parameters
```

**2. Data Availability**

```markdown
## Data Availability

Raw data and analysis code are available at:
- GitHub: https://github.com/example/forest-analysis
- Zenodo: https://doi.org/10.5281/zenodo.XXXXX
- University Repository: https://[institution].edu/data/forest-diversity

Data files:
- species_observations.csv (raw observational data)
- temperature_records.csv (climate data)
- processed_dataset.csv (cleaned data used in analysis)

License: CC BY 4.0
```

**3. Code Availability and Quality**

✅ **Good Code Practices:**

```r
# Load libraries
library(tidyverse)
library(brms)

# Set seed for reproducibility
set.seed(12345)

# Load and prepare data
data <- read_csv("processed_dataset.csv") %>%
  filter(!is.na(species_richness)) %>%
  # Standardize continuous predictors
  mutate(across(c(temperature, precipitation), scale))

# Fit Bayesian model
model <- brm(
  richness ~ temperature + precipitation + (1|region),
  data = data,
  family = gaussian(),
  chains = 4,
  iter = 2000,
  warmup = 1000,
  seed = 12345,
  cores = 4
)

# Check convergence
rhat(model)  # All < 1.01

# Extract and visualize results
results <- as_draws_df(model)
post_pred <- posterior_predict(model)
```

**4. Documentation**

**README.md:**
```markdown
# Forest Biodiversity and Climate Analysis

## Overview
This repository contains data, code, and results for analyzing 
forest species richness in response to climate change across 50 sites.

## Quick Start
```bash
# Install dependencies
install.packages(c("tidyverse", "brms"))

# Run full analysis
Rscript scripts/01_data_preparation.R
Rscript scripts/02_analysis.R
Rscript scripts/03_visualization.R
```

## Repository Structure
```
project/
├── data/
│   ├── raw/
│   │   ├── species_observations.csv
│   │   └── temperature_records.csv
│   └── processed/
│       └── analysis_dataset.csv
├── scripts/
│   ├── 01_data_preparation.R
│   ├── 02_analysis.R
│   └── 03_visualization.R
├── results/
│   ├── figures/
│   └── tables/
└── README.md
```

## Methods
[Detailed methods section]

## Results
[Summary of key findings]

## Citation
Smith et al. (2024). Forest biodiversity and climate analysis. 
https://doi.org/10.5281/zenodo.XXXXX
```

**5. Sensitivity Analyses**

Show your results are robust to reasonable assumptions:

```markdown
## Sensitivity Analyses

### Alternative model specifications
- Linear vs. polynomial temperature relationships
- Including vs. excluding outliers
- Alternative imputation methods for missing data
- Different random effect structures

### Results
All models converged and showed similar patterns:
- Temperature effect consistent (β = -0.45, 95% CI: -0.52 to -0.38)
- Precipitation effect robust (β = 0.32, 95% CI: 0.25 to 0.39)
- Conclusions unchanged across specifications
```

#### 3.2 Collaboration and Contribution Framework

**Why Collaboration Matters for Open Results:**

Scientific results are produced by teams, not individuals:
- Idea generation (multiple perspectives)
- Design (collaborative refinement)
- Execution (different skills)
- Analysis (statistical and domain expertise)
- Writing (clear communication)
- Revision (feedback from multiple reviewers)

**Benefits of Transparent Collaboration:**
- Clear accountability
- Fair recognition of contributions
- Reduced conflicts
- Increased trust
- Better retention
- Enables equity

#### 3.3 Contributor Roles and Responsibilities

**Different Roles in Research:**

**1. Project Leader / Principal Investigator**
- Sets research direction
- Secures funding
- Makes final decisions
- Takes responsibility for integrity
- Leads publication process

**2. Senior Researcher / Postdoc**
- Designs detailed methods
- Conducts analyses
- Writes manuscripts
- Mentors junior staff
- Often corresponding author

**3. Graduate Student / Research Scientist**
- Conducts experiments/analyses
- Collects/processes data
- Tests hypotheses
- Writes drafts
- First author on related papers

**4. Undergraduate / Research Assistant**
- Assists with data collection
- Performs routine analyses
- Documents procedures
- Often acknowledged contributor

**5. Technical Specialist**
- Provides specialized expertise
- Operates instruments
- Develops tools/methods
- May be co-author if contribution significant

**6. Collaborator**
- Contributes specific expertise
- May contribute data
- Co-author on joint publications
- Equal partnership

**7. Data Manager / Biostatistician**
- Ensures data quality
- Conducts statistical analyses
- Develops analysis plans
- Often co-author

**8. Research Support Staff**
- Administrative support
- Lab management
- Facility operation
- Usually acknowledged

#### 3.4 Authorship and Contribution Guidelines

**Defining Authorship:**

**Traditional Definition (Problematic):**
- Only those who wrote the paper
- Excludes critical contributors
- Creates disputes

**Modern Definition (Recommended):**

Authors should meet ALL of these criteria:
1. **Substantial contributions** to conception OR design OR data acquisition OR analysis
2. **Drafting** or critically revising the work
3. **Final approval** of published version
4. **Agreement** to be accountable for work

**ICMJE Criteria** (International Committee of Medical Journal Editors)

Most widely accepted standard:
1. Substantial contributions to conception/design OR data acquisition/analysis
2. Drafting or critical revision for intellectual content
3. Final approval of version to be published
4. Accountability for all aspects of work

**CRediT Framework** (Contributor Roles Taxonomy)

More detailed specification of contributions:

```markdown
## Author Contributions

**Jane Smith:** Conceptualization, Design, Data Collection, 
Analysis, Writing - Original Draft

**Alice Johnson:** Conceptualization, Design, Data Collection, 
Funding Acquisition, Writing - Review & Editing

**Bob Brown:** Statistical Analysis, Visualization, Writing - Review & Editing

**Carol Davis:** Field Site Management, Data Collection

### Detailed CRediT Roles:
- Conceptualization: JS, AJ
- Methodology: JS, AJ, BB
- Software: BB
- Validation: BB
- Formal Analysis: BB, JS
- Investigation: JS, AJ, CD
- Resources: AJ
- Data Curation: CD
- Writing - Original Draft: JS
- Writing - Review & Editing: AJ, BB
- Visualization: BB
- Supervision: AJ
- Project Administration: AJ
- Funding Acquisition: AJ
```

**Authorship Order Conventions:**

**Standard (Sciences):**
- First author: Usually lead researcher
- Middle authors: Various contributions
- Last author: Usually PI/senior person

**Alternative conventions:**
- Equal contributions (noted explicitly)
- Alphabetical order (sometimes in mathematics)
- Senior author last, all equally contributing

**Example:**
```
Smith, J.*, Johnson, A.*, and Brown, B.
*Equal contribution
```

#### 3.5 Creating Contributor Guidelines

**CONTRIBUTING.md for Your Project:**

```markdown
# Contribution Guidelines

Thank you for interest in contributing to this research!

## Who Can Contribute?
We welcome contributions from:
- Lab members
- Collaborating researchers
- External researchers
- Anyone with relevant expertise

## How to Contribute

### For Internal Lab Members
1. Discuss ideas with PI
2. Document your work
3. Use version control
4. Write clear code/protocols
5. Share code on GitHub
6. Propose authorship discussions early

### For External Collaborators
1. Contact project lead
2. Establish collaboration agreement
3. Define contribution scope
4. Clarify authorship expectations
5. Work via shared repositories

### For Data Contributors
1. Ensure data quality
2. Document methods
3. Provide metadata
4. Agree on sharing timeline
5. Approve figures/publications using data

### For Code Contributors
1. Fork repository
2. Make feature branch
3. Write tests
4. Document changes
5. Submit pull request
6. Respond to review

## Authorship Criteria
We follow ICMJE criteria. Contributors meeting all criteria are offered authorship:
1. Substantial contributions
2. Manuscript drafting/revision
3. Final approval
4. Accountability

## Contribution Agreement
All contributors agree to:
- Follow our Code of Conduct
- Disclose conflicts of interest
- Contribute to reproducibility
- Share work openly
- Respect intellectual property

## Acknowledgment
Contributors not meeting authorship criteria will be acknowledged for:
- Providing feedback
- Facility/equipment use
- Technical assistance
- Statistical review
- Specimen preparation

## Conflict Resolution
If contribution/authorship disputes arise:
1. Discuss with immediate supervisor
2. Refer to ICMJE guidelines
3. Contact ombudsperson if needed
4. Engage mediator if necessary

## Questions?
Contact: research@example.edu
```

#### 3.6 Ensuring Reproducible Manuscript Preparation

**Creating Reproducible Manuscripts:**

**Dynamic Documents:**

Instead of separate code, results, figures, write integrated documents:

**R Markdown:**
```r
---
title: "Forest Biodiversity and Climate Change"
author: "Smith et al."
date: "`r Sys.Date()`"
output: pdf_document
---

## Methods

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo=FALSE)
library(tidyverse)
data <- read_csv("data.csv")
```

We analyzed `r nrow(data)` observations from `r n_distinct(data$site)` sites.

## Results

```{r analysis}
model <- lm(richness ~ temperature, data=data)
```

Temperature had a significant effect (β = `r coef(model)[2]`, p < 0.001).

```{r fig, fig.cap="Relationship between temperature and species richness"}
plot(richness ~ temperature, data=data)
abline(model)
```
```

**Jupyter Notebooks:**
```python
# Forest Biodiversity Analysis

import pandas as pd
import numpy as np
from scipy import stats

# Load data
data = pd.read_csv('data.csv')

print(f"Dataset has {len(data)} observations from {data['site'].nunique()} sites")

# Statistical analysis
slope, intercept, r_value, p_value, se = stats.linregress(
    data['temperature'], 
    data['richness']
)

print(f"Temperature effect: β = {slope:.3f}, p = {p_value:.4f}")
```

**Benefits:**
- Code runs to generate figures
- Numbers update automatically
- Errors visible immediately
- Transparent methods
- Reproducible output

**Manuscript Checklist for Open Results:**

- ✅ Methods section detailed enough to replicate
- ✅ All data available with open license
- ✅ Analysis code available and runs successfully
- ✅ Random seeds specified for stochastic procedures
- ✅ Software versions documented
- ✅ Assumptions and limitations discussed
- ✅ Sensitivity analyses included
- ✅ Conflicts of interest disclosed
- ✅ Funding sources stated
- ✅ Author contributions clearly specified
- ✅ Data availability statement included
- ✅ Code availability statement included
- ✅ Preregistration mentioned (if applicable)
- ✅ DOIs provided for data/code

#### Summary

Making open results requires:
1. **Computational Reproducibility:** Code, data, methods all available
2. **Transparent Collaboration:** Clear roles and contribution documentation
3. **Equitable Recognition:** Proper authorship and acknowledgment
4. **Complete Documentation:** Enough detail for others to replicate
5. **Accessible Sharing:** Publishing code, data, and results openly

By following these practices, you produce research that is verifiable, trustworthy, and maximally useful to the scientific community.

### Lesson 4: Sharing Open Results

:::{admonition} Activities for Lesson 3
:class: activity

Complete at least two of the following activities to practice making open results:

**Activity 3.1: Create Contributor Guidelines**
Develop a CONTRIBUTING.md file for a research project (real or hypothetical):
- Define what constitutes a contribution
- Outline how people can get involved
- Clearly specify authorship criteria using ICMJE guidelines
- Include acknowledgment categories for non-author contributors
- Create a conflict-of-interest disclosure form
- Add your contact information and next steps

Share with colleagues and incorporate their feedback.

**Activity 3.2: Document Your Code for Reproducibility**
Take a piece of your analysis code (or create a simple example):
- Add comprehensive comments explaining each step
- Create a README file with:
   - Overview of what the code does
   - Software and package requirements with versions
   - Instructions for running the code
   - Expected inputs and outputs
   - Known limitations
- Create a requirements.txt or environment file
- Test that someone unfamiliar with your work could run the code successfully

**Activity 3.3: Write a Data Availability Statement**
For a dataset you're working with (real or hypothetical), write a complete data availability statement that includes:
- Where the data is/will be stored
- How it can be accessed
- Any restrictions on access (and why)
- License information
- How to cite the data
- Version information
- DOI or persistent identifier

Include this statement in a manuscript or research plan.

**Activity 3.4: Define Authorship for Your Project**
For a current or planned research project:
- List all team members and their anticipated contributions
- Apply the ICMJE criteria to determine who should be authors
- Assign specific CRediT roles to each team member
- Create an authorship agreement document that team members can sign
- Plan how you will discuss authorship throughout the project (e.g., at regular meetings)

**Activity 3.5: Conduct a Reproducibility Audit**
For your own research project:
- Create a checklist of reproducibility elements (data, code, documentation, etc.)
- Assess which elements are currently available
- Identify what's missing
- Make an action plan to fill gaps before publication
- Estimate the time needed for each action
- Commit to completing at least one item this month
:::

### Lesson 4: Sharing Open Results

#### Overview
In this lesson we will place emphasis on publishing manuscripts as open access. You will learn what subtleties to consider when determining what journal to publish in, including how to make sense of a journal's policies on self-archiving. Finally, we discuss some commonly held concerns about sharing open access publications, and how to overcome them. Ultimately, we want to ensure that you have confidence in your decision to publish as open access.

#### 4.1 Open Access Publishing Models

**What Is Open Access?**

Open access (OA) means research is freely available online for anyone to read, download, and reuse without payment or subscription barriers.

**Why Open Access Matters:**

- **Maximizes Impact:** More readers = more citations
- **Public Benefit:** Taxpayers can access funded research
- **Global Equity:** Researchers in low-income countries access research
- **Speed:** Findings available immediately, not after embargoes
- **Discoverability:** Higher visibility in search engines and repositories
- **Compliance:** Many funders now require OA

**Open Access Models:**

**1. Gold Open Access (Publisher OA)**

**Advantages:**
- ✅ Published immediately open
- ✅ Professionally formatted and copyedited
- ✅ Appears in journal with full prestige
- ✅ Citable with journal name
- ✅ Clear version of record

**Disadvantages:**
- ✅ Author Pays model: $1,000-$5,000+ per article
- ✅ Impacts of excessive fees on authors without funding
- ✅ Not all journals offer

**Examples:** PLOS, Frontiers, eLife, Nature Communications

**2. Green Open Access (Repository OA)**

**Advantages:**
- ✅ Free to author and reader
- ✅ Can self-archive peer-reviewed articles
- ✅ Publicly available regardless of subscription
- ✅ No fees required

**Disadvantages:**
- ✅ Embargo periods (6-24 months before can post)
- ✅ Often only postprint available, not final PDF
- ✅ Requires author initiative to archive
- ✅ Visibility lower than gold OA

**How it works:**
1. Publish in traditional journal (author or institution pays)
2. After embargo period, deposit copy in:
   - Institutional repository
   - Discipline-specific repository (PubMed Central, ArXiv, etc.)
   - Preprint servers
   - Personal website (if rights allow)

**3. Hybrid Open Access**

**Concept:**
Journal still has subscription model, but individual articles can be OA for a fee

**Advantages:**
- ✅ OA available immediately
- ✅ Author can choose per article
- ✅ Subscriber access included
- ✅ Less expensive than full gold OA

**Disadvantages:**
- ✅ Still requires author fees
- ✅ Double-dipping criticism (subscribers + author fees)
- ✅ Confusing licensing status

**Examples:** Wiley journals, Springer, Elsevier

**4. Preprint Model**

**Concept:**
Share work before, during, or without peer review

**Advantages:**
- ✅ Immediate sharing
- ✅ Establishes precedence
- ✅ Rapid feedback
- ✅ Can eventually be published

**Disadvantages:**
- ✅ Not peer-reviewed (initially)
- ✅ Some journals don't accept preprinted work
- ✅ Needs clear labeling

**Examples:** ArXiv, bioRxiv, medRxiv, OSF Preprints

**5. Diamond (Platinum) Open Access**

**Concept:**
Free for authors and readers, supported by institutions/funding

**Advantages:**
- ✅ No author fees
- ✅ No reader fees
- ✅ True open access
- ✅ Sustainable funding model

**Disadvantages:**
- ✅ Fewer journals available
- ✅ May have lower impact factors
- ✅ Limited resources for support

**Examples:** European journals often diamond OA, some society journals

#### 4.2 Evaluating and Selecting Journals

**Factors to Consider Beyond Impact Factor:**

**1. Open Access Status**

**Check:**
- Is it fully OA, hybrid, or subscription-only?
- Author pay or free?
- What licenses are used?
- Green OA policies (can you self-archive)?

**Resources:**
- **Directory of Open Access Journals (DOAJ):** doaj.org
- **Journal Checker Tool:** journalcheckertool.org
- **Open Access Button:** openaccessbutton.org
- **Sherpa/RoMEO:** sherpa.ac.uk/romeo (self-archiving policies)

**2. Audience and Scope**

- Does journal publish in my field?
- Who are typical readers?
- Is this the right venue for my work?
- Will it reach intended audience?

**3. Review Process**

- Traditional or open peer review?
- How long is review typically (months?)?
- Single or multiple reviewers?
- What is desk rejection rate?
- Are conflicts of interest managed?

**4. Journal Quality Indicators**

**✅ Good Signs:**
- Publishes open science (open data statements required)
- Rapid publication timeline
- Transparent editorial practices
- Disclosures and corrections published
- Engaged editorial board

**⚠️ Warning Signs:**
- Excessive impact factor claims
- No clear review process
- Limited editorial transparency
- Predatory publishing indicators
- No conflict of interest policies

**5. Predatory Journal Detection**

**Warning Signs:**
- ❌ Unsolicited submissions requests
- ❌ No clear peer review
- ❌ Inflated impact metrics
- ❌ Hidden fees
- ❌ Generic scope (publishes everything)
- ❌ No plagiarism checking
- ❌ Email with many misspellings
- ❌ Named editors who deny involvement

**Resources:**
- **Predatory Journal Check:** predatoryjournals.com (use with caution)
- **DOAJ Directory:** if listed, more likely legitimate
- **Ask librarian:** institutional librarians can help evaluate

**6. Practical Considerations**

**Cost:**
- Can your institution/grant cover author fees?
- Are there waivers for low-income countries?
- Is there a green OA option (free)?

**Timeline:**
- How long is the review process?
- When do you need results published?
- Is preprint an option?

**Impact:**
- Who reads this journal?
- How many citations do similar papers get?
- Will this advance my career?

#### 4.3 Open Access Policies and Self-Archiving

**Understanding Self-Archiving Rights:**

**What Is Self-Archiving?**

Posting a copy of your published paper in a public repository, after the publisher's embargo period

**When Can You Archive?**

**Immediately (No Embargo):**
- ✅ Your preprints (always)
- ✅ Gold OA journals (upon publication)
- ✅ Green OA journals that allow (check Sherpa/RoMEO)

**After Embargo Period:**
- Most subscription journals allow 6-24 months after publication
- Check journal policy specifically

**Never (Rights Retained by Publisher):**
- ❌ Some closed-access journals forbid
- ❌ Always check before archiving

**Where to Archive:**

**1. Institutional Repository**
- University website
- Often free
- Visible to institution
- May be harvested to broader archives

**2. Discipline-Specific Repository**
- PubMed Central (biomedical)
- ArXiv (physics, math, CS)
- PsyArXiv (psychology)
- Zenodo (multidisciplinary)

**3. Preprint Servers**
- bioRxiv, medRxiv, etc.
- Can post any time (before, during, after peer review)

**4. Personal/Lab Website**
- Some journals allow
- Check publisher policy first
- Less discoverable than repositories

**Finding Your Journal's Policy:**

1. **Sherpa/RoMEO:** sherpa.ac.uk/romeo
   - Search journal name
   - Shows archiving permissions
   - Lists allowed versions (preprint, postprint, PDF)

2. **Journal Website:**
   - Look for author rights/copyright policy
   - Check FAQ section
   - Contact copyright@journalname.com

3. **Ask Your Librarian:**
   - They know journal policies
   - Can help understand restrictions

**Example Policy:**
```
Publisher: Wiley
Journal: Journal of Ecology

Archiving Policy (Sherpa/RoMEO): GREEN
- Can archive preprint: Yes
- Embargo: 12 months
- Can archive postprint: Yes (accepted manuscript)
- Embargo: 12 months
- Can archive publisher's PDF: No

Meaning: Can post your preprint immediately and accepted manuscript 
after 12 months, but not final publisher's PDF.
```

#### 4.4 Concerns About Open Access and Rebuttals

**Concern 1: "Publishing OA hurts my reputation"**

**Myth or Reality?** Myth

**Evidence:**
- ✅ OA papers cited more frequently
- ✅ Top journals increasingly offer OA
- ✅ Funders mandate OA
- ✅ OA no longer perceived as lower quality

**Reality Check:**
- Quality depends on journal rigor, not access model
- Many prestigious journals are OA (eLife, PLOS, Nature Communications)

**Concern 2: "OA journals are too expensive"**

**Reality:** Some charge, but alternatives exist

**Solutions:**
- ✅ Use green OA (free)
- ✅ Publish in diamond OA (no fees)
- ✅ Request fee waivers
- ✅ Use your institution's OA fund
- ✅ Negotiate with publishers
- ✅ Publish preprints first

**Concern 3: "OA journals have lower impact/quality"**

**Evidence Against:**
- ✅ PLOS ONE highly cited
- ✅ eLife publishes prestigious research
- ✅ Nature Communications has high impact factor
- ✅ Journal quality ≠ OA vs. closed

**Reality Check:**
- Quality varies within OA and closed access
- Judge journal by rigor, not access model

**Concern 4: "Preprints are not citable"**

**Reality:** Increasingly citable and valued

**Evidence:**
- ✅ ArXiv citations respected in physics/math
- ✅ BioRxiv citations growing rapidly
- ✅ Many journals now allow preprint citations
- ✅ Preprints have DOIs

**Best Practice:**
Cite preprints when appropriate, but note "preprint" in citation

**Concern 5: "Sharing before publication risks being scooped"**

**Reality:** Risk is minimal with proper dating

**Protections:**
- ✅ Preprints have timestamp (prevents scooping)
- ✅ Establishing precedence
- ✅ Building community priority
- ✅ Some journals welcome preprints

**Best Practice:**
Post preprint or submit paper quickly to establish priority

**Concern 6: "Who will curate and preserve OA publications?"**

**Reality:** Multiple archives ensure preservation

**Preservation Solutions:**
- ✅ CLOCKSS/LOCKSS: Global digital preservation
- ✅ Portico: Journal preservation service
- ✅ Internet Archive: Wayback Machine
- ✅ Institutional repositories
- ✅ Discipline repositories

**These services:** Ensure long-term access even if publisher fails

#### 4.5 Open Access Best Practices

**Strategy for OA Publication:**

**Immediate OA:**

If you have funding:
1. Publish in gold OA journal
2. Use hybrid option in subscription journal
3. Share immediately on preprint server

**Delayed OA:**

If no funding:
1. Publish in subscription journal
2. Post preprint on bioRxiv/ArXiv immediately
3. Self-archive accepted manuscript in institutional repository after embargo
4. Share on personal/lab website

**Combination Strategy:**

```markdown
# Publication Timeline Strategy

**Day 0:** Submit paper
- Make preprint available (bioRxiv)
- Share on lab website

**Month 3:** Under review
- Announce manuscript on social media
- Discuss with colleagues
- Get feedback

**Month 6:** Accepted
- Ensure all data/code publicly available
- Include data availability statement
- Coordinate with journal

**Month 7:** Published
- If subscription journal:
  - Post accepted manuscript in institutional repository (after embargo)
  - Share on personal website
  - Alert everyone to preprint version
- If OA journal:
  - Celebrate open publication
  - Share widely
  - Track downloads/citations

**Months 8-12:** Post-publication
- Respond to comments
- Share additional analyses
- Support replication efforts
```

**Making Your Work Discoverable:**

1. **Ensure Full Accessibility:**
   - Post PDFs where possible
   - Use common formats
   - Avoid paywalls

2. **Include Rich Metadata:**
   - Full abstract
   - Keywords
   - Author names (multiple formats)
   - Funding information
   - DOI

3. **Make It Findable:**
   - Register with Google Scholar
   - Share on ResearchGate, Academia.edu
   - Announce on social media
   - Link from institutional pages
   - Include in CV

4. **Support Reuse:**
   - Use explicit license (CC BY, CC0)
   - Encourage sharing
   - Enable machine reading
   - Support data reuse

#### Summary

Sharing open results via open access publications ensures:
1. **Immediate Access:** No paywalls limiting readership
2. **Maximum Impact:** Higher citations and visibility
3. **Equitable Access:** Researchers worldwide can read
4. **Compliance:** Meeting funder requirements
5. **Career Benefit:** Open work has more impact

Multiple pathways to OA exist; choose the best option for your situation.

### Lesson 5: From Theory to Practice

:::{admonition} Activities for Lesson 4
:class: activity

Complete at least two of the following activities to practice sharing open results:

**Activity 4.1: Evaluate Journals for Open Access Options**
For your field, identify 5-10 journals where you might publish:
- Check each journal's open access options using DOAJ, Journal Checker Tool, or Sherpa/RoMEO
- Create a comparison table showing:
   - Journal name and field
   - Open access options (gold, hybrid, green)
   - Author fees (if applicable)
   - Self-archiving policies and embargo periods
   - Quality indicators (peer review process, impact metrics, editorial transparency)
- Identify your top 3 choices and explain your reasoning
- Calculate the cost of publishing gold OA in each and explore fee waiver options

**Activity 4.2: Create a Publication Strategy Timeline**
For a current or planned research project, develop a detailed publication strategy:
- Identify target journals (primary and alternatives)
- Estimate timeline for each stage (data collection, analysis, writing, submission, review, publication)
- Decide on preprint strategy (when and where to post)
- Plan data and code release (concurrent with publication? After embargo?)
- Outline your communication strategy (press release, social media, blog, etc.)
- Include contingencies for rejection and revision

**Activity 4.3: Self-Archive a Paper**
If you have a published paper, practice self-archiving it:
- Check the journal's policy using Sherpa/RoMEO
- If allowed, deposit a copy in:
   - Your institutional repository
   - A discipline-specific repository (PubMed Central, ArXiv, etc.)
   - Zenodo or similar service
- Add proper metadata and DOIs
- Verify that the paper is now accessible through multiple channels
- Reflect on how increasing access changes visibility of your work

**Activity 4.4: Write an Open Access Justification**
Prepare an argument for your advisor or institution about why publishing open access matters for your research:
- Gather evidence on OA citation impact
- Calculate the long-term costs vs. benefits of OA vs. subscription publishing
- Address specific concerns in your field about OA
- Propose how to fund OA publications (institutional support, grants, etc.)
- Write a 500-word position paper you could share with decision-makers

**Activity 4.5: Design a Communication Strategy for Your Results**
Develop a comprehensive communication plan for sharing your results:
- Who is your audience? (scientists, policymakers, public, practitioners, etc.)
- What are the key messages for each audience?
- What formats will you use? (manuscript, preprint, blog, video, infographic, social media, press release)
- What timeline works for each format?
- How will you measure success/impact?
- Create mockups or draft text for at least 3 different formats
:::

### Lesson 5: From Theory to Practice

#### Overview
In this lesson, we tie the concepts from previous lessons together with some specific guidance for writing the Sharing Results section of an Open Science and Data Management Plans (OSDMP). We will also reflect on how our society and technology constantly evolve, as does the way we do and share science. A new technology with the potential to radically alter the way we do and share science is artificial intelligence (AI), particularly when it comes to large language models. These AI tools are already changing how we interact with written text. In this lesson, we discuss some of the ways that AI is and will affect how we do and share our science.

#### 5.1 Writing the Sharing Results Section of an OSDMP

**What Is an OSDMP?**

An Open Science and Data Management Plan (OSDMP) integrates:
- Data management planning
- Software/code planning
- Results sharing planning
Into one cohesive document

**Why Write a Sharing Results Section?**

- **Funder Requirement:** Most now require SMD guidance compliance
- **Planning Tool:** Forces thinking through publication strategy
- **Communication:** Aligns team on expectations
- **Documentation:** Records decisions and rationale
- **Accountability:** Demonstrates commitment to open science

#### 5.1.1 Components of Results Sharing Section

**1. Publication Strategy**

```markdown
## Publication Strategy

### Target Journals
- Primary: Nature Climate Change, Global Change Biology
- Alternative: Journal of Applied Ecology, Ecology Letters
- Preprint: bioRxiv for rapid dissemination

### Publication Timeline
- Data collection + analysis: Months 1-24
- Manuscript writing: Months 18-24
- Submission: Month 24
- Publication expected: Month 30

### Open Access Strategy
- Primary: Gold OA (Nature Communications if accepted)
- Backup: Green OA to institutional repository after embargo
- Preprint: Immediate posting to bioRxiv
- License: CC BY 4.0 for all publicly shared versions

### Rationale
Nature Climate Change has highest impact in our field and offers OA 
option. Alternative journals ensure publication even if rejected. 
BioRxiv provides rapid community access to findings.
```

**2. Manuscript and Supplementary Materials Plan**

```markdown
## Manuscript Preparation

### Main Manuscript
- Title: "Forest Biodiversity Shifts Under Climate Change (1980-2023)"
- Target length: 40-50 pages including figures
- Main text: Methods, results, discussion (~30 pages)
- Figures: 6 main figures, each carefully designed
- Tables: 3 main summary tables

### Supplementary Materials
Supplementary Data:
1. Detailed site information (100 forest sites)
2. Species list with taxonomy validation
3. Temperature and precipitation data
4. Statistical model specifications
5. Sensitivity analysis results
6. Additional figures (15 supplementary figures)

Supplementary Methods:
1. Detailed field sampling protocols (5 pages)
2. Species identification procedures (3 pages)
3. Statistical methodology (10 pages)
4. Data quality assessment (5 pages)

Supplementary Code:
1. Data cleaning script (R)
2. Statistical analysis script (R)
3. Figure generation script (R)
4. README with instructions
```

**3. Data Availability and Accessibility**

```markdown
## Data Sharing Plan

### Dataset Description
- Raw species observations: 500,000 records from 100 sites
- Temperature data: Daily from 1980-2023
- Processed dataset: Analysis-ready format

### Timeline
- Raw data: Shared upon publication (to preserve priority)
- Processed data: Published concurrently with manuscript
- Derived data: Available immediately

### Repository Selection
- Primary: Dryad (for data with manuscript)
- Secondary: Zenodo (long-term archival)
- Institutional: University data repository

### Format and Documentation
- Format: CSV for tables, NetCDF for spatial/temporal data
- Metadata: Comprehensive README files
- Codebook: Complete variable dictionary
- Quality info: Data quality flags documented
- Licenses: CC0 (public domain) to maximize reuse

### Access Control
- All data publicly available (no restrictions)
- No registration or approval required
- DOIs assigned for citation
```

**4. Code and Analysis Sharing**

```markdown
## Code and Analysis Sharing

### Analysis Code
- Location: GitHub (github.com/example/forest-analysis)
- Language: R (with accompanying Python scripts)
- License: MIT License
- Accessibility: Public, no registration needed

### Code Availability
- Concurrent with publication
- Version control (Git) from beginning of analysis
- Release: Tagged version matching submitted manuscript
- DOI: Obtain via Zenodo GitHub integration

### Code Documentation
- README: Quick start guide
- Comments: In-code explanation of key steps
- Examples: Sample runs with test data
- Requirements: Package list with versions

### Reproducibility
- Fully reproducible from raw data to figures
- Docker container provided for exact environment
- Test data included for verification
- Random seed specified for stochastic procedures
```

**5. Communication and Outreach**

```markdown
## Results Communication

### Preprint Strategy
- Post to bioRxiv at journal submission
- Include statement: "This is a preprint and not yet peer-reviewed"
- Announce via social media
- Share with relevant mailing lists

### Manuscript Discussion
- Open online platform for feedback
- Respond to questions and critiques
- Engage with broader community
- Support replication efforts

### Broader Dissemination
- Press release through university
- Blog post explaining key findings
- Tweet thread summarizing main results
- Conference presentations (3-4 meetings)
- Public seminar/webinar

### Engagement with Stakeholders
- Forest managers: Direct discussion of implications
- Policy makers: Brief for environmental policy
- Public: Accessible summary for general audience
- Colleagues: Detailed presentation and discussion
```

**6. Authorship and Contributions**

```markdown
## Authorship and Contributions

### Authorship Criteria
We follow ICMJE criteria. Authorship includes anyone who:
1. Makes substantial contributions to conception/design or 
   data acquisition/analysis
2. Drafts or critically revises for intellectual content
3. Approves final version
4. Is accountable for the work

### Anticipated Authors
Primary authors:
- Dr. Jane Smith (PI): Conception, design, funding, writing
- Alice Johnson (Postdoc): Design, analysis, writing
- Bob Brown (Grad student): Data collection, analysis, writing

Contributor roles (CRediT):
- Conceptualization: JS, AJ
- Methodology: JS, AJ
- Data curation: BB, CD
- Analysis: AJ, BB
- Writing: JS, AJ, BB
- Funding: JS

### Acknowledgment
Contributors not meeting authorship criteria will be acknowledged for:
- Statistical consultation
- Facility access
- Research assistance
- Manuscript feedback
```

#### 5.2 Impact of Artificial Intelligence on Open Science

**The AI Revolution in Science:**

Artificial Intelligence, particularly large language models (LLMs), is transforming how science is conducted and communicated.

#### 5.2.1 How AI Is Changing Scientific Research

**1. Literature Analysis and Synthesis**

**Current Use:**
- ChatGPT, Claude summarize papers
- Scoping reviews conducted faster
- Literature gaps identified
- Themes and patterns extracted

**Implications for Open Science:**
- More comprehensive literature reviews possible
- Need for machine-readable abstracts
- Greater value of open access papers
- Better discoverability of findings

**Best Practices:**
- ✅ Verify AI-generated summaries against originals
- ✅ Disclose AI tool use in methods
- ✅ Use for synthesis, not final interpretation
- ✅ Cite original papers, not AI summaries

**2. Data Analysis and Visualization**

**Current Use:**
- Generate analysis code from natural language
- Create figures and visualizations
- Suggest statistical approaches
- Identify patterns in large datasets

**Example:**
```
Prompt: "I have a CSV with temperature, precipitation, and species 
richness data. Generate R code to create a correlation plot."

Response: [Generates ggplot code]
```

**Implications:**
- ✅ More thorough exploratory analyses
- ✅ Faster prototyping
- ⚠️ Risk of inappropriate methods
- ⚠️ Need for verification

**Best Practices:**
- ✅ Verify code before running
- ✅ Understand methods suggested
- ✅ Include generated code in repository
- ✅ Disclose AI tool use
- ✅ Check results for reasonableness

**3. Manuscript Writing and Editing**

**Current Use:**
- Grammar and style improvement
- Outlining and organization
- Abstract generation
- Clarity enhancement
- Translation

**Example:**
```
Original: "The analyses were performed using statistical methods 
to determine if there was a relationship."

AI Improved: "We used linear regression to test whether temperature 
affected species richness."
```

**Implications:**
- ✅ Improved writing quality
- ✅ Faster manuscript preparation
- ⚠️ Loss of author voice
- ⚠️ Potential accuracy issues
- ⚠️ Authorship questions

**Best Practices:**
- ✅ Use AI for polishing, not generation
- ✅ Maintain scientific accuracy
- ✅ Disclose substantial AI use
- ✅ Verify all AI-assisted content
- ✅ Understand guidelines for your journal

**4. Hypothesis Generation and Research Design**

**Current Use:**
- Suggest novel research questions
- Identify research gaps
- Design experiments
- Anticipate results

**Implications:**
- ✅ Novel research directions
- ⚠️ May duplicate existing work
- ⚠️ Potential for inappropriate methods

**Best Practices:**
- ✅ Use AI suggestions to inspire
- ✅ Verify novelty through literature review
- ✅ Consult with experts
- ✅ Document AI-assisted ideation

#### 5.2.2 Risks and Concerns with AI in Research

**1. Accuracy and Hallucinations**

**Issue:** LLMs generate plausible-sounding but false information

**Example:**
- AI cites non-existent papers
- AI describes methods differently than described
- AI "invents" statistical results

**Mitigation:**
- ✅ Verify all AI-generated facts
- ✅ Cross-check citations
- ✅ Don't trust AI for critical facts
- ✅ Use AI as assistant, not authority

**2. Authorship and Credit**

**Issue:** Unclear if AI assistance constitutes authorship

**Current Guidance:**
- Most journals: AI cannot be author
- Must disclose AI tool use
- Human responsible for content
- Declare extent of AI assistance

**Example Disclosure:**
```
Author Contributions: JS and AJ designed the study, collected data, 
and conducted analyses. All authors wrote the manuscript. ChatGPT 
was used to improve grammar and clarity of the final draft.
```

**3. Bias in AI Models**

**Issue:** AI trained on biased data reproduces biases

**Examples:**
- Overrepresentation of English-language papers
- Overrepresentation of certain researchers/institutions
- Biased summaries of controversial topics
- Preferred methodologies in training data

**Mitigation:**
- ✅ Be aware of AI training data
- ✅ Seek diverse perspectives beyond AI
- ✅ Fact-check summary statements
- ✅ Supplement with manual literature review

**4. Intellectual Property and Licensing**

**Issue:** Unclear rights when AI uses copyrighted material

**Concerns:**
- AI trained on all available papers (including paywalled)
- Copyright and licensing implications
- Fair use vs. commercial use

**Best Practices:**
- ✅ Use AI from reputable providers
- ✅ Understand their data sources
- ✅ Check licensing terms
- ✅ Favor open science data

**5. Reproducibility and Transparency**

**Issue:** AI-generated content may not be reproducible

**Challenges:**
- Different prompts yield different outputs
- Non-deterministic results
- Hard to replicate exact AI output
- Version changes affect results

**Best Practices:**
- ✅ Document AI prompts used
- ✅ Include AI-generated content in supplementary
- ✅ Provide version and date of AI tool
- ✅ Verify reproducibility independently

#### 5.2.3 Opportunities for AI in Open Science

**1. Accelerating Discovery**

- Rapid literature synthesis
- Pattern identification in large datasets
- Hypothesis generation
- Novel connections across fields

**Result:** Faster scientific progress

**2. Improving Accessibility**

- Translation of papers
- Simplified explanations of complex findings
- Making science more accessible
- Reaching broader audiences

**Result:** More equitable science access

**3. Enhancing Reproducibility**

- Automatic code generation
- Verification of statistics
- Checking methodology consistency
- Identifying common errors

**Result:** Higher quality research

**4. Supporting Equity**

- Assistance for non-native speakers
- Help for researchers in low-resource settings
- Lowering barriers to publication
- Assisting with statistical guidance

**Result:** More inclusive science

#### 5.2.4 Guidelines for Responsible AI Use in Research

**General Principles:**

1. **Transparency**
   - Disclose all AI tool use
   - Document methods and extent of use
   - Be honest about limitations

2. **Verification**
   - Don't trust AI output blindly
   - Verify facts and methods
   - Check citations
   - Test code

3. **Accuracy**
   - Ensure scientific accuracy
   - Maintain rigorous standards
   - Don't compromise quality

4. **Accountability**
   - Researchers remain responsible
   - Can't blame AI for errors
   - Must understand all content

5. **Equity**
   - Consider access disparities
   - Ensure AI doesn't widen gaps
   - Support inclusive practices

**Specific Guidance:**

**For Literature Review:**
- ✅ Use AI to organize and summarize
- ✅ Do your own synthesis
- ✅ Verify key facts
- ✅ Don't skip reading original papers

**For Data Analysis:**
- ✅ Use AI to generate starter code
- ✅ Understand what code does
- ✅ Test thoroughly
- ✅ Disclose AI assistance

**For Writing:**
- ✅ Use for editing, not generation
- ✅ Maintain your voice and ideas
- ✅ Verify all content
- ✅ Disclose substantial assistance

**For Idea Generation:**
- ✅ Use as brainstorming partner
- ✅ Verify novelty independently
- ✅ Don't over-rely on AI suggestions
- ✅ Consult with colleagues

#### 5.3 Implementation Roadmap for Open Results

**For Your Next Research Project:**

**Before Starting (Month -1):**
- Develop OSDMP with results sharing section
- Define publication targets
- Establish team communication norms
- Create contributor guidelines
- Plan preregistration (if applicable)

**During Research (Months 1-24):**
- Document everything thoroughly
- Use version control for code
- Regular progress communication
- Share drafts with team
- Plan supplementary materials

**Before Submission (Month 24):**
- Finalize data and code
- Write full reproducibility documentation
- Create supplementary materials
- Prepare data availability statement
- Select target journal

**At Submission (Month 24):**
- Post preprint if possible
- Ensure data/code ready for sharing
- Obtain DOIs for manuscripts/data
- Include data availability statement
- Announce submission to team

**Upon Acceptance (Month 30):**
- Publish data and code
- Share in repositories
- Announce publication widely
- Prepare for questions/feedback
- Update OSF/GitHub

**Post-Publication (Ongoing):**
- Respond to questions
- Share supplementary analyses
- Support replication efforts
- Track citations
- Maintain repositories

#### 5.4 Practical Examples

**Complete OSDMP Results Section Example:**

```markdown
# Open Science and Data Management Plan: Forest Biodiversity Study

## Results Sharing Plan

### Publication Strategy
**Target Journals:** (in order of preference)
1. Nature Climate Change (OA option available)
2. Global Change Biology (Green OA policy)
3. Journal of Applied Ecology

**Preprint:** bioRxiv at submission

**Timeline:**
- Data analysis completion: Month 20
- Draft manuscript: Month 22
- Team review: Month 23
- Submission: Month 24
- Expected publication: Month 30

### Manuscript Content

**Main Manuscript:**
- Title: "Divergent responses of forest biodiversity to climate change across latitudes, 1980-2023"
- Length: 40-50 pages
- 6 main figures
- 3 summary tables

**Supplementary Materials:**
- Extended methods (15 pages)
- Additional figures (20 figures)
- Sensitivity analyses
- Species list with taxonomy

### Data Sharing

**Datasets:**
1. Raw observations (500,000 records)
2. Temperature and precipitation time series
3. Processed analysis dataset
4. Site metadata

**Repositories:**
- Primary: Dryad (linked with manuscript)
- Secondary: Zenodo (long-term archival)
- Institutional: University data repository

**Timeline:** Concurrent with publication

**Format:** CSV and NetCDF

**License:** CC0 (public domain)

**DOI:** Will be assigned by repository

### Code and Analysis

**Repository:** GitHub (github.com/smith/forest-biodiversity)

**Contents:**
- All analysis code (R and Python)
- Data processing scripts
- Figure generation code
- Test data
- Dockerfile for reproducibility

**License:** MIT

**Documentation:**
- README with quick start
- Inline code comments
- Requirements file with package versions
- Example analysis notebook

**Availability:** Concurrent with publication

**DOI:** Will be obtained via Zenodo integration

### Authorship and Contributions

**Anticipated Authors:**
- Smith, J. (PI) - Conception, design, funding, analysis, writing
- Johnson, A. (Postdoc) - Design, analysis, writing
- Brown, B. (Graduate Student) - Data collection, analysis, writing
- Davis, C. (Research Technician) - Acknowledgment for field assistance

**Authorship Criteria:** ICMJE standards

**Contributions** (CRediT):
- Conceptualization: SJ, JA
- Methodology: SJ, JA
- Software: JA
- Validation: JA, BB
- Formal analysis: JA, BB
- Investigation: SJ, JA, BB
- Resources: SJ
- Data curation: BB
- Writing - original draft: SJ
- Writing - review & editing: SJ, JA, BB
- Visualization: JA, BB
- Supervision: SJ
- Project administration: SJ
- Funding acquisition: SJ

### Communication and Outreach

**Preprint Strategy:**
- Post to bioRxiv with at-submission note
- Share via Twitter and lab website
- Announce via relevant mailing lists

**Post-Publication Communication:**
- Press release through university
- Blog post explaining findings
- Conference presentations (3-4 meetings)
- Public webinar
- Update to policy makers

### Data Management

**Storage During Project:**
- Primary: Lab server with daily backup
- Secondary: University secure storage
- Cloud: Regularly synced to Box/Dropbox

**Data Quality Assurance:**
- Automated validation checks
- Manual verification of 10% of data
- Cross-checking with source datasets
- Quality flags documented

**Access Control:**
- During research: Restricted to team
- Public: Upon manuscript publication
- No authentication required for published data

### Sustainability and Long-term Preservation

**Maintenance Responsibility:**
- Years 1-3: PI and postdoc
- Years 3+: Zenodo and institutional repository

**Archival:**
- Data archived on Zenodo and university repository
- Code archived on Zenodo via GitHub integration
- Published version maintained on journal website

**Retention Period:**
- Minimum 7 years (per funder requirement)
- Expected: Indefinite (via repositories)

### Compliance and Ethics

**Funder Requirements:**
- NSF SMD Data Management and Sharing Plan: Compliant
- Open science: Plans for immediate dissemination
- Data preservation: 7-year minimum

**Ethical Considerations:**
- No human subjects or sensitive data
- No export control concerns
- No conflicts of interest

### Budget

**Data Management and Sharing Costs:**
- Repository fees: $0 (Zenodo free, Dryad covered by library)
- Data curator time: Included in project
- Total: No additional cost
```

#### Summary

From theory to practice requires:
1. **Planning:** Clear OSDMP section on results sharing
2. **Awareness:** Understanding AI's role in modern research
3. **Implementation:** Following best practices for open results
4. **Adaptation:** Adjusting to evolving technologies
5. **Commitment:** Sustained effort to advance open science

By putting these principles into practice, you contribute to a more transparent, reproducible, and impactful scientific enterprise that serves both the research community and society at large.

## References

:::{admonition} Activities for Lesson 5
:class: activity

Complete at least one of the following activities to integrate open results into your research practice:

**Activity 5.1: Write Your Sharing Results OSDMP Section**
Following the template and guidance in section 5.1, write the Sharing Results section of an Open Science and Data Management Plan for a current or planned research project:
- Publication strategy (target journals, timeline, open access approach)
- Manuscript and supplementary materials plan
- Data availability and accessibility plan
- Code and analysis sharing plan
- Communication and outreach strategy
- Authorship and contribution framework

Have your advisor or colleague review it and provide feedback.

**Activity 5.2: Develop a Lab Open Science Policy**
Create a policy document for your research group that outlines standards for open results:
- Expectations for data sharing
- Code documentation and sharing requirements
- Default licenses for data and software
- Preprint practices
- Authorship decision-making process
- Collaboration agreements
- Timeline for sharing results (concurrent with publication vs. embargo)

Present this to your lab and discuss how to implement it.

**Activity 5.3: Evaluate AI Tools for Your Research**
Research how AI tools (ChatGPT, Claude, specialized scientific AI) could be used ethically in your research:
- Literature synthesis and analysis
- Code writing and debugging
- Figure generation and interpretation
- Manuscript writing and editing
- Data analysis and visualization

Write a reflection (300-500 words) on:
- Which applications are most relevant to your work
- Potential benefits and risks
- Ethical considerations
- How you would disclose AI use in publications
- Your guidelines for responsible AI use in research

**Activity 5.4: Create a Continuous Open Science Improvement Plan**
Develop a personal or lab action plan for advancing open science practices:
- Audit current practices against open results principles
- Identify top 3 priorities for improvement
- Create SMART goals for the next 6-12 months
- Identify resources and support needed
- Establish checkpoints for evaluation and adjustment
- Plan how to track progress and celebrate successes

Share your plan with colleagues or mentors and ask for accountability.

**Activity 5.5: Design an Open Science Training Program**
Create a brief training or workshop for your research community on open results:
- Who is your audience?
- What are the learning objectives?
- What topics will you cover? (Choose 3-5 from this module)
- What activities will you include?
- How will you assess learning?
- Create an outline or agenda for your training session

Consider actually delivering it to your lab, department, or research group.
:::

## References

[^1]: Baker, M. (2016). 1,500 scientists lift the lid on reproducibility. *Nature*, 533(7604), 452-454. https://doi.org/10.1038/533452a

## Additional Resources

In addition to the TOPS module training, the community resources below are excellent information sources about open science.
- Geoscience Paper of the Future from [https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/2015EA000136](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/2015EA000136)
- Symposium report, October 2015. Reproducibility and reliability of biomedical research: improving research practice \[[PDF](https://acmedsci.ac.uk/viewFile/56314e40aac61.pdf)\].
- TOPS Guidelines, [https://www.cos.io/initiatives/top-guidelines](https://www.cos.io/initiatives/top-guidelines)
- The [Budapest Open Access](http://www.budapestopenaccessinitiative.org/read) Agreement
- Open Science Framework, [https://osf.io/](https://osf.io/)
- "Researcher Degrees of Freedom" ([Wicherts et al., 2016](https://doi.org/10/gc5sjn)).
- Björk (2017). Growth of hybrid open access, 2009–2016. PeerJ 5:e3878 [doi.org/10.7717/peerj.3878](https://doi.org/10.7717/peerj.3878)
- Piwowar H, Priem J, Larivière V, Alperin JP, Matthias L, Norlander B, Farley A, West J, Haustein S. (2018) The state of OA: a large-scale analysis of the prevalence and impact of Open Access articles. PeerJ 6:e4375 [https://doi.org/10.7717/peerj.4375](https://doi.org/10.7717/peerj.4375)
