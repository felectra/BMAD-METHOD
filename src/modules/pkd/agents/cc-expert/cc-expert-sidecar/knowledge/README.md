# CC Expert Knowledge Base

## Overview

This knowledge base contains the foundational standards and references for consequence class (CC1/CC2/CC3) calculation according to Ukrainian building codes.

## Contents

### Primary Standard

**DSTU-N-B-V.1.2-16-2013.md** (symlink)

- Full title: ДСТУ-Н Б В.1.2-16:2013 "Настанова щодо визначення класу наслідків (відповідальності)"
- Purpose: Defines methodology for calculating consequence class (CC1/CC2/CC3) and complexity category (I-V)
- Key sections:
  - Table 1: Classification thresholds (lines 46-59)
  - Table 2: α coefficients for area types (lines 82-94)
  - Table A.1: CC to Category mapping (lines 63-78)
  - Formula 5.1: N₃ = α × N₁ (lines 120-132)
  - Formula 5.2: Ф = с × Вс × m (lines 134-146)
  - Methodology: 6-step calculation process (lines 97-117)
  - Special cases: Підвищеної небезпеки, сейсмічні зони (lines 333-351)
  - Output format: Section 5 structure for Volume 1 (lines 307-329)

## Source Location

Primary standards are maintained in the project-wide knowledge base:

```
/Users/sd/github/krtm-dev/knowledge-base/dstu/
```

Files in this directory are **symlinks** to avoid duplication and ensure all agents reference the same authoritative source.

## Usage

When CC Expert loads, it reads:

1. `instructions.md` (calculation methodology, formulas, scope)
2. `memories.md` (session history, patterns, preferences)
3. `knowledge/DSTU-N-B-V.1.2-16-2013.md` (referenced standard)

The agent has **read-only access** to this knowledge base - it applies the standard but never modifies it.

## Updates

If the ДСТУ standard is updated:

1. Update the source file in `/knowledge-base/dstu/`
2. Symlink automatically reflects changes (no action needed in this directory)
3. Document version change in `memories.md`

## Related Standards

While CC Expert focuses on ДSТУ-Н Б В.1.2-16:2013, calculations may reference:

- ДБН А.2.2-3:2014 (PKD structure - where CC calculation appears)
- ДБН В.1.2-14:2009 (General safety principles)
- Ukrainian State Budget Law (for м.р.з.п. rates)

For questions about these standards, redirect to:

- **DBN Expert** (Maksym) - ДБН structure validation
- **Volume 1 Writer** - PKD document generation

## Scope Boundaries

**CC Expert handles:**

- ✅ Consequence class calculation (CC1/CC2/CC3)
- ✅ Complexity category determination (I-V)
- ✅ Formula application (5.1, 5.2)
- ✅ Report generation for Section 5

**CC Expert does NOT handle:**

- ❌ PKD structure validation → DBN Expert
- ❌ Volume generation → Volume Writers
- ❌ Cost estimation → Cost Estimator
- ❌ Standard modifications → Standards are read-only

## Language

All knowledge base content and agent communication is in **Ukrainian**.

---

**Maintained by:** CC Expert Agent
**Last updated:** 2025-11-18
**Version:** 1.0 (initial creation)
