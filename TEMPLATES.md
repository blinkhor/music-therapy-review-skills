# Project File Templates for Music Therapy Literature Reviews

## CLAUDE.md Template

```markdown
# [Topic] Music-Based Intervention Literature Review Writing Guidelines

## Terminology Standardization

| Preferred Term | Avoid Using | Reason |
|----------------|-------------|--------|
| Music-based intervention (MBI) | Music treatment, music cure | NIH standardized terminology |
| Music therapy | Music healing, therapeutic music | Requires credentialed practitioner |
| Music medicine | Background music therapy | Distinct from credentialed practice |
| Rhythmic auditory stimulation (RAS) | Beat therapy, rhythm therapy | Established NMT protocol name |
| Melodic intonation therapy (MIT) | Singing therapy | Established protocol name |
| Neurologic music therapy (NMT) | Neuromusic therapy | Professional certification term |
| Therapeutic affordances | Music benefits, music effects | Theoretical framework term |
| Auditory-motor coupling | Sound-movement connection | Neuroscience precision |
| Entrainment | Synchronization | Technical term for rhythmic coupling |
| Effect size (Cohen's d, SMD) | Improvement, benefit | Quantitative precision |
| Music therapist (MT-BC) | Music healer | Credential-specific |

## Key Distinctions

### Music Therapy vs Music Medicine
| Dimension | Music Therapy | Music Medicine |
|-----------|---------------|----------------|
| Provider | Credentialed music therapist | Other healthcare providers |
| Relationship | Therapeutic relationship required | Not required |
| Approach | Individualized, process-oriented | Standardized, outcome-oriented |
| Examples | Nordoff-Robbins, NMT, GIM | Recorded music listening protocols |

## Reference Sources

### PubMed MCP (Clinical Literature - Primary)
````

MeSH queries:

* "Music Therapy"[Mesh] AND "[condition]"[Mesh]
* "Acoustic Stimulation"[Mesh] AND "Rehabilitation"[Mesh]
* "Auditory Perception"[Mesh] AND "[condition]"[Mesh]

Free text additions:

* "rhythmic auditory stimulation"[tiab]
* "melodic intonation therapy"[tiab]
* "music-based intervention"[tiab]

Filters:

* Publication types: Randomized Controlled Trial, Meta-Analysis, Systematic Review
* Date: Last 10 years (with seminal works exception)

```

### Cochrane Library (Systematic Reviews)
```

Search terms:

* "music therapy"
* "music intervention"

Key existing reviews to cite:

* CD003477 (Dementia)
* CD006787 (Acquired brain injury)
* CD004517 (Depression)

```

### PsycINFO (Psychological Mechanisms)
```

Subject headings:

* Music Therapy
* Neurologic Music Therapy
* Auditory Stimulation
* Rhythm

Filters: Peer-reviewed, Empirical study

```

### ArXiv/bioRxiv (Neuroscience & Technology)
```

Search queries:

* "music therapy neural mechanism" (q-bio.NC)
* "auditory-motor coupling" (q-bio.NC)
* "adaptive musical instrument" (cs.HC)
* "music information retrieval health" (cs.SD)

Categories: q-bio.NC, cs.SD, cs.HC, eess.AS
Date range: 2020-present
Downloaded papers: [list paper IDs]

```

### Trial Registries
```

ClinicalTrials.gov:

* "music therapy" [Intervention]
* "music-based intervention" [Intervention]

WHO ICTRP:

* Combined search across international registries

```

### Zotero Database
```

API: [http://localhost:23119/api/users/[USER_ID]/](http://localhost:23119/api/users/[USER_ID]/)
Collections:

* Neurologic Music Therapy: collections/[KEY]/items
* Music and Parkinson's: collections/[KEY]/items
* Music and Dementia: collections/[KEY]/items
* Neural Mechanisms: collections/[KEY]/items

```

## Literature Categories

### By Intervention Type
1. **Neurologic Music Therapy (NMT)**: RAS, MIT, PSE, TIMP, [N papers]
2. **Receptive Interventions**: Music listening, GIM, [N papers]
3. **Active Interventions**: Singing, instrument playing, dance, [N papers]
4. **Technology-Enhanced MBIs**: ADMI, games, AI systems, [N papers]

### By Population
1. **Neurological**: Parkinson's, stroke, TBI, [N papers]
2. **Neurodegenerative**: Dementia, AD, [N papers]
3. **Psychiatric**: Depression, anxiety, PTSD, [N papers]
4. **Developmental**: ASD, ADHD, [N papers]
5. **Other**: Pain, palliative, pediatric, [N papers]

