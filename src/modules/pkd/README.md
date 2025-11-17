# PKD Module - ПКД Expert System

**Ukrainian Building Standards Validation & Generation**

Comprehensive toolkit for working with ПКД (Проєктно-кошторисна документація) - project cost documentation - based on Ukrainian building standards (ДБН, ДСТУ, ISO).

---

## 📚 What is ПКД?

ПКД (Проєктно-кошторисна документація) is project-estimate documentation required for construction projects in Ukraine. It consists of 14 volumes covering all aspects of project design, from site investigations to cost estimates.

**Key Standard:** ДБН А.2.2-3:2014 - Structure and content of project documentation

---

## 🎯 Module Capabilities

### Validation
- **Structure Validation:** Verify volume structure compliance with ДБН А.2.2-3
- **Reference Validation:** Check ДБН/ДСТУ reference format and existence
- **Compliance Reports:** Full compliance check with recommendations
- **Multi-Project Support:** Residential (Додаток Д) + Industrial (Додаток Е)

### Standards Knowledge Base

**ДБН Standards (7 files):**
- ДБН А.2.2-3:2014 - Structure and content (⭐⭐⭐ CORE)
- ДБН А.2.1-1:2014 - Engineering surveys
- ДБН В.2.5-39:2008 - Heat networks, dispatch
- ДБН В.2.5-23:2010 - Electrical equipment
- ДБН В.2.5-67:2013 - Heat supply
- ДБН В.1.1-7:2016 - Fire safety
- KMU-373-2021 - Cybersecurity for critical infrastructure

**ДСТУ Standards (2 files):**
- ДСТУ Б А.2.4-7:2009 - Drawing formatting
- ДСТУ-Н Б В.1.2-16:2013 - CC1 class calculation

**Reference Matrix:**
- standards-matrix.md - Volume × Standard mapping with priorities

---

## 🤖 Agents

### Maksym - DBN Expert

**Role:** ДБН Експерт - Валідація ПКД

**Icon:** 📋 (Compliance checklist)

**Purpose:** Validates project documentation (ПКД) structure compliance with Ukrainian building standards (ДБН А.2.2-3:2014)

**Scope:**
- VALIDATION ONLY (not generation, not calculations)
- Multi-project support: Додаток Д (residential) + Додаток Е (industrial)
- Universal scope: житлові, промислові, інфраструктурні об'єкти

**Commands:**
- `*validate-structure` - Validate volume structure against ДБН А.2.2-3
- `*check-compliance` - Full compliance check with detailed report
- `*check-reference` - Validate ДБН reference format and existence
- `*list-requirements` - List requirements from ДБН standard or volume
- `*find-standard` - Find relevant ДБН standard for topic with priority

**Communication:** Ukrainian only (technical documentation language)

**Expertise:**
- 15+ років досвіду з ПКД за стандартами ДБН
- Compliance First, Reference Everything, Zero Assumptions
- Systematic validation: структура → зміст → посилання

---

## 🚀 Getting Started

### Installation

```bash
# Install BMAD with PKD module
npx bmad-method@alpha install

# During installation, select "PKD - ПКД Expert System"
```

### Configuration

During installation, you'll be asked:
1. **Output location** - Where to save validation reports (default: `output/pkd`)
2. **Standards focus** - ДБН, ДСТУ, or All Standards
3. **Project type** - Residential, Industrial, or Infrastructure

### First Validation

```bash
# Load Maksym agent in your IDE
*dbn-expert

# Validate volume structure
*validate-structure

# User provides volume number (1-14)
# Agent validates structure per ДБН А.2.2-3
```

---

## 📖 Use Cases

### Use Case 1: Validate Existing ПКД

**Scenario:** You have project documentation and need to verify ДБН compliance

**Workflow:**
1. Load DBN Expert agent: `*dbn-expert`
2. Run compliance check: `*check-compliance`
3. Review report with recommendations
4. Fix missing/incorrect sections

### Use Case 2: Check ДБН Reference

**Scenario:** You're writing documentation and want to verify a ДБН reference

**Workflow:**
1. Load DBN Expert: `*dbn-expert`
2. Run reference check: `*check-reference`
3. Provide reference string (e.g., "ДБН В.2.5-39:2008 п.15.2")
4. Get validation result with suggestions

### Use Case 3: Find Relevant Standard

**Scenario:** You need a standard for a specific topic (e.g., "автоматизація")

