---
name: music-therapy-review
description: Write comprehensive literature reviews for music therapy and music-based intervention (MBI) research. Use when writing survey papers, systematic reviews, or literature analyses on topics like neurologic music therapy, rhythm-based interventions, music medicine, or therapeutic applications for neurological/psychiatric conditions. Triggers on requests for "review paper", "survey", "literature review", "综述", "音乐疗法", "music therapy", "MBI", or mentions of writing academic reviews on music-based interventions for health.
allowed-tools:
  - Read
  - Write
  - Edit
  - Glob
  - Grep
  - Bash
  - WebSearch
  - WebFetch
  - TodoWrite
---

# Music Therapy & Music-Based Intervention Literature Review Writing Skill

A systematic workflow for writing comprehensive literature reviews in music therapy and music-based interventions (MBIs).

## Quick Start

When user requests a literature review:

1. **Initialize project** with three core files:
   - `CLAUDE.md` - Writing guidelines and terminology
   - `IMPLEMENTATION_PLAN.md` - Staged execution plan
   - `manuscript_draft.md` - Main manuscript

2. **Follow the 7-phase workflow** (see [WORKFLOW.md](WORKFLOW.md))

3. **Use standard templates** (see [TEMPLATES.md](TEMPLATES.md))

## Core Principles

### Writing Style
- Use **hedging language**: "may", "suggests", "appears to", "has shown promising results"
- Avoid absolute claims: Never say "X is the most effective intervention"
- Every claim needs citation support
- Distinguish clearly between **music therapy** (credentialed therapist + therapeutic relationship) and **music medicine** (music as "medication")
- Each intervention section needs a **Limitations** and **Evidence Quality** paragraph

### Required Elements
- **Key Points box** (3-5 bullets) after title
- **Comparison table** for each intervention category
- **Evidence quality indicators** (RCT, meta-analysis, case study)
- **Effect sizes** with consistent format (Cohen's d, Hedges' g, or SMD)
- **NIH Toolkit Building Blocks** compliance check
- **Figure placeholders** with detailed captions
- **References organized by topic** (80-120 typical)

### Paragraph Structure
1. Topic sentence (main claim about intervention/mechanism)
2. Supporting evidence (citations + outcome data)
3. Mechanistic explanation (neural pathway or theoretical framework)
4. Limitations and gaps
5. Transition to next paragraph

### Terminology Standards

| Preferred Term | Avoid | Reason |
|----------------|-------|--------|
| Music-based intervention (MBI) | Music treatment | NIH standardized terminology |
| Music therapy | Music healing | Professional credential required |
| Music medicine | Background music therapy | Distinct from credentialed practice |
| Rhythmic auditory stimulation (RAS) | Beat therapy | Technical precision |
| Melodic intonation therapy (MIT) | Singing therapy | Established protocol name |
| Therapeutic affordances | Music benefits | Theoretical framework term |
| Auditory-motor coupling | Sound-movement link | Neuroscience precision |

## Literature Sources

### ArXiv MCP (Preprints & Latest Research)

GitHub: https://github.com/blazickjp/arxiv-mcp-server

**Available Tools:**
- `search_papers` - Search by keywords with date range and category filters
- `download_paper` - Download paper by arXiv ID
- `list_papers` - List all downloaded papers
- `read_paper` - Read downloaded paper content

