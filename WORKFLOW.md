# 7-Phase Music Therapy Literature Review Workflow

## Phase 1: Project Initialization

Create project structure:
```

project_root/
├── CLAUDE.md              # Writing guidelines & terminology
├── IMPLEMENTATION_PLAN.md # Staged plan
├── manuscript_draft.md    # Main manuscript
├── figures/               # Figure placeholders
└── supplementary/         # Additional materials
├── PRISMA_checklist.md
└── quality_assessment.md

```

**Actions:**
1. Create `CLAUDE.md` from template (see TEMPLATES.md)
   - Include music therapy terminology standards
   - Define hedging language requirements
   - Specify NIH Toolkit compliance requirements
2. Create `IMPLEMENTATION_PLAN.md` with stages
3. Initialize empty `manuscript_draft.md`
4. Prepare PRISMA checklist for systematic reviews

## Phase 2: Literature Collection

### Data Sources

#### 1. PubMed (Clinical & Biomedical Evidence)

**Best for:** RCTs, clinical validation, peer-reviewed medical literature

**Search Strategy:**
```

Query structure:
([Intervention terms]) AND ([Population terms]) AND ([Study design])

Example:
("Music Therapy"[Mesh] OR "music-based intervention"[tiab] OR
"rhythmic auditory stimulation"[tiab])
AND
("Parkinson Disease"[Mesh] OR "Stroke"[Mesh] OR "Dementia"[Mesh])
AND
("randomized controlled trial"[pt] OR "clinical trial"[pt])

```

**MeSH Terms for Music Therapy:**
| Category | MeSH Terms |
|----------|------------|
| Intervention | "Music Therapy"[Mesh], "Acoustic Stimulation"[Mesh] |
| Mechanism | "Auditory Perception"[Mesh], "Motor Activity"[Mesh] |
| Neurological | "Parkinson Disease"[Mesh], "Stroke"[Mesh], "Brain Injuries"[Mesh] |
| Cognitive | "Dementia"[Mesh], "Alzheimer Disease"[Mesh], "Cognition"[Mesh] |
| Psychiatric | "Depression"[Mesh], "Anxiety"[Mesh] |
| Outcomes | "Quality of Life"[Mesh], "Activities of Daily Living"[Mesh] |

**Workflow:**
1. Develop comprehensive search string using MeSH + free text
2. Apply filters: Publication type, Date range, Language
3. Export results to reference manager
4. Screen by title/abstract
5. Retrieve full text for included studies

#### 2. Cochrane Library (Systematic Reviews & Meta-analyses)

**Best for:** Evidence synthesis, existing systematic reviews, quality RCTs

**Key Collections:**
- Cochrane Database of Systematic Reviews (CDSR)
- Central Register of Controlled Trials (CENTRAL)

**Relevant Existing Reviews:**
| Topic | Cochrane ID | Status |
|-------|-------------|--------|
| Music therapy for dementia | CD003477 | Updated 2018 |
| Music for acquired brain injury | CD006787 | Updated 2017 |
| Music therapy for depression | CD004517 | Updated 2017 |
| Music for pain relief | CD006908 | Updated 2006 |

**Workflow:**
1. Search CDSR for existing reviews on topic
2. Extract conclusions and limitations from existing reviews
3. Search CENTRAL for RCTs not yet included in reviews
4. Identify gaps in current evidence synthesis

#### 3. PsycINFO (Psychology & Behavioral Science)

**Best for:** Psychological mechanisms, behavioral outcomes, therapy process

**Subject Headings:**
- Music Therapy
- Neurologic Music Therapy
- Auditory Stimulation
- Rhythm (Music)
- Emotional States
- Motor Processes