### By Mechanism
1. **Auditory-Motor**: Entrainment, gait, motor learning, [N papers]
2. **Auditory-Reward**: Dopamine, motivation, pleasure, [N papers]
3. **Auditory-Cognitive**: Attention, memory, executive function, [N papers]
4. **Auditory-Affective**: Emotion regulation, stress, [N papers]

## Key Interventions to Cover

| Category | Interventions | Status |
|----------|---------------|--------|
| NMT - Motor | RAS, PSE, TIMP | [ ] |
| NMT - Speech | MIT, MUSTIM, RVT | [ ] |
| NMT - Cognitive | MPC, APT, MACT | [ ] |
| Receptive | Music listening, GIM, song discussion | [ ] |
| Active | Therapeutic singing, drumming, dance | [ ] |
| Technology | ADMI, serious games, BCI | [ ] |

## Evidence Summary by Condition

| Condition | Intervention | N Studies | Effect Size Range | Evidence Level |
|-----------|--------------|-----------|-------------------|----------------|
| PD - Gait | RAS | X | d = 0.XX - 0.XX | ⬛⬛⬛◻ |
| Stroke - Gait | RAS | X | d = 0.XX - 0.XX | ⬛⬛⬛◻ |
| Stroke - Aphasia | MIT | X | d = 0.XX - 0.XX | ⬛⬛⬛◻ |
| Dementia - BPSD | Music therapy | X | d = 0.XX - 0.XX | ⬛⬛◻◻ |
| Depression | Music therapy | X | d = 0.XX - 0.XX | ⬛⬛◻◻ |

### Evidence Level Key
- ⬛⬛⬛⬛ = Level 1a (SR of RCTs)
- ⬛⬛⬛◻ = Level 1b (Individual RCT)
- ⬛⬛◻◻ = Level 2 (Cohort/quasi-experimental)
- ⬛◻◻◻ = Level 3-4 (Case-control, case series)

## Neural Mechanisms Summary

| Mechanism | Brain Regions | Evidence Type | Key Refs |
|-----------|---------------|---------------|----------|
| Auditory-motor coupling | STG, PMC, BG, SMA | fMRI, TMS | Zatorre, Thaut |
| Reward processing | NAcc, VTA, VMPFC | fMRI, PET | Salimpoor, Koelsch |
| Entrainment | BG, cerebellum, PMC | EEG, fMRI | Grahn, Large |
| Emotion | Amygdala, insula, ACC | fMRI | Koelsch |

## NIH Toolkit Building Blocks Checklist

For each intervention reviewed, ensure coverage of:

### Intervention Description
- [ ] Musical elements (melody, rhythm, harmony, timbre)
- [ ] Participation mode (active/receptive)
- [ ] Personalization level
- [ ] Cultural considerations

### Protocol Delivery
- [ ] Format (live/recorded)
- [ ] Setting (individual/group)
- [ ] Modality (in-person/telehealth)
- [ ] Session parameters (duration, frequency, total)
- [ ] Provider qualifications

### Population Specification
- [ ] Condition/diagnosis
- [ ] Severity/stage
- [ ] Inclusion/exclusion criteria
- [ ] Sample characteristics

### Control Conditions
- [ ] Control type used
- [ ] Appropriateness evaluated
- [ ] Blinding feasibility discussed

### Outcomes
- [ ] Clinical outcomes specified
- [ ] Mechanistic outcomes if applicable
- [ ] Measurement timing (immediate/delayed)
- [ ] Validated instruments used

## Quality Checklist

### Structure
- [ ] Key Points section (3-5 bullets)
- [ ] PRISMA flow diagram (systematic reviews)
- [ ] Table per major section
- [ ] Figure placeholders with captions
- [ ] Supplementary materials referenced

### Content
- [ ] Music therapy vs music medicine distinguished
- [ ] Theoretical frameworks explained
- [ ] All major interventions covered
- [ ] Neural mechanisms discussed (with hedging)
- [ ] Limitations for each intervention category
- [ ] Control condition issues addressed
- [ ] Future directions articulated
- [ ] Clinical implications stated (cautiously)

### Evidence Reporting
- [ ] Effect sizes reported (Cohen's d, SMD, Hedges' g)
- [ ] Confidence intervals included
- [ ] Sample sizes reported
- [ ] Evidence quality indicators used
- [ ] Risk of bias assessed
- [ ] Heterogeneity addressed

