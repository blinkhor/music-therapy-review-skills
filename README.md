# Music Therapy Literature Review Skill

A comprehensive Claude skill for writing systematic literature reviews on music therapy and music-based interventions (MBIs). This skill provides structured workflows, templates, and guidelines for producing high-quality academic reviews in the field of music therapy research.

中文文档
 | English

Overview

This skill enables systematic and rigorous literature review writing for music therapy research, covering:

Neurologic Music Therapy (NMT): Rhythmic Auditory Stimulation (RAS), Melodic Intonation Therapy (MIT)

Clinical Applications: Parkinson's disease, stroke rehabilitation, dementia, depression, anxiety

Neural Mechanisms: Auditory-motor coupling, reward circuitry, cognitive pathways

Technology-Enhanced Interventions: Adaptive digital instruments, music-based games, AI systems

Key Features
📚 Comprehensive Literature Sources

PubMed/MEDLINE: Clinical trials and biomedical research

Cochrane Library: Systematic reviews and meta-analyses

PsycINFO: Psychological mechanisms and behavioral outcomes

ArXiv/bioRxiv: Latest neuroscience and computational methods

ClinicalTrials.gov: Ongoing and completed trials

📝 Structured Writing Framework

7-phase workflow from initialization to publication

NIH MBI Toolkit compliance

Standardized terminology and hedging language

Evidence quality indicators

PRISMA guidelines for systematic reviews

🎯 Quality Assurance

Methodological rigor checks

NIH Building Blocks compliance verification

Evidence quality assessment

Consistent effect size reporting

Publication bias consideration

Quick Start
Trigger Phrases

The skill activates when you mention:

"literature review" / "综述"

"music therapy" / "音乐疗法"

"systematic review"

"MBI" (music-based intervention)

"survey paper"

Basic Usage
Write a systematic review on rhythmic auditory stimulation for Parkinson's disease gait rehabilitation
帮我写一篇关于音乐疗法改善阿尔茨海默病认知功能的综述
Project Structure
music-therapy-review/
├── skill.md                    # Skill definition and core principles
├── WORKFLOW.md                 # 7-phase detailed workflow
├── TEMPLATES.md                # Project file templates
├── DOMAINS.md                  # Theoretical frameworks (empty in current version)
├── papers.json                 # Sample literature database
└── README.md                   # This file
Core Principles
Writing Style

Hedging Language: Use "may", "suggests", "appears to" instead of absolute claims

Evidence-Based: Every claim requires citation support

Precision: Distinguish music therapy (credentialed) from music medicine

Transparency: Report effect sizes, confidence intervals, and limitations

Required Elements

Key Points box (3-5 bullets)

Comparison tables for each intervention category

Evidence quality indicators (⬛⬛⬛◻ system)

Effect sizes with consistent format

NIH Toolkit Building Blocks compliance

PRISMA flow diagram (for systematic reviews)

Terminology Standards
Preferred Term	Avoid	Reason
Music-based intervention (MBI)	Music treatment	NIH standardized
Music therapy	Music healing	Professional credential required
Rhythmic auditory stimulation (RAS)	Beat therapy	Technical precision
Melodic intonation therapy (MIT)	Singing therapy	Established protocol name
Auditory-motor coupling	Sound-movement link	Neuroscience precision
Workflow Overview
Phase 1: Project Initialization

Create project structure (CLAUDE.md, IMPLEMENTATION_PLAN.md, manuscript_draft.md)

Set up writing guidelines and terminology standards

Phase 2: Literature Collection

Search multiple databases (PubMed, Cochrane, PsycINFO, ArXiv)

Screen and select studies using PRISMA guidelines

Conduct quality assessment

Create literature matrix

Phase 3: Outline Development

Define theoretical frameworks

Organize intervention categories

Map papers to sections

Plan comparison tables and figures

Phase 4: Section Writing

Write theoretical framework sections

Write intervention sections with NIH Building Blocks

Write clinical application sections

Include limitations and evidence quality

Phase 5: Tables and Figures

Create comparison tables

Generate PRISMA flow diagram

Design neural pathway schematics

Create evidence maps

Phase 6: Quality Assurance

Structure check

Content check

NIH Toolkit compliance verification

Evidence quality check

Language and reference check

Phase 7: Incremental Updates

Set up monitoring alerts

Quarterly review cycle

Version control and change log

Example Output Structure
# [Title]: A Systematic Review of Evidence and Neural Mechanisms

**Key Points**
- [3-5 bullet points summarizing main findings]

## Abstract

## 1. Introduction
### 1.1 Clinical Need and Rationale
### 1.2 Defining Music-Based Interventions
### 1.3 Neural Mechanisms Overview
### 1.4 Scope and Contributions

## 2. Methods
### 2.1 Search Strategy
### 2.2 Inclusion/Exclusion Criteria
### 2.3 Quality Assessment

## 3. Theoretical Frameworks
### 3.1 Brain Circuitry Framework
### 3.2 NIH Conceptual Models

## 4. Intervention Categories
### 4.1 Neurologic Music Therapy
### 4.2 Receptive Music Interventions
### 4.3 Active Music Interventions
### 4.4 Technology-Enhanced MBIs

## 5. Clinical Applications
### 5.1 Neurological Disorders
### 5.2 Neurodegenerative Disorders
### 5.3 Psychiatric Disorders

## 6. Discussion
### 6.1 Summary of Evidence
### 6.2 Gaps and Future Directions

## 7. Conclusion

## References
Sample Literature Database

The papers.json file contains 30+ curated papers covering:

Chronic pain management

Work-related stress

Emotional regulation in college students

Alzheimer's disease and dementia

Stroke rehabilitation

Parkinson's disease

Depression and anxiety

Key References
Foundational Works

Thaut, M.H. - Neurologic Music Therapy

Koelsch, S. - Music and emotion neuroscience

Zatorre, R.J. - Auditory-motor coupling

Salimpoor, V.N. - Music and reward

NIH Framework

NIH MBI Toolkit (Cheung et al., 2023)

Sound Health Initiative publications

Brain circuitry strategies paper

Cochrane Reviews

Music therapy for dementia (CD003477)

Music interventions for acquired brain injury (CD006787)

Music therapy for depression (CD004517)

Evidence Quality System
Level	Description	Notation
1a	Systematic review of RCTs	⬛⬛⬛⬛
1b	Individual RCT	⬛⬛⬛◻
2a	Systematic review of cohort studies	⬛⬛◻◻
2b	Individual cohort study	⬛⬛◻◻
3	Case-control studies	⬛◻◻◻
4	Case series/reports	◻◻◻◻
Contributing

This skill is designed for academic research in music therapy. Contributions should maintain:

Scientific rigor and evidence-based approach

NIH MBI Toolkit compliance

Consistent terminology and formatting

Transparent reporting of methods and results

License

This skill is provided for academic and research purposes.

Citation

If you use this skill in your research, please cite:

Music Therapy Literature Review Skill (2024)
GitHub: [repository URL]
Contact

For questions or suggestions about this skill, please open an issue in the repository.