**Search Strategy:**
```

(DE "Music Therapy" OR DE "Neurologic Music Therapy")
AND
(DE "Rehabilitation" OR DE "Motor Processes" OR DE "Cognition")

````

#### 4. RILM Abstracts (Music-Specific Research)

**Best for:** Music perception, cognition, ethnomusicology, interdisciplinary music studies

**Coverage:**
- Music perception and cognition studies
- Ethnomusicological perspectives on healing music
- Music education research with therapeutic applications
- Historical perspectives on music and health

#### 5. ArXiv & bioRxiv (Preprints & Computational Methods)

**Best for:** Latest neuroscience research, computational methods, MIR techniques

**Configuration (ArXiv MCP):**
```json
{
  "mcpServers": {
    "arxiv": {
      "command": "uvx",
      "args": ["arxiv-mcp-server"],
      "env": {
        "ARXIV_STORAGE_PATH": "~/.arxiv-mcp-server/papers"
      }
    }
  }
}
````

**Relevant Categories:**

| Category                    | Code     | Focus                            |
| --------------------------- | -------- | -------------------------------- |
| Neurons and Cognition       | q-bio.NC | Neural mechanisms of music       |
| Sound                       | cs.SD    | Audio processing, MIR            |
| Human-Computer Interaction  | cs.HC    | Adaptive instruments, interfaces |
| Audio and Speech Processing | eess.AS  | Signal processing                |

**Example Queries:**

```
Search: "music therapy neural mechanism"
Search: "auditory-motor coupling rhythm"
Search: "music reward dopamine"
Search: "adaptive musical instrument rehabilitation"
Categories: q-bio.NC, cs.SD, cs.HC
Date: 2020-present
```

#### 6. ClinicalTrials.gov & ICTRP (Trial Registries)

**Best for:** Ongoing trials, unpublished results, protocol details

**Search Terms:**

* "music therapy"
* "music-based intervention"
* "rhythmic auditory stimulation"
* "melodic intonation therapy"

**Data to Extract:**

* Study design and protocol
* Primary/secondary outcomes
* Sample size and population
* Intervention details (dose, frequency, duration)
* Status (recruiting, completed, results posted)

#### 7. Zotero (Reference Management)

**Best for:** Managing collected references, existing collections, team collaboration

**Workflow:**

1. Connect to Zotero API or use Zotero-MCP
2. Create collection structure mirroring review sections
3. Tag papers by: intervention type, population, outcome, quality
4. Export metadata for citation management

### Collection Workflow

**Step-by-Step Actions:**

1. **Develop search protocol**

   * Define PICO(S) elements
   * Create search strings for each database
   * Document search date and strategy

2. **Database searches** (in order)

   ```
   a. PubMed/MEDLINE - Clinical evidence (target: 100-200 records)
   b. Cochrane CENTRAL - RCTs (target: 50-100 records)
   c. PsycINFO - Psychological mechanisms (target: 50-100 records)
   d. RILM - Music-specific studies (target: 30-50 records)
   e. ArXiv/bioRxiv - Latest methods (target: 20-50 records)
   f. ClinicalTrials.gov - Ongoing work (target: 10-30 records)
   ```

3. **Remove duplicates** using reference manager

4. **Title/Abstract screening**

   * Apply inclusion/exclusion criteria
   * Use dual screening for systematic reviews

5. **Full-text retrieval and screening**

6. **Data extraction** - Create literature matrix:

| Category     | Subcategory     | Key Papers | N | Source       | Evidence Level |
| ------------ | --------------- | ---------- | - | ------------ | -------------- |
| Intervention | RAS             | [refs]     | N | PubMed       | RCT            |
| Intervention | MIT             | [refs]     | N | PubMed       | RCT            |
| Intervention | Music Listening | [refs]     | N | Mixed        | Mixed          |
| Mechanism    | Auditory-Motor  | [refs]     | N | ArXiv/PubMed | Basic          |
| Mechanism    | Reward          | [refs]     | N | ArXiv/PubMed | Basic          |
| Population   | Parkinson's     | [refs]     | N | PubMed       | RCT            |
| Population   | Stroke          | [refs]     | N | PubMed       | RCT            |
| Population   | Dementia        | [refs]     | N | Cochrane     | SR             |
| Technology   | ADMI            | [refs]     | N | ArXiv        | Pilot          |
| Methodology  | NIH Toolkit     | [refs]     | N | PubMed       | Guideline      |

