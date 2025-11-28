# Writing Style Guide - DevInfra IC Calibration Notes

**Template**: DevInfra - IC Calibration Notes Template
**Target Audience**: AI Agents (Shakespeare)

---

## ⚠️ CRITICAL: Confidentiality Header

**MANDATORY**: All documents MUST include the 'Confidential' header.

---

## Overarching Style and Tone

### Primary Tone
**Professional, Direct, and Action-Oriented**

### Key Elements

1. **Start with Strong Recognition**
   - Begin the rationale with a strong recognition of the individual's performance and achievements
   - Lead with accomplishments, not gaps

2. **Frame Improvement as Growth**
   - Frame feedback on improvement areas as opportunities to 'increase impact' or 'grow'
   - Avoid deficit language; use forward-looking framing

3. **Forward-Looking Orientation**
   - Be forward-looking, mentioning expectations for the next review cycle (e.g., H2)
   - Link current performance to future goals

### Required Language: Strong Action Verbs

**MUST USE** these action verbs throughout:
- **Landed** (for shipping/delivery)
- **Root caused** (for debugging/analysis)
- **Led** (for leadership)
- **Owned** (for ownership)
- **Enabled** (for unblocking/empowering)
- **Spearheaded** (for initiative-taking)
- **Drove** (for driving outcomes)
- **Authored** (for documentation/design)

---

## Metadata Requirements

### Employee Data (MANDATORY)
Must include:
- Name
- Title
- Location
- Year

**Format**: `[Name] [Title] @ [Location] [Year]`

**Example**: Brian Kelley Software Engineer @ Bellevue, USA 2025

### Reviewer Data (MANDATORY)
Must include:
- Manager Name
- Title
- Submission Date

**Format**: `[Manager Name] • [Title] Submitted [Date]`

**Example**: Mauricio Nunes • Software Engineering Manager Submitted 2025-08-11

---

## Evidence and Detail Requirements

### 1. Quantification (MANDATORY)

Impact MUST be expressed using **specific metrics and quantifiable results**:

**Required Metrics**:
- WAU (Weekly Active Users)
- MAU (Monthly Active Users)
- TSD reduction (Time to Successful Development)
- Percentage improvements
- Speed increases
- User counts
- SEV (Site Event) numbers
- Error rate reductions
- Freeze reductions

**Examples**:
- ✅ "Reduced Latency by 15%"
- ✅ "Increased WAU from 10K to 15K"
- ✅ "Improved build speed by 40%"
- ✅ "Reduced OOM errors by 60%"
- ❌ "Improved performance" (too vague)
- ❌ "Made things better" (no metrics)

### 2. Citation Use (MANDATORY)

**Use numbered citations** `[i]` or `[i, j]` to reference:
- Specific evidence
- Support tickets
- Related incidents
- Production Incidents

**Format**: `[i]` where i is citation number

**Examples**:
- "Resolved critical Production Incident [1] affecting 50K users"
- "Delivered DSS-4 compliance [4]"

### 3. Peer Feedback Integration (MANDATORY)

**Integrate direct quotes** from:
- Peers
- Partners
- Managers

**Must cite the source**: Name/Title/Level

**Format**:
```
"[Quote]" - [Name], [Title], [Level]
```

**Example**:
```
"Brian's technical deep dive saved us weeks of debugging" - Sarah Chen, Staff Engineer, E6
```

---

## Formatting Rules

### 1. Bold Text Usage (MANDATORY)

**MUST BOLD**:
- Names of major initiatives
- Key results
- Employee names
- Manager names
- Critical statements (e.g., strength summary, overall rating justification)

**Examples**:
- "**Brian** led the **VS Code Extension Migration**"
- "**Sarah Chen** (Staff Engineer, E6)"
- "This demonstrates **strong direction setting**"

### 2. List Structure (MANDATORY)

**Primary items**: Use standard markdown bullet points (`*`)
**Sub-bullets**: Use nested sub-bullets (`°`) for:
- Specific deliverables
- Metrics
- Dependencies