### Language
- [ ] Hedging language used ("may", "suggests", "appears to")
- [ ] No absolute claims
- [ ] Consistent terminology (per table above)
- [ ] All claims cited
- [ ] Technical terms defined

### References
- [ ] 60-100 references total
- [ ] NIH Toolkit/Sound Health cited
- [ ] Cochrane reviews cited
- [ ] Foundational works included
- [ ] Recent literature emphasized (5 years)
```

---

## IMPLEMENTATION_PLAN.md Template

```markdown
# Implementation Plan: [Music Therapy Review Title]

## Overview
- **Topic**: [specific MBI topic, e.g., "RAS for Parkinson's Disease Gait"]
- **Review type**: [Systematic review / Narrative review / Scoping review]
- **Target journals**: 
  - Music Therapy Perspectives
  - Journal of Music Therapy
  - Frontiers in Neuroscience
  - Neuropsychological Rehabilitation
  - [Other relevant journal]
- **Target length**: [word count], [reference count]
- **PROSPERO registration**: [ID if applicable]

## Stage 1: Protocol Development & Literature Collection
**Goal**: Develop search protocol and gather comprehensive corpus
**Status**: Not Started

### 1.1 Protocol Development
- [ ] Define PICO(S) elements
  - Population: [specific condition/population]
  - Intervention: [specific MBI type]
  - Comparator: [control conditions]
  - Outcomes: [primary and secondary]
  - Study design: [RCT, quasi-experimental, etc.]
- [ ] Draft inclusion/exclusion criteria
- [ ] Select quality assessment tools
- [ ] Register protocol (PROSPERO) if systematic review

### 1.2 PubMed/MEDLINE Search
- [ ] Develop MeSH + free text strategy
- [ ] Search: "Music Therapy"[Mesh] AND "[condition]"[Mesh]
- [ ] Search: "[intervention]"[tiab] AND "[condition]"[tiab]
- [ ] Apply filters (RCT, date range)
- [ ] Export results (target: 100-200 records)

### 1.3 Cochrane Library Search
- [ ] Search CDSR for existing reviews
- [ ] Extract key findings from relevant reviews
- [ ] Search CENTRAL for additional RCTs
- [ ] Note gaps in existing syntheses

### 1.4 PsycINFO Search
- [ ] Develop subject heading strategy
- [ ] Search for psychological/behavioral mechanism studies
- [ ] Export results (target: 50-100 records)

### 1.5 Additional Databases
- [ ] RILM - Music-specific studies
- [ ] CINAHL - Nursing/allied health
- [ ] ArXiv/bioRxiv - Neuroscience preprints
- [ ] ClinicalTrials.gov - Ongoing/completed trials
- [ ] Grey literature (dissertations, conference abstracts)

### 1.6 Screening & Selection
- [ ] Remove duplicates
- [ ] Title/abstract screening (dual if SR)
- [ ] Full-text retrieval
- [ ] Full-text screening
- [ ] Create PRISMA flow diagram

### 1.7 Organization
- [ ] Export to Zotero
- [ ] Categorize by intervention/population/outcome
- [ ] Create literature matrix
- [ ] Conduct gap analysis
- [ ] Targeted supplementary searches

## Stage 2: Quality Assessment & Data Extraction
**Goal**: Assess study quality and extract data systematically
**Status**: Not Started

### 2.1 Quality Assessment
- [ ] Select appropriate tools:
  - RCTs: Cochrane Risk of Bias 2.0
  - Non-randomized: ROBINS-I
  - Observational: Newcastle-Ottawa Scale
- [ ] Train assessors (if team)
- [ ] Assess each study
- [ ] Resolve discrepancies
- [ ] Create quality summary table

### 2.2 Data Extraction
- [ ] Design extraction form with NIH Building Blocks:
  - Study characteristics
  - Population details
  - Intervention parameters (dose, frequency, duration)
  - Control conditions
  - Outcome measures
  - Results (effect sizes, CIs, p-values)
- [ ] Pilot test extraction form
- [ ] Extract data from all studies
- [ ] Calculate effect sizes where missing

## Stage 3: Outline Development
**Goal**: Define paper structure based on evidence
**Status**: Not Started

- [ ] Finalize section headings
- [ ] Map papers to sections
- [ ] Plan comparison tables (minimum 5)
- [ ] Design figure placeholders (minimum 4)
- [ ] Align with NIH Toolkit Building Blocks