7. **Quality assessment**

   * RCTs: Cochrane Risk of Bias tool
   * Non-randomized: ROBINS-I
   * Observational: Newcastle-Ottawa Scale

8. **Gap analysis** - Identify missing:

   * Populations (age groups, conditions)
   * Intervention types
   * Outcome domains
   * Time periods
   * Geographic regions

9. **Targeted supplementary search** - Fill gaps

10. **PRISMA flow diagram** - Document selection process

## Phase 3: Outline Development

**Actions:**

1. **Define theoretical framework section**

   * Brain circuitry framework (auditory-motor, reward, cognitive pathways)
   * NIH conceptual models (SOBC, neuromechanistic, resilience)
   * Therapeutic affordances framework

2. **Organize intervention categories**

   ```
   Neurologic Music Therapy
   ├── Rhythmic Auditory Stimulation (RAS)
   ├── Melodic Intonation Therapy (MIT)
   └── Other NMT techniques

   Receptive Interventions
   ├── Music listening
   └── Guided imagery with music

   Active Interventions
   ├── Singing-based
   ├── Instrument playing
   └── Dance/movement to music

   Technology-Enhanced MBIs
   ├── Adaptive digital instruments
   ├── Music-based games
   └── AI/personalized systems
   ```

3. **Map papers to sections**

   * Create section-paper assignment table
   * Identify sections needing more evidence

4. **Plan comparison tables**

   * Table 1: Theoretical frameworks
   * Table 2: Intervention characteristics
   * Table 3: Clinical evidence by population
   * Table 4: Outcome measures
   * Table 5: Methodological quality

5. **Design figure placeholders**

   * Figure 1: PRISMA flow diagram
   * Figure 2: Neural pathways schematic
   * Figure 3: Intervention taxonomy
   * Figure 4: Evidence map by population/intervention

6. **NIH Toolkit alignment check**

   * Building blocks coverage
   * Outcome measure categorization
   * Biomarker discussion plan

**Output:** Detailed outline in IMPLEMENTATION_PLAN.md

## Phase 4: Section Writing

For each major section, follow this protocol:

### 4.1 Theoretical Framework Sections

1. **Introduce the framework** (1-2 paragraphs)

   * Historical development
   * Key proponents and seminal works

2. **Explain core mechanisms**

   * Neural pathways involved
   * Behavioral/psychological processes
   * Use diagrams where helpful

3. **Link to clinical applications**

   * Which conditions does this framework explain?
   * What predictions does it make?

4. **Discuss evidence base**

   * Supporting studies (neuroimaging, TMS, behavioral)
   * Animal model evidence where applicable

5. **Note limitations and gaps**

### 4.2 Intervention Sections

1. **Write introduction** (1-2 paragraphs)

   * Definition and distinction from related interventions
   * Theoretical rationale
   * Clinical need addressed

2. **Describe protocol elements** (NIH Building Blocks)

   ```markdown
   **Intervention Characteristics:**
   - Musical elements: [melody, rhythm, harmony, timbre]
   - Mode: [active/receptive]
   - Delivery: [live/recorded, individual/group, in-person/remote]
   - Provider: [music therapist/other healthcare provider]
   - Dosage: [session duration, frequency, total sessions]
   - Personalization: [standardized/individualized]
   ```

3. **Summarize evidence** using template:

   ```markdown
   **[Study Author, Year]:** [Design] study with N=[sample size] 
   [population] receiving [intervention details] for [duration].
   - Primary outcome: [measure] showed [effect] (effect size, p-value)
   - Secondary outcomes: [summary]
   - Quality: [risk of bias assessment]
   ```

4. **Create comparison table** for section

5. **Write limitations paragraph**

   * Methodological issues across studies
   * Gaps in evidence
   * Generalizability concerns

6. **Discuss clinical translation**

   * Current implementation status
   * Barriers to adoption
   * Resources required

7. **Update references**

### 4.3 Population/Clinical Application Sections