**Example**:
```
* Landed VS Code Extension Migration (+)
  ° Reduced bundle size by 60%
  ° Improved load time from 3s to 800ms
  ° Coordinated with 5 partner teams
```

### 3. Rating Notation - Axes (MANDATORY)

**Summary rating for each axis** must be contained in **brackets** `[Rating]`

**Valid Template Ratings**:
- `[BE]` - Below Expectations
- `[ME]` - Meets Expectations
- `[EE]` - Exceeds Expectations
- `[GE]` - Greatly Exceeds


**Example**:
```
Project Work [EE]
Technical Debt [ME]
Leadership [GE]
Others [BE]
```

### 4. Rating Notation - Individual Bullets (MANDATORY)

**Individual accomplishments** within axis sections must use:
- `(=)` - Meeting baseline expectations
- `(++)` - Significantly positive contribution
- `(+)` - Surpassing expectations
- `(-)` - Missing expectations


**Example**:
```
* Landed VS Code Extension GA (+)
* Root caused 3 critical SEVs (=)
* Authored design doc for LSP migration (++)
```

---

## Acronym and Glossary Management

### Acronym Usage

**Use internal acronyms freely** within impact sections:
- SLAs (Service Level Agreements)
- WAU (Weekly Active Users)
- MAU (Monthly Active Users)
- OOM (Out Of Memory)
- LSP (Language Server Protocol)
- CPE (Client Platform Engineering)
- DSS-4 (Data Security Standard 4)
- XFN (Cross-Functional)

### Glossary Requirement (MANDATORY)

**A mandatory Glossary section** must be included in the Rationale to define:
- Key terminology
- Complex terms
- Internal terminology for reviewers without prior context

**Terms requiring glossary entries** (examples):
- DSS-4
- CPE
- AS-243
- LSP
- Any team-specific acronyms

**Format**:
```
## Glossary
* **DSS-4**: Data Security Standard 4 compliance requirements
* **CPE**: Client Platform Engineering team
```

---

## Section Details

### Section 1: Rationale for the Recommended Performance Rating

**Template Field**: "Rationale for the performance rating [IC Name] received."

**Word Limit**: 100 words (recommendation)

**Required Sub-Sections**:

#### 1.1 Overall Rationale/Justification
**Style**: A concise summary covering the 'why' of the rating
- Must address key goals delivered
- Overall performance signal
- Often presented in 1-2 bullet points

**Example**:
```
* **Brian** consistently exceeded expectations across all axes, landing major initiatives like **VS Code Extension GA** and **LSP Migration** while maintaining exceptional engineering excellence through SEV mitigation and technical deep dives.
* His strategic direction setting and XFN alignment enabled 3 partner teams to accelerate their roadmaps.
```

#### 1.2 Glossary
**Style**: Define/Expand on internal terminology
- List all acronyms and internal terms used throughout packet

**Example**:
```
## Glossary
er* **DSS-4**: Data Security Standard 4 compliance requirements
* **CPE**: Client Platform Engineering
* **AS-243**: Security Assessment 243
```

#### 1.3 Business-Context
**Style**: One or two sentences summarizing team/org business context
- Focus on core strategies

**Example**:
```
The DevInfra team focuses on **VS Code first strategy**, improving **DevX (Developer Experience)**, reducing **TSD**, and enabling **AI-driven development** across the organization.
```

#### 1.4 Relationship-context
**Style**: A few sentences describing the individual's role differentiation in multi-person projects

**Key Elements**:
- TL (Tech Lead) role
- Main contributor role
- Delegation
- Partnership roles

**Example**:
```
**Brian** served as **TL** for the VS Code Extension Migration, coordinating with 5 partner teams. On the LSP project, he was the **main contributor** for the parser implementation while **delegating** UI work to junior engineers. He **partnered** with FAIR and Security teams on AI model integration.
```

#### 1.5 Thesis
**Style**: Concise reasoning for the rating
- Summarize the packet's main findings
- Link performance to core outcomes