**Configuration:**
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
```

**Usage Example:**
```
Search: "music therapy neural" OR "auditory-motor coupling"
Categories: q-bio.NC, cs.SD, cs.HC, eess.AS
Date range: 2020-01-01 to present
Max results: 50
```

**Relevant Categories:**
- q-bio.NC (Neurons and Cognition)
- cs.SD (Sound)
- cs.HC (Human-Computer Interaction)
- eess.AS (Audio and Speech Processing)

### PubMed MCP (Biomedical Literature)

GitHub: https://github.com/grll/pubmedmcp

Access 35+ million biomedical literature citations.

**Configuration:**
```json
{
  "mcpServers": {
    "pubmedmcp": {
      "command": "uvx",
      "args": ["pubmedmcp@latest"],
      "env": {
        "UV_PRERELEASE": "allow",
        "UV_PYTHON": "3.12"
      }
    }
  }
}
```

**MeSH Terms for Music Therapy:**
- "Music Therapy"[Mesh]
- "Acoustic Stimulation"[Mesh]
- "Auditory Perception"[Mesh]
- "Parkinson Disease/rehabilitation"[Mesh]
- "Stroke Rehabilitation"[Mesh]
- "Dementia/therapy"[Mesh]

**Search Example:**
```
("Music Therapy"[Mesh] OR "music-based intervention"[tiab])
AND ("Parkinson Disease"[Mesh] OR "Stroke"[Mesh])
AND ("randomized controlled trial"[pt] OR "meta-analysis"[pt])
```

**Search Tips:**
- Use MeSH terms for precise medical searches
- Combine with publication type filters (Review, Clinical Trial)
- Filter by date for recent literature

### Zotero Integration (Reference Management)

Access local Zotero database (Requires the user to provide their user ID.):
```bash
# List collections
curl -s "http://localhost:23119/api/users/[USER_ID]/collections"

# Get items from collection
curl -s "http://localhost:23119/api/users/[USER_ID]/collections/[KEY]/items"
```

Alternatively, Zotero-MCP can be used, but it requires users to perform manual configuration in advance.

Extract: title, abstractNote, date, creators, publicationTitle, DOI

### Source Selection Guide

| Source | Best For | Strengths |
|--------|----------|-----------|
| **ArXiv** | Latest computational methods, neuroscience research | Preprints, fast access, CS/AI focus |
| **PubMed** | Clinical trials, RCTs, medical applications | Peer-reviewed, MeSH indexing, clinical |
| **Zotero** | Organized collections, existing library | Local management, annotations, PDFs |

## Standard Review Structure

```markdown
# [Title]: A Systematic Review of Evidence and Neural Mechanisms

## Key Points
- [3-5 bullets summarizing main findings]

## Abstract

## 1. Introduction
### 1.1 Clinical Need and Rationale
### 1.2 Defining Music-Based Interventions
#### 1.2.1 Music Therapy vs Music Medicine
#### 1.2.2 Therapeutic Affordances Framework
### 1.3 Neural Mechanisms Overview
### 1.4 Scope and Contributions

## 2. Methods
### 2.1 Search Strategy
### 2.2 Inclusion/Exclusion Criteria
### 2.3 Quality Assessment
### 2.4 Data Extraction

## 3. Theoretical Frameworks
### 3.1 Brain Circuitry Framework
#### 3.1.1 Auditory-Motor Pathway
#### 3.1.2 Auditory-Reward Pathway
#### 3.1.3 Auditory-Cognitive Pathway
### 3.2 Conceptual Models (NIH Toolkit)
#### 3.2.1 Experimental Medicine Framework (SOBC)
#### 3.2.2 Neuromechanistic Framework
#### 3.2.3 Resilience Framework

**Table 1. Theoretical Frameworks for MBI Research**
| Framework | Core Principle | Application | Key References |

## 4. Intervention Categories
### 4.1 Neurologic Music Therapy
#### 4.1.1 Rhythmic Auditory Stimulation (RAS)
#### 4.1.2 Melodic Intonation Therapy (MIT)
#### 4.1.3 Other NMT Techniques
### 4.2 Receptive Music Interventions
#### 4.2.1 Music Listening
#### 4.2.2 Guided Imagery with Music
### 4.3 Active Music Interventions
#### 4.3.1 Singing-Based Interventions
#### 4.3.2 Instrument Playing
#### 4.3.3 Dance and Movement to Music
### 4.4 Technology-Enhanced MBIs
#### 4.4.1 Adaptive Digital Musical Instruments
#### 4.4.2 Music-Based Serious Games
#### 4.4.3 AI and Personalized Music Systems

**Table 2. Intervention Comparison**
| Intervention | Mode | Population | Mechanism | Evidence Level | Key Outcome |