**Workflow:**
1. Load DBN Expert: `*dbn-expert`
2. Search standards: `*find-standard`
3. Provide keyword/topic
4. Get ranked list with priorities (⭐⭐⭐ > ⭐⭐ > ⭐)

---

## 🏗️ Module Structure

```
pkd/
├── agents/
│   ├── dbn-expert.agent.yaml          # Maksym - DBN Expert
│   └── dbn-expert-sidecar/
│       ├── instructions.md            # Validation rules
│       └── memories.md                # Project context
├── data/
│   ├── dbn/                           # ДБН Standards (7 files)
│   │   ├── DBN-A.2.2-3-2014.md       # ⭐⭐⭐ CORE
│   │   ├── DBN-V.2.5-39-2008.md      # Heat networks
│   │   └── ... (5 more standards)
│   ├── dstu/                          # ДСТУ Standards (2 files)
│   │   ├── DSTU-B-A.2.4-7-2009.md
│   │   └── DSTU-N-B-V.1.2-16-2013.md
│   └── iso/                           # ISO Standards (placeholder)
├── workflows/                         # (Future: generation workflows)
├── config.yaml                        # Generated from install-config.yaml
└── README.md                          # This file
```

---

## 🎓 ДБН Standards Overview

### ДБН А.2.2-3:2014 - Structure and Content

**Purpose:** Defines structure and content requirements for project documentation

**Key Appendices:**
- **Додаток Д:** Residential/non-industrial objects (12-15 sections)
- **Додаток Е:** Industrial/production objects (19 sections for Volume 1)

**Project Types:**
- Житлові будинки (Residential buildings)
- Громадські будівлі (Public buildings)
- Промислові об'єкти (Industrial facilities)
- Критична інфраструктура (Critical infrastructure)

### Volume Structure (14 Volumes)

**Volume 1:** Пояснювальна записка (Explanatory note)
**Volume 2:** Проєктні рішення (Project solutions)
**Volume 3-13:** Specialized sections (varies by project type)
**Volume 14:** Кошторисна документація (Cost estimates)

---

## 📊 Validation Process

### Automatic Detection

Agent automatically determines project type:
1. Check Volume 1 Section 2: "Загальна характеристика об'єкта"
2. If CC1/CC2/CC3 mentioned → Industrial (Додаток Е)
3. If unclear → Ask user: "Виробничий чи невиробничий об'єкт?"

### Validation Hierarchy

```
Validation:
├── Structure Check
│   ├── Load ДБН А.2.2-3:2014
│   ├── Determine Додаток Д або Е
│   ├── Extract required sections
│   └── Output checklist (✅ Present / ❌ Missing)
├── Reference Validation
│   ├── Parse format: "ДБН X.X.X-YYYY п.N.M"
│   ├── Verify standard exists
│   └── Check section exists
└── Compliance Report
    ├── Structure validation
    ├── Reference format check
    ├── Cross-reference validation
    └── Priority standards check
```

---

## 🔄 Future Enhancements

### Planned Agents (v1.1)

- **Volume 1 Writer** - Generate Volume 1 (Пояснювальна записка)
- **Volume 2 Writer** - Generate Volume 2 (Проєктні рішення)
- **CC1 Calculator** - Calculate CC1 consequence class per ДСТУ-Н Б В.1.2-16:2013

### Planned Workflows (v1.2)

- `generate-volume` - Automated volume generation
- `compliance-report` - Detailed compliance reporting
- `standard-update` - Track and update standards lifecycle

### Planned Standards (v1.3)

- **ДСТУ Family** - Additional Ukrainian state standards
- **ISO Family** - International standards (ISO 9001, ISO 27001)

---

## 🤝 Contributing

This module is developed for felectra organization projects. If you find issues or have suggestions:

1. Open issue in [krtm-dev](https://github.com/felectra/krtm-dev)
2. Tag with `pkd-module` label
3. Provide ДБН reference if applicable

---

## 📝 License

Module developed for internal felectra use. Standards content subject to Ukrainian government regulations.

---

## 🔗 Resources

- **ДБН Portal:** [e-construction.gov.ua](https://e-construction.gov.ua/)
- **ЄДЕССБ:** Unified database of building standards
- **KMU-373-2021:** [Cybersecurity requirements](https://zakon.rada.gov.ua/)

---

**Module Version:** 1.0.0
**Created:** 2025-11-17
**Maintained by:** @joyshmitz (felectra)
**Source Project:** krtm-dev (Beads issue: krtm-dev-e8c)