1. **Clinical background** (1 paragraph)

   * Disease/condition overview
   * Symptoms addressable by music

2. **Rationale for music intervention**

   * Neural systems involved
   * Therapeutic affordances relevant

3. **Evidence synthesis by intervention type**

   * Organize by intervention category
   * Report effect sizes consistently

4. **Evidence quality summary**

   * Overall strength of evidence
   * Confidence in conclusions

5. **Clinical recommendations** (with appropriate hedging)

6. **Research priorities**

**Progress tracking:** Use TodoWrite for each section:

```markdown
## Section Progress
- [ ] 3.1 RAS - Draft complete
- [ ] 3.2 MIT - In progress
- [ ] 3.3 Music Listening - Not started
```

## Phase 5: Tables and Figures

### Required Tables

**Table 1: Theoretical Frameworks**

| Framework               | Core Principle           | Key Neural Systems      | Application            | Key References     |
| ----------------------- | ------------------------ | ----------------------- | ---------------------- | ------------------ |
| Auditory-Motor Coupling | Rhythm entrains movement | Basal ganglia, SMA, PMC | Gait disorders         | Zatorre, Thaut     |
| Reward Circuitry        | Music activates reward   | NAcc, VTA, VMPFC        | Motivation, mood       | Salimpoor, Koelsch |
| SOBC                    | Mechanism verification   | Variable                | All MBIs               | NIH SOBC           |
| Resilience              | Coping support           | Stress systems          | Aging, chronic illness | Robb               |

**Table 2: Intervention Characteristics Comparison**

| Intervention    | Mode      | Delivery      | Provider | Typical Dose      | Primary Target |
| --------------- | --------- | ------------- | -------- | ----------------- | -------------- |
| RAS             | Active    | Live/recorded | MT/PT    | 30min, 3x/wk, 6wk | Gait           |
| MIT             | Active    | Live          | SLP/MT   | 45min, 5x/wk, 6wk | Speech         |
| Music Listening | Receptive | Recorded      | Any      | Variable          | Mood, pain     |

**Table 3: Clinical Evidence Summary**

| Condition        | Intervention  | N (studies) | N (participants) | Effect Size | Evidence Quality |
| ---------------- | ------------- | ----------- | ---------------- | ----------- | ---------------- |
| PD - Gait        | RAS           | X           | X                | SMD = X.XX  | ⬛⬛⬛◻             |
| Stroke - Aphasia | MIT           | X           | X                | SMD = X.XX  | ⬛⬛⬛◻             |
| Dementia - BPSD  | Music therapy | X           | X                | SMD = X.XX  | ⬛⬛◻◻             |

**Table 4: Outcome Measures by Domain**

| Domain    | Measure | Type        | Validated For | Psychometrics    |
| --------- | ------- | ----------- | ------------- | ---------------- |
| Motor     | 10MWT   | Performance | PD, Stroke    | Good reliability |
| Cognitive | MMSE    | Performance | Dementia      | Well-established |
| Mood      | GDS     | Self-report | Older adults  | Good validity    |
| QoL       | SF-36   | Self-report | General       | Excellent        |

**Table 5: Methodological Quality Summary** (for systematic reviews)

| Study          | Randomization | Blinding | Control | Fidelity | Attrition | Overall       |
| -------------- | ------------- | -------- | ------- | -------- | --------- | ------------- |
| [Author, Year] | ✓/? /✗        | ✓/? /✗   | ✓/? /✗  | ✓/? /✗   | ✓/? /✗    | Low/Some/High |

**Table 6: Technology-Enhanced MBI Tools** (if applicable)

| Tool/System | Type | Target Population | Evidence | Accessibility |
| ----------- | ---- | ----------------- | -------- | ------------- |
| EyeHarp     | ADMI | Motor impairment  | Pilot    | Open source   |

### Required Figures

**Figure 1: PRISMA Flow Diagram**