## 5. Clinical Applications
### 5.1 Neurological Disorders
#### 5.1.1 Parkinson's Disease
#### 5.1.2 Stroke Rehabilitation
#### 5.1.3 Traumatic Brain Injury
### 5.2 Neurodegenerative Disorders
#### 5.2.1 Alzheimer's Disease and Dementia
### 5.3 Psychiatric Disorders
#### 5.3.1 Depression
#### 5.3.2 Anxiety
### 5.4 Developmental Disorders
#### 5.4.1 Autism Spectrum Disorder
### 5.5 Pain Management

**Table 3. Clinical Evidence Summary**
| Condition | Intervention | Outcomes | Effect Size | Evidence Quality | N (studies) |

## 6. Outcome Measures and Biomarkers
### 6.1 Clinical Outcome Measures
### 6.2 Mechanistic Outcome Measures
### 6.3 Biomarkers
#### 6.3.1 Neuroimaging Biomarkers
#### 6.3.2 Physiological Biomarkers
#### 6.3.3 Auditory Biomarkers

**Table 4. Recommended Outcome Measures**
| Domain | Measure | Type | Validity | Clinical Use |

## 7. Methodological Considerations
### 7.1 NIH MBI Toolkit Building Blocks
### 7.2 Control Condition Design
### 7.3 Dosage Parameters
### 7.4 Treatment Fidelity

**Table 5. Methodological Quality Assessment**
| Study | Randomization | Blinding | Control | Fidelity | Attrition | Overall |

## 8. Discussion
### 8.1 Summary of Evidence
### 8.2 Gaps in Current Research
### 8.3 Challenges and Limitations
#### 8.3.1 Heterogeneity of Interventions
#### 8.3.2 Control Condition Difficulties
#### 8.3.3 Blinding Challenges
### 8.4 Future Directions
#### 8.4.1 Precision Music Medicine
#### 8.4.2 Technology Integration
#### 8.4.3 Mechanism Elucidation

## 9. Conclusion

## References
```

## Intervention Description Template

```markdown
### 4.X [Intervention Category]

[1-2 paragraph introduction with clinical rationale and theoretical basis]

**Mechanism:** [Neural pathway or theoretical framework explanation]
- Auditory-motor coupling via [specific pathway]
- Engagement of [brain regions/networks]
- Therapeutic affordance: [emotion regulation / entrainment / social bonding]

**[Intervention Name]:** [Author] et al. [ref] investigated [intervention] in [population]:
- **Design:** [RCT/quasi-experimental/case series]
- **Sample:** N=[number], [demographics]
- **Protocol:** [frequency, duration, total sessions]
- **Delivery:** [therapist-led/recorded/technology-assisted]
- **Outcome:** [primary outcome] improved by [effect size] (p<0.05)

**NIH Building Blocks Compliance:**
- [ ] Intervention clearly defined
- [ ] Dosage parameters specified
- [ ] Control condition appropriate
- [ ] Outcome measures validated

**Comparative Evidence:**
| Study | N | Design | Duration | Effect Size | Quality |
|-------|---|--------|----------|-------------|---------|

**Limitations:** Despite promising results, [intervention] faces:
(1) [methodological limitation];
(2) [generalizability issue];
(3) [mechanistic gap].

**Clinical Translation:** [Current clinical uptake and barriers]
```

## Citation Patterns

```markdown
# Effect size citation
"...demonstrated significant improvement (SMD = 0.75, 95% CI: 0.42-1.08) [23]"

# RCT citation
"In a randomized controlled trial (N=120), Smith et al. [45] found..."

# Cochrane review citation
"A Cochrane systematic review [12] concluded that evidence is..."

# Multi-study citation
"Several RCTs have demonstrated benefits... [12, 15, 23, 31]"

# Comparative
"While RAS has strong evidence for gait [12], MIT shows promise for aphasia [15]"

# Mechanism citation
"The auditory-motor coupling hypothesis [Zatorre & Halpern, 2005] suggests..."