**Example**:
```
**Brian's** [EE] rating reflects his **strong execution across all axes**, delivering critical infrastructure improvements (VS Code Extension, LSP Migration) that reduced TSD by 15%, combined with **strategic direction setting** through technical deep dives and XFN alignment, and **growing people impact** through mentorship of 2 junior engineers.
```

#### 1.6 Why not Lower/Higher rating?
**Style**: One sentence summarizing why the rating was not different
- Must reference contextual factors

**Example**:
```
**Why not [GE]**: While Brian's technical execution is exceptional, [GE] at E5 requires broader org-level impact and more extensive people development; Brian is on track for this next half.
```

**Context factors to mention**:
- Scope constraints
- Onboarding time
- Leave duration
- Team size
- Project complexity

#### 1.7 Special circumstances (MANDATORY if applicable)
**Style**: Mandatory inclusion of factors affecting performance

**Must specify**:
- Onboarding time
- Periods of leave
- Duration

**Examples**:
```
* Brian joined the team late December 2024, so this was his onboarding half.
* Considering his 50-day leave during H1.
* Ramped up for 6 weeks at start of cycle.
```

---

### Section 2: Highlight IC's Impact Relative to Goals and Expectations

**Template Field**: "Project-Impact [Rating], Engineering-Excellence [Rating], Direction [Rating], People [Rating]"

**Word Limit**: 400 words (Total for all four axes)

**Format**: Each axis uses **bulleted list** with `(=)`, `(+)`, `(-)` notation

---

#### Axis 1: Project Work [Rating]

**Focus**:
- Core goals delivery
- Quantified business impact (TSD, MAU, WAU)
- Achievement of key milestones (GA, open-beta, rollout)

**Required Format**: Bulleted list using `(=)`, `(+)`, `(-)` notation

**Example**:
```
## Project Work [EE]

* **Landed VS Code Extension GA** [+]
  ° Migrated 15 core extensions to new architecture
  ° Reduced bundle size by 60% (10MB → 4MB)
  ° Increased WAU from 50K to 75K
  ° Coordinated with 5 partner teams across 3 orgs

* **Delivered LSP Migration to open-beta** (=)
  ° Implemented parser and semantic analysis
  ° Achieved 40% speed improvement in code completion
  ° Onboarded 2K beta users
  ° Partnered with Language Platform team

* **Owned new metric rollout to Infra** [+]
  ° Reduced build times by 35%
  ° Enabled 200+ developers
  ° Root caused and fixed 5 critical build failures

* **Owned new metric rollout to Infra** [+]
  ° Reduced build times by 35%
  ° Enabled 200+ developers
  ° Root caused and fixed 5 critical build failures

```

---

#### Axis 2: Technical Debt [Rating]

**Focus**:
- Code health contributions
- Production stability (SEVs mitigation, root cause analysis)
- Telemetry/analysis pipelines
- CI improvements
- Documentation
- Efficiency initiatives (reducing freezes/errors)

**Required Format**: Bulleted list using `(=)`, `(+)`, `(-)` notation

**Example**:
```
## Tech Debt [CME]

* **Root caused 3 critical incidents** [1, 2, 3] (+)
  ° I512020: OOM errors affecting 10K users
  ° I513405: Build freeze impacting CI pipeline
  ° I514890: Extension crash on macOS
  ° Implemented fixes reducing error rates by 80%

* **Authored LSP design doc** (=)
  ° 40-page technical specification
  ° Became template for team design docs
  ° Reviewed by 8 senior engineers

* **Improved telemetry pipeline** (+)
  ° Added 50+ new metrics for performance tracking
  ° Reduced WAU measurement latency by 60%
  ° Enabled real-time dashboards for leadership

* **Reduced extension OOM errors by 70%** (++)
  ° Memory profiling and optimization
  ° Implemented lazy loading patterns
  ° Prevented estimated 5K user complaints
```

---

#### Axis 3: Leadership [Rating]