```
Records identified (N=XXX)
├── PubMed (n=XXX)
├── Cochrane (n=XXX)
├── PsycINFO (n=XXX)
└── Other (n=XXX)
    ↓
Duplicates removed (n=XXX)
    ↓
Records screened (n=XXX)
├── Excluded (n=XXX)
    ↓
Full-text assessed (n=XXX)
├── Excluded with reasons (n=XXX)
    ↓
Studies included (n=XXX)
├── RCTs (n=XXX)
├── Quasi-experimental (n=XXX)
└── Observational (n=XXX)
```

**Figure 2: Neural Pathways Underlying MBI Effects**

```
[Placeholder: Schematic showing]
- Auditory cortex connections to:
  - Motor system (dorsal stream → PMC → BG)
  - Reward system (NAcc, VTA)
  - Cognitive systems (PFC, hippocampus)
  - Affective systems (amygdala, insula)
```

**Figure 3: MBI Intervention Taxonomy**

```
[Placeholder: Hierarchical diagram showing]
Music-Based Interventions
├── Music Therapy (credentialed)
│   ├── Neurologic Music Therapy
│   ├── Psychodynamic
│   └── Humanistic
└── Music Medicine (non-credentialed)
    ├── Active
    └── Receptive
```

**Figure 4: Evidence Map**

```
[Placeholder: Matrix/heatmap showing]
- Y-axis: Conditions (PD, Stroke, Dementia, Depression...)
- X-axis: Interventions (RAS, MIT, Listening, Singing...)
- Cell color: Evidence strength
- Cell size: Number of studies
```

**Figure 5: NIH MBI Toolkit Building Blocks**

```
[Placeholder: Diagram adapted from NIH Toolkit]
- Intervention components
- Protocol delivery elements
- Population considerations
- Control condition types
```

## Phase 6: Quality Assurance

### Structure Check

* [ ] Key Points present (3-5 bullets after abstract)
* [ ] All sections have summary tables
* [ ] Consistent heading hierarchy (H2 for main, H3 for sub)
* [ ] PRISMA diagram included (for systematic reviews)
* [ ] Figures numbered sequentially with captions

### Content Check

* [ ] Clear distinction between music therapy and music medicine
* [ ] Theoretical framework(s) explained adequately
* [ ] All major intervention categories covered
* [ ] Evidence organized by population and/or intervention
* [ ] Neural mechanisms discussed with appropriate hedging
* [ ] Limitations for each intervention type
* [ ] Future directions articulated
* [ ] Clinical implications stated (with caution)

### NIH Toolkit Compliance Check

* [ ] Building blocks framework referenced
* [ ] Interventions described with required elements:

  * [ ] Musical elements specified
  * [ ] Delivery mode specified
  * [ ] Dosage parameters reported
  * [ ] Provider qualifications noted
* [ ] Control conditions evaluated and discussed
* [ ] Outcome measures categorized (clinical/mechanistic)
* [ ] Biomarkers discussed where applicable
* [ ] Treatment fidelity addressed

### Evidence Quality Check