## Stage 4: Sections 1-2 (Introduction, Methods)
**Goal**: Write foundation sections
**Status**: Not Started

### Section 1: Introduction
- [ ] 1.1 Clinical Need and Rationale
  - Disease burden
  - Current treatment gaps
  - Why music may help
- [ ] 1.2 Defining the Intervention
  - Music therapy vs music medicine
  - Specific intervention description
  - Therapeutic affordances
- [ ] 1.3 Theoretical Framework
  - Neural mechanisms
  - Conceptual model
- [ ] 1.4 Existing Evidence
  - Previous reviews
  - Gaps addressed
- [ ] 1.5 Objectives

### Section 2: Methods
- [ ] 2.1 Protocol and Registration
- [ ] 2.2 Eligibility Criteria
- [ ] 2.3 Information Sources
- [ ] 2.4 Search Strategy
- [ ] 2.5 Selection Process
- [ ] 2.6 Data Extraction
- [ ] 2.7 Quality Assessment
- [ ] 2.8 Synthesis Methods

## Stage 5: Section 3 (Results - Study Characteristics)
**Goal**: Write descriptive results
**Status**: Not Started

- [ ] 3.1 Search Results (PRISMA diagram)
- [ ] 3.2 Study Characteristics
  - Design summary
  - Population summary
  - Intervention summary (Table: NIH Building Blocks)
  - Control conditions
  - Outcomes measured
- [ ] 3.3 Quality Assessment Results (Table)

## Stage 6: Section 4 (Results - Synthesis)
**Goal**: Write evidence synthesis
**Status**: Not Started

### Organize by [Intervention/Population/Outcome]
- [ ] 4.1 [Category 1]
  - Narrative synthesis
  - Effect sizes and CIs
  - Heterogeneity discussion
  - Evidence quality
- [ ] 4.2 [Category 2]
- [ ] 4.3 [Category 3]
- [ ] Summary comparison table
- [ ] Evidence map figure

### If Meta-analysis
- [ ] Forest plots
- [ ] Subgroup analyses
- [ ] Sensitivity analyses
- [ ] Publication bias assessment

## Stage 7: Sections 5-6 (Discussion, Conclusion)
**Goal**: Write synthesis sections
**Status**: Not Started

### Section 5: Discussion
- [ ] 5.1 Summary of Evidence
  - Key findings
  - Comparison with previous reviews
- [ ] 5.2 Mechanisms
  - Neural pathway evidence
  - Theoretical implications
- [ ] 5.3 Clinical Implications
  - Recommendations (with appropriate caution)
  - Implementation considerations
- [ ] 5.4 Strengths and Limitations
  - Review strengths
  - Evidence limitations
  - NIH Toolkit compliance gaps
- [ ] 5.5 Future Research Directions
  - Methodological improvements needed
  - Mechanism studies needed
  - Technology opportunities
  - Implementation research

### Section 6: Conclusion
- [ ] Summary statement
- [ ] Key recommendations
- [ ] Final caveats

## Stage 8: Integration & Polish
**Goal**: Finalize manuscript
**Status**: Not Started

### Content Finalization
- [ ] Write abstract (structured: Background, Methods, Results, Discussion)
- [ ] Write Key Points (3-5 bullets)
- [ ] Finalize all tables
- [ ] Create/finalize all figures
- [ ] Write figure/table captions

### Quality Assurance
- [ ] NIH Toolkit compliance check
- [ ] Terminology consistency check
- [ ] Hedging language verification
- [ ] Effect size reporting check
- [ ] Cross-reference verification
- [ ] Citation completeness check

### Final Steps
- [ ] Format references (journal style)
- [ ] Prepare supplementary materials
- [ ] Author contributions
- [ ] Conflict of interest statements
- [ ] Funding acknowledgments
- [ ] PRISMA checklist completion

## Key Literature Mapping

| Section | Key Papers | Notes |
|---------|------------|-------|
| Framework | Thaut (NMT), Koelsch (emotion), NIH Toolkit | Foundational |
| [Intervention 1] | [Paper A], [Paper B], [Paper C] | RCTs |
| [Intervention 2] | [Paper D], [Paper E] | Mixed quality |
| Mechanisms | Zatorre, Salimpoor, [fMRI studies] | Neuroscience |
| Cochrane | CD003477, CD006787 | Existing SRs |