**Focus**:
- Strategic ownership
- Defining strategy/roadmaps
- XFN alignment
- Complex problem resolution
- Technical deep dives
- H2 planning
- Technical analysis

**MUST explicitly name partners/cohorts**:
- FAIR
- Security
- CPE
- PMs
- Product teams
- Infrastructure teams

**Required Format**: Bulleted list using `(=)`, `(+)`, `(-)` notation

**Example**:
```
## Leadership [GE]

* **Drove macOS Memory Management strategy** (++)
  ° Authored 30-page technical analysis
  ° Identified 3 critical optimization opportunities
  ° Partnered with **CPE** and **Security** teams
  ° Presented findings to VP of Engineering
  ° Shaped H2 roadmap priorities

* **Led H2 planning for Infrastructure** (+)
  ° Defined strategy for AI-driven development
  ° Aligned with **Product** team on model integration
  ° Coordinated with 4 **PM**s across Product org
  ° Created quarterly OKRs adopted by team

* **Owned DSS-4 compliance technical strategy** (=)
  ° Partnered with **Security** team
  ° Designed architecture meeting compliance requirements
  ° Unblocked 3 teams waiting on compliance certification

* **Spearheaded VS Code first strategy adoption** (+)
  ° Created technical roadmap
  ° XFN alignment with 6 partner teams
  ° Enabled migration of 50+ internal tools

* **Led AI Adoption on Infrastructure (-)
  ° Responsible for defining the AI tools the org would adopt.
  ° Had problems on making timely critical decisions, leading the team to lose the opportunity to adopt the AI tools.

```

---

#### Axis 4: People [Rating]

**Focus**:
- Mentorship (naming individuals and focus areas)
- Onboarding new hires/interns
- XFN support
- Recruiting efforts (interviews)
- Team leadership/process improvement

**Must include**:
- Names of mentees
- Focus areas of mentorship
- Interview counts
- Process improvements (e.g., promo packet writing, tech talks, offsites, working groups)

**Required Format**: Bulleted list using `(=)`, `(+)`, `(-)` notation

**Example**:
```
## Others [EE]

* **Mentored 2 junior engineers** (+)
  ° **Alex Torres** (E3): Focused on code review skills and architecture patterns
  ° **Jordan Lee** (E4): Developed system design capabilities
  ° Both shipped first major features with Brian's guidance
  ° "Brian's mentorship accelerated my growth significantly" - Alex Torres, E3

* **Onboarded 3 new hires and 1 intern** (=)
  ° Created onboarding documentation
  ° Reduced ramp-up time from 8 weeks to 4 weeks
  ° All successfully shipped within first month

* **Conducted 15 technical interviews** (+)
  ° Contributed to hiring 4 engineers
  ° Improved interview rubric based on feedback
  ° Trained 2 interviewers on technical assessment

* **Led Infra tech talks series** (++)
  ° Delivered 3 talks on LSP architecture
  ° Attended by 100+ engineers
  ° Created reusable presentation materials

* **Authored promo packet writing guide** (=)
  ° Helped 3 teammates prepare packets
  ° Reduced packet revision cycles by 50%

* **Led H2 offsite planning** (+)
  ° Organized team roadmap session
  ° Facilitated technical deep dive workshops
  ° Improved team alignment scores by 40%

* **Team planning (-)
  ° Responsible for organizing team planning sessions, but failed on preparing the session, causing delays in team alignment.

```

---

### Section 3: Strengths

**Template Field**: "Share 1-3 strengths IC demonstrated."

**Word Limit**: 40 words

**Content Style**: List 1-3 core strengths demonstrated

**Must align with Career Expectations Explorer themes**:
- Strong Direction
- Technical Expertise/Problem-Solving
- Collaboration
- Self-direction
- Delegation
- Doing the Right Thing

**Example**:
```
## Strengths

* **Strong Direction**: Drove macOS memory strategy and H2 planning with clear technical vision
* **Technical Expertise**: Root caused complex SEVs with deep system knowledge
* **Collaboration**: Effective XFN partnership with FAIR, Security, and CPE teams
```