* [ ] Effect sizes reported consistently (Cohen's d, SMD, etc.)
* [ ] Confidence intervals included where available
* [ ] Sample sizes reported
* [ ] Evidence quality indicators used (⬛⬛⬛◻ system)
* [ ] Risk of bias assessed for included studies
* [ ] Heterogeneity addressed
* [ ] Publication bias considered

### Language Check

* [ ] Hedging language used ("may", "suggests", "appears to")
* [ ] No absolute claims ("X is the best intervention")
* [ ] Consistent terminology (see SKILL.md terminology table)
* [ ] Music therapy vs music medicine distinguished
* [ ] Smooth transitions between sections
* [ ] Technical terms defined on first use

### Reference Check

* [ ] 80-120 references total
* [ ] Recent literature included (last 5 years emphasized)
* [ ] Seminal/foundational works cited
* [ ] NIH Toolkit and Sound Health documents cited
* [ ] Cochrane reviews cited where applicable
* [ ] References organized by topic in text
* [ ] All citations have corresponding reference entries

### Supplementary Materials Check

* [ ] Search strategies documented
* [ ] Full inclusion/exclusion criteria provided
* [ ] Quality assessment details available
* [ ] Data extraction forms described

## Phase 7: Incremental Updates

When new literature becomes available:

### Monitoring Strategy

1. **Set up alerts**

   * PubMed: My NCBI saved searches with email alerts
   * Google Scholar: Citation alerts for key papers
   * ClinicalTrials.gov: New trials in area

2. **Quarterly review cycle**

   * Check for new systematic reviews
   * Check for new large RCTs
   * Check for new NIH guidance documents

### Update Protocol

1. **Categorize** new papers

   * New intervention type?
   * New population?
   * New mechanism evidence?
   * Replication/extension of existing evidence?

2. **Assess impact**

   * Does this change conclusions?
   * Does this fill a gap?
   * Does this require new section?

3. **Update CLAUDE.md**

   * New terminology if needed
   * New key references

4. **Update IMPLEMENTATION_PLAN.md**

   * Add new stage for updates
   * Document update rationale

5. **Identify insertion points** in manuscript

   * Which section(s) affected?
   * Does table need updating?

6. **Update sections** with new evidence

   * Maintain consistent format
   * Update effect size summaries
   * Revise conclusions if warranted

7. **Add new sections** if new paradigm emerges

   * New intervention category
   * New population application
   * New mechanism discovery

8. **Update tables** with new data

   * Add rows for new studies
   * Update evidence quality ratings
   * Recalculate pooled effects if applicable

9. **Update figures**

   * Revise PRISMA numbers
   * Update evidence map

10. **Expand references**

    * Add new citations
    * Ensure no duplicates

### Version Control

```markdown
## Change Log

### [Date] - v1.2
- **New evidence:** Added 3 RCTs on RAS for PD gait (Section 4.1.1)
- **Updated tables:** Table 3 now includes studies through [date]
- **Revised conclusions:** Evidence for RAS upgraded to "strong" based on new meta-analysis
- **New references:** Added citations #95-#102

### [Date] - v1.1
- **New section:** Added Section 4.4.3 on AI-personalized music systems
- **Updated Table 2:** Added characteristics of digital interventions
- **Gap filled:** Now includes pediatric population evidence (Section 5.X)
- **References:** Added #85-#94
```

### Living Review Considerations

For living systematic reviews:

1. **Pre-specify update triggers**

   * New RCT with N > X published
   * New systematic review published
   * Major guideline update

2. **Document search updates**

   * Date range for each update
   * Any modifications to search strategy

3. **Track cumulative evidence**

   * Update meta-analyses if applicable
   * Note direction of evidence over time

4. **Transparency**

   * Clearly mark updated sections
   * Provide date stamps
   * Archive previous versions

---

## Quick Reference: Phase Checklist

```markdown
□ Phase 1: Project Initialization
  □ CLAUDE.md created
  □ IMPLEMENTATION_PLAN.md created
  □ manuscript_draft.md initialized
  □ PRISMA checklist prepared

□ Phase 2: Literature Collection
  □ Search protocol documented
  □ All databases searched
  □ Duplicates removed
  □ Screening completed
  □ Literature matrix created
  □ Quality assessment done
  □ PRISMA diagram drafted

□ Phase 3: Outline Development
  □ Theoretical framework planned
  □ Intervention categories defined
  □ Papers mapped to sections
  □ Tables planned
  □ Figures planned

□ Phase 4: Section Writing
  □ All framework sections written
  □ All intervention sections written
  □ All population sections written
  □ Limitations included
  □ References updated

□ Phase 5: Tables and Figures
  □ All tables created
  □ All figures created/placeholder
  □ Captions written

□ Phase 6: Quality Assurance
  □ Structure check passed
  □ Content check passed
  □ NIH Toolkit compliance verified
  □ Evidence quality check passed
  □ Language check passed
  □ Reference check passed

□ Phase 7: Ready for Updates
  □ Monitoring alerts set
  □ Update protocol documented
  □ Version control in place
```