## Literature Sources Summary

| Source | Query/Collection | Records | Included | Status |
|--------|------------------|---------|----------|--------|
| PubMed | [MeSH strategy] | N | N | [ ] |
| Cochrane CENTRAL | [terms] | N | N | [ ] |
| PsycINFO | [headings] | N | N | [ ] |
| RILM | [terms] | N | N | [ ] |
| ArXiv | [query] | N | N | [ ] |
| ClinicalTrials.gov | [terms] | N | N | [ ] |
| **Total unique** | - | N | N | - |

## Timeline

| Stage | Target Date | Actual Date | Status |
|-------|-------------|-------------|--------|
| Protocol | [date] | | [ ] |
| Search complete | [date] | | [ ] |
| Screening complete | [date] | | [ ] |
| Quality assessment | [date] | | [ ] |
| Draft complete | [date] | | [ ] |
| Revision | [date] | | [ ] |
| Submission | [date] | | [ ] |

## Change Log

### [Date] - Initial version
- Created implementation plan
- Defined scope and objectives
```

---

## Comparison Table Templates

### Table 1: Theoretical Frameworks

```markdown
**Table 1. Theoretical Frameworks for Music-Based Interventions**

| Framework | Core Principle | Neural Systems | Clinical Application | Key References |
|-----------|---------------|----------------|---------------------|----------------|
| Auditory-Motor Coupling | Rhythm entrains movement via shared neural substrates | BG, SMA, PMC, cerebellum | Gait disorders, motor rehabilitation | Thaut, Zatorre |
| Reward Circuitry | Music activates dopaminergic reward pathways | NAcc, VTA, VMPFC | Motivation, mood disorders | Salimpoor, Koelsch |
| Predictive Coding | Music engages prediction/error mechanisms | Auditory cortex, frontal regions | Learning, cognitive training | Vuust, Koelsch |
| SOBC (NIH) | Target identification and mechanism verification | Variable | All MBI research | NIH Toolkit |
| Resilience | Supportive music environment reduces stress | Stress response systems | Coping, chronic illness | Robb |
```

### Table 2: Intervention Characteristics (NIH Building Blocks)

```markdown
**Table 2. Music-Based Intervention Characteristics**

| Intervention | Mode | Musical Elements | Delivery | Provider | Typical Dose | Primary Target |
|--------------|------|------------------|----------|----------|--------------|----------------|
| RAS | Active | Rhythm, tempo | Live or recorded | MT, PT | 30 min, 3×/wk, 4-8 wk | Gait |
| MIT | Active | Melody, rhythm | Live | SLP, MT | 45 min, 5×/wk, 6 wk | Speech production |
| Music Listening | Receptive | All elements | Recorded | Any | Variable | Mood, pain, anxiety |
| GIM | Receptive | Selected music | Live guidance | Certified GIM | 90 min, weekly | Psychotherapy |
| Drumming | Active | Rhythm | Live, group | MT | 60 min, weekly | Social, motor |
| Singing | Active | Melody, rhythm, breath | Live | MT, SLP | 45 min, 2×/wk | Respiratory, mood |
```

### Table 3: Clinical Evidence Summary

```markdown
**Table 3. Evidence Summary for Music-Based Interventions by Condition**

| Condition | Intervention | N Studies | N Participants | Effect Size (95% CI) | Evidence Level | Key Outcomes |
|-----------|--------------|-----------|----------------|---------------------|----------------|--------------|
| PD - Gait | RAS | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛⬛◻ | Velocity, cadence, stride |
| PD - Balance | Dance | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛◻◻ | BBS, TUG |
| Stroke - Gait | RAS | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛⬛◻ | Velocity, symmetry |
| Stroke - Aphasia | MIT | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛⬛◻ | Naming, repetition |
| Dementia - Cognition | Music therapy | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛◻◻ | MMSE, MoCA |
| Dementia - BPSD | Music therapy | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛◻◻ | NPI, agitation |
| Depression | Music therapy | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛◻◻ | HDRS, BDI |
| Chronic Pain | Music listening | X | X | SMD = 0.XX (0.XX-0.XX) | ⬛⬛◻◻ | VAS, analgesic use |

*Evidence Level: ⬛⬛⬛⬛ = SR of RCTs; ⬛⬛⬛◻ = Individual RCT; ⬛⬛◻◻ = Quasi-experimental; ⬛◻◻◻ = Case series*
```

### Table 4: Outcome Measures by Domain

```markdown
**Table 4. Recommended Outcome Measures for MBI Studies**

