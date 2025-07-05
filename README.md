# 🔍 PredCatchAnalysis

A data repository and analytical framework based on predator catcher interviews, focusing on behavioral analysis, interviewer techniques, and statistical patterns.

> ⚠️ **DEVELOPMENT STATUS** ⚠️  
> This repository is currently in early development stages. Data structures, analysis methods, and documentation are actively evolving.

## Project Overview

This repository contains structured data from predator catching interviews, including:
- Text data from interview conversations
- Behavioral analysis of subject responses
- Interviewer technique assessment
- Statistical data on patterns across multiple interviews

The project aims to identify effective interview techniques, common deception patterns, and provide evidence-based insights for law enforcement, researchers, decoys and predator catching teams.

## Repository Structure

```
PredCatchAnalysis/
├── scripts/
│   ├── processing/
│   └── visualization/
├── events/
│   └── [catcher]_[iso-date]_[city-state]/
│       ├── analysis/
│       │   ├── admissions.md
│       │   ├── behavioral.md
│       │   ├── deception.md
│       │   ├── linguistic.md
│       │   ├── summary.md
│       │   ├── techniques.md
│       │   └── timeline.md
│       └── raw/
│           ├── interview.json
│           └── metadata.json
└── schemas/
    └── interview.schema.json
```

## Interview Data Format

Interview data is stored in a structured JSON format following a defined schema. The schema is available in the repository at [`schemas/transcription.schema.json`](schemas/transcription.schema.json).

### Key Data Points

| Level | Data Point | Description |
|-------|------------|-------------|
| **Document** | `language` | Primary language of the interview |
| | `num_speakers` | Number of distinct speakers |
| **Segment** | `speaker` | Speaker identifier (e.g., "interviewer", "subject") |
| | `start`/`end` | Timestamp in seconds |
| | `text` | Transcribed speech segment |
| | `duration` | Length of speech segment in seconds |
| **Word** | `word` | Individual transcribed word |
| | `start`/`end` | Precise timestamp for each word |
| | `probability` | Confidence score for word accuracy |

### Sample Visualization

```
[00:01:23] Interviewer: "Did she tell you she was 11?"
[00:01:28] Subject:     "I don't remember."
           ^^^^^^^^^    ^^^^^^^^^^^^^^^^^^^
           Speaker      Text content
```

This granular structure allows for detailed analysis of response timing, speech patterns, and confidence metrics across interviews.

## Analysis Framework

Analysis is conducted across multiple dimensions:

### Behavioral Analysis
- Deception indicators
- Minimization techniques
- Admission patterns
- Self-contradiction tracking
- Evasion strategies

### Interviewer Techniques
- Rapport building effectiveness
- Question sequencing
- Evidence presentation strategy
- Pressure application methods
- Confession elicitation success rates

### Statistical Patterns
- Common excuses and rationalizations
- Platform frequency analysis
- Demographic correlations
- Technique effectiveness metrics
- Temporal patterns in admissions

## Usage

This repository is intended for:
- Researchers studying predatory behavior
- Law enforcement training
- Forensic psychology professionals
- Predator catching organizations

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This repository examines sensitive dialogue from online predator catching operations. It is intended solely for research, educational, and law enforcement purposes. The maintainers of this repository do not condone or support any illegal activities.