# NIH framework citation
"Following the NIH MBI Toolkit guidelines [Cheung et al., 2023]..."
```

## Evidence Quality Indicators

Use standardized evidence quality notation:

| Level | Description                         | Notation |
| ----- | ----------------------------------- | -------- |
| 1a    | Systematic review of RCTs           | ⬛⬛⬛⬛     |
| 1b    | Individual RCT                      | ⬛⬛⬛◻     |
| 2a    | Systematic review of cohort studies | ⬛⬛◻◻     |
| 2b    | Individual cohort study             | ⬛⬛◻◻     |
| 3     | Case-control studies                | ⬛◻◻◻     |
| 4     | Case series/reports                 | ◻◻◻◻     |

## Effect Size Reporting Standards

```markdown
# Continuous outcomes
Cohen's d = 0.XX (95% CI: X.XX - X.XX)
Hedges' g = 0.XX (preferred for small samples)
SMD = 0.XX (for meta-analyses)

# Interpretation guide
Small: d ≈ 0.2
Medium: d ≈ 0.5
Large: d ≈ 0.8

# Binary outcomes
OR = X.XX (95% CI: X.XX - X.XX)
RR = X.XX (95% CI: X.XX - X.XX)
NNT = X
```

## Quality Checklist

Before completion, verify:

### Content Quality

* [ ] Key Points present (3-5 bullets)
* [ ] Clear distinction between music therapy and music medicine
* [ ] Theoretical framework(s) explained
* [ ] Neural mechanisms discussed with appropriate hedging
* [ ] Table per major intervention category
* [ ] Limitations for each intervention type
* [ ] Evidence quality indicated for each claim
* [ ] Effect sizes reported consistently

### NIH Toolkit Compliance

* [ ] Building blocks framework referenced
* [ ] Dosage parameters reported for interventions
* [ ] Control conditions evaluated
* [ ] Outcome measures categorized (clinical/mechanistic)
* [ ] Biomarkers discussed where applicable

### Methodological Rigor

* [ ] Search strategy documented
* [ ] Inclusion/exclusion criteria stated
* [ ] Quality assessment performed
* [ ] Heterogeneity addressed
* [ ] Publication bias considered

### Writing Quality

* [ ] Consistent terminology throughout (see table above)
* [ ] Hedging language used appropriately
* [ ] 80-120 references, organized by topic
* [ ] Figure placeholders with captions
* [ ] PRISMA diagram included (for systematic reviews)

## Domain-Specific Considerations

### For Neurologic Music Therapy Reviews

* Emphasize RAS and MIT protocols
* Include motor outcome measures (gait parameters, UPDRS)
* Discuss basal ganglia and auditory-motor circuitry
* Reference Thaut's neurologic music therapy framework

### For Dementia/Aging Reviews

* Address cognitive and behavioral outcomes separately
* Include quality of life measures
* Discuss music and autobiographical memory
* Reference NIH Sound Health aging focus

### For Technology-Enhanced MBI Reviews

* Categorize by technology type (ADMI, games, AI)
* Include usability and accessibility considerations
* Discuss home-based vs clinical delivery
* Reference MIR and HCI frameworks

### For Mechanism-Focused Reviews

* Emphasize neuroimaging evidence
* Discuss animal models where applicable
* Include TMS and causal evidence
* Reference ASAP hypothesis and reward circuitry

## Key References to Include

### Foundational Works

* Thaut, M.H. (Neurologic Music Therapy)
* Koelsch, S. (Music and emotion neuroscience)
* Zatorre, R.J. (Auditory-motor coupling)
* Salimpoor, V.N. (Music and reward)

### NIH Framework Documents

* NIH MBI Toolkit (Cheung et al., 2023)
* Sound Health Initiative publications
* Brain circuitry strategies paper

### Cochrane Reviews

* Music therapy for dementia
* Music interventions for acquired brain injury
* Music therapy for depression

## File References

* [WORKFLOW.md](WORKFLOW.md) - Detailed 7-phase workflow
* [TEMPLATES.md](TEMPLATES.md) - CLAUDE.md and IMPLEMENTATION_PLAN.md templates
* [DOMAINS.md](DOMAINS.md) - Music therapy theoretical frameworks and intervention categories