---

### Section 4: Growth Areas

**Template Field**: "Share 1-3 areas IC can develop or improve."

**Word Limit**: 60 words

**Content Style**: List 1-3 actionable areas for development

**Common themes**:
- Scope expansion/Taking Risk
- People impact/Mentorship
- Developing a Business-Oriented Mindset
- Delegation
- Faster Pivoting

**Example**:
```
## Growth Areas

* **Scope expansion**: To grow to E6, increase impact to 3+ teams and org-level initiatives
* **People impact**: Expand mentorship from 2 to 4-5 engineers and develop senior-level delegation skills
* **Business-oriented mindset**: Develop stronger connection between technical decisions and revenue/growth metrics
```

---

## Performance Review Archetype

### Purpose
The document must function as a **comprehensive Technical and Leadership Case Study**, not a mere summary of tasks.

### Delivery Goal
Provide a **justified argument for the rating** based on:
- Verifiable, quantitative impacts
- Demonstrated strategic direction
- Technical depth
- Growth in people leadership

### Analogy for Understanding
The document must balance **'code machine' contributions** (deep technical skill) with **scaling through leadership and delegation**, ensuring every section serves as evidence supporting the final rating signal.

**Think of it as**: An architect presenting detailed blueprints and material specifications to justify the integrity and quality of a complex structure.

---

## How Shakespeare Should Use This Guide

Shakespeare MUST:

1. ✅ **Match this tone throughout the review** - Professional, Direct, Action-Oriented
2. ✅ **Use ONLY the specified action verbs** - Landed, Root caused, Led, Owned, Enabled, Spearheaded, Drove, Authored
3. ✅ **Include ALL mandatory metadata** - Employee data, Reviewer data, Confidential header
4. ✅ **Use EXACT formatting rules** - Bold text, bullet notation `(=)`, `(+)`, `(-)`, rating brackets `[Rating]`
5. ✅ **Include numbered citations** - `[i]` for evidence/SEVs
6. ✅ **Integrate peer feedback with attribution** - "Quote" - Name, Title, Level
7. ✅ **Include mandatory Glossary section** - Define all acronyms and internal terms
8. ✅ **Use specific metrics** - WAU, MAU, TSD, percentages, user counts
9. ✅ **Include all required sub-sections** - Rationale, Glossary, Business-Context, Relationship-context, Thesis, Why not lower/higher, Special circumstances
10. ✅ **Apply section-specific formatting** - Bullets with sub-bullets (`°`)
11. ✅ **Name XFN partners explicitly** - FAIR, Security, CPE, PM teams
12. ✅ **Name mentees and interview counts** - In People axis
13. ✅ **Stay within word limits** - 100 words (Rationale), 400 words (Axes), 40 words (Strengths), 60 words (Growth)
14. ✅ **Frame improvement as growth opportunities** - Not deficits
15. ✅ **Be forward-looking** - Link to H2 expectations and future goals

---

## Summary Checklist for Shakespeare

Before presenting ANY draft section, verify:

- [ ] Confidential header included
- [ ] Employee metadata present (Name, Title, Location, Year)
- [ ] Reviewer metadata present (Manager, Title, Date)
- [ ] Action verbs used (Landed, Root caused, Led, Owned, Enabled, Spearheaded, Drove, Authored)
- [ ] Metrics quantified (WAU, MAU, TSD, percentages)
- [ ] Citations included `[i]`
- [ ] Peer feedback with attribution
- [ ] Bold text for initiatives, names, key statements
- [ ] Bullet notation: `(=)`, `(+)`, `(-)` for items
- [ ] Rating brackets: `[Rating]` for axes
- [ ] Glossary section included with all acronyms
- [ ] XFN partners named (FAIR, Security, CPE, PMs)
- [ ] Mentees named in People axis
- [ ] All required sub-sections present
- [ ] Word limits respected
- [ ] Forward-looking language used

---

**This guide is LAW. Follow it exactly.**