| Domain | Measure | Type | Validated For | Administration | Psychometrics |
|--------|---------|------|---------------|----------------|---------------|
| **Motor - Gait** | 10-Meter Walk Test | Performance | PD, Stroke | 2 min | Excellent reliability |
| | 6-Minute Walk Test | Performance | Multiple | 10 min | Good validity |
| | GAITRite | Instrumented | PD, Stroke | Variable | Excellent precision |
| **Motor - Balance** | Berg Balance Scale | Performance | Older adults | 20 min | Good reliability |
| | Timed Up and Go | Performance | Falls risk | 2 min | Excellent |
| **Motor - Upper limb** | ARAT | Performance | Stroke | 15 min | Good validity |
| **Cognition** | MMSE | Performance | Dementia | 10 min | Well-established |
| | MoCA | Performance | MCI, Dementia | 10 min | Good sensitivity |
| | NIH Toolbox Cognition | Performance | General | 30 min | Excellent norms |
| **Speech** | WAB-R | Performance | Aphasia | 60 min | Gold standard |
| | BNT | Performance | Naming | 15 min | Good validity |
| **Mood** | PHQ-9 | Self-report | Depression | 5 min | Excellent |
| | GAD-7 | Self-report | Anxiety | 5 min | Excellent |
| | GDS | Self-report | Older adults | 5 min | Good validity |
| **Quality of Life** | SF-36 | Self-report | General | 10 min | Excellent |
| | PDQ-39 | Self-report | Parkinson's | 15 min | Good validity |
| | DEMQOL | Self-report | Dementia | 15 min | Good validity |
| **BPSD** | NPI | Caregiver | Dementia | 20 min | Well-established |
| **Pain** | VAS | Self-report | General | 1 min | Good validity |
| | BPI | Self-report | Chronic pain | 5 min | Good validity |
| **Biomarker** | HRV | Physiological | Stress | Continuous | Good reliability |
| | Cortisol | Biological | Stress | Variable | Established |
```

### Table 5: Methodological Quality Assessment

```markdown
**Table 5. Risk of Bias Assessment for Included RCTs**

| Study | Random Sequence | Allocation Concealment | Blinding (Participants) | Blinding (Outcome) | Incomplete Data | Selective Reporting | Other | Overall |
|-------|-----------------|----------------------|------------------------|-------------------|-----------------|--------------------|----|---------|
| Author 2023 | ✓ Low | ✓ Low | ? Unclear | ✓ Low | ✓ Low | ✓ Low | ✓ | Low |
| Author 2022 | ✓ Low | ? Unclear | ✗ High | ✓ Low | ✓ Low | ✓ Low | ✓ | Some concerns |
| Author 2021 | ? Unclear | ✗ High | ✗ High | ? Unclear | ✓ Low | ✓ Low | ? | High |

*✓ = Low risk; ? = Unclear/Some concerns; ✗ = High risk*
*Note: Blinding of participants is often not feasible in MBI studies; assessor blinding is critical*
```

### Table 6: NIH Building Blocks Compliance

```markdown
**Table 6. NIH MBI Toolkit Building Blocks Compliance Assessment**

| Study | Intervention Defined | Musical Elements | Dose Specified | Control Appropriate | Fidelity Monitored | Outcomes Validated | Compliance Score |
|-------|---------------------|------------------|----------------|--------------------|--------------------|-------------------|-----------------|
| Author 2023 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | 6/6 |
| Author 2022 | ✓ | ✓ | ✓ | ? | ✗ | ✓ | 4/6 |
| Author 2021 | ✓ | ? | ✓ | ✗ | ✗ | ✓ | 3/6 |

*✓ = Adequately addressed; ? = Partially addressed; ✗ = Not addressed*
```

### Table 7: Technology-Enhanced MBI Tools

```markdown
**Table 7. Technology-Enhanced Music-Based Intervention Tools**

| Tool/System | Type | Technology | Target Population | Evidence Level | Accessibility | Reference |
|-------------|------|------------|-------------------|----------------|---------------|-----------|
| EyeHarp | ADMI | Eye-tracking | Motor impairment | Pilot studies | Open source | [ref] |
| Soundbeam | ADMI | Motion sensor | Physical disability | Case studies | Commercial | [ref] |
| Rhythmic Auditory Cueing App | Mobile app | Metronome + music | PD
```
