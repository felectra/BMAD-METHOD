# CC Expert's Memory Bank

## User Preferences

**User:** Serhii
**Interaction Style:** (to be populated during first interaction)

## Project Context

**Current Project:** (to be set during first calculation)
**Project Type:** (CC1/CC2/CC3 - to be determined)
**Domain:** (to be identified - житловий/виробничий/громадський)

## Session History

### Template for Session Records

```
### [Date] Session N - [Brief Description]

**Завдання:** [What calculation was requested]

**Вхідні дані:**
- N₁: [value] осіб
- N₂: [value] осіб
- Вс: [value] тис. грн.
- Функціональне призначення: [спальний/громадський/виробничий/прибережний]
- α коефіцієнт: [value]
- с коефіцієнт: [value]
- m коефіцієнт: [value]

**Розрахунки:**
- N₃ = α × N₁ = [calculation]
- Ф = с × Вс × m = [calculation]
- Ф (м.р.з.п.) = [conversion]

**Результат:**
| Характеристика | Значення | Клас |
|----------------|----------|------|
| N₁ | [value] | CC[X] |
| N₂ | [value] | CC[X] |
| N₃ | [value] | CC[X] |
| Ф | [value] м.р.з.п. | CC[X] |
| Культурна спадщина | [оцінка] | CC[X] |
| Транспорт | [оцінка] | CC[X] |

**Фінальний клас:** CC[X] (консервативний підхід - найвища характеристика)
**Категорія складності:** [I/II/III/IV/V]

**Edge cases encountered:** (if any)
- [describe any special cases, threshold boundaries, etc.]

**Feedback від користувача:** (if any)
> [user quotes]

**Lessons learned:**
- [insights from this calculation]
```

---

## Calculation Patterns

### Pattern #1: (to be populated with repeated calculation scenarios)

**Context:** (project type, typical parameters)
**Common coefficients:** (α, с, m values for this pattern)
**Typical result:** (CC class range)
**Special considerations:** (edge cases specific to this pattern)

---

## ДСТУ Insights

### Practical Notes from Standard Application

**Threshold Awareness:**

- N₁ = 50 осіб → critical CC1/CC2 boundary
- N₁ = 400 осіб → critical CC2/CC3 boundary
- Ф = 2000 м.р.з.п. → CC1/CC2 economic boundary
- Ф = 150000 м.р.з.п. → CC2/CC3 economic boundary

**Conservative Approach Examples:**

- When N₁ = 48-52 → recommend verifying occupancy calculations
- When Ф near threshold → suggest sensitivity analysis
- When multiple characteristics yield different classes → always choose highest

**Coefficient Selection Patterns:**

- α = 1.0 (виробничі) most common for industrial projects
- α = 1.5 (спальні) for residential areas
- α = 2.5 (громадські) for public centers
- α = 3.0 (прибережні) rare, requires specific location justification

**Common с coefficient justifications:**

- с = 0.45 (ДСТУ standard recommendation) - most common
- с = 0.30-0.40 when partial damage scenario justified
- с = 0.225 minimum (requires strong engineering justification)

**m coefficient patterns:**

- m = 1.0 for new construction (standard)
- m < 1.0 for existing buildings (requires depreciation analysis)

---

## Special Cases Encountered

### Case Log Template

```
**Case:** [Brief description]
**Date:** [YYYY-MM-DD]
**Project:** [Project name]
**Issue:** [What made this special/edge case]
**Resolution:** [How it was handled]
**ДСТУ Reference:** [Relevant standard section]
**Lesson:** [What to remember for future]
```

---

## User-Specific Preferences

### Calculation Preferences

- Preferred output format: (table/detailed/summary)
- Coefficient conservativeness: (standard/conservative/optimistic)
- Level of detail in justifications: (brief/detailed)

### Report Preferences

- Report language: Ukrainian (default)
- Include formulas: (yes/no)
- Include ДСТУ references: (yes/no)
- Save reports to: {project-root}/pkd/00-metadata/

---

## Quick Reference

### Most Common Calculations

**KRTM Project Example:**

- Type: Виробничий об'єкт (industrial infrastructure)
- N₁: 30 осіб (operators/staff)
- N₂: 15 осіб (50% of N₁ typical for industrial)
- α: 1.0 (виробнича зона)
- N₃: 30 осіб (α × N₁)
- Вс: 2500 тис. грн.
- с: 0.45 (ДСТУ standard)
- m: 1.0 (new construction)
- Ф: 1125 тис. грн. ≈ 450 м.р.з.п.
- Result: CC1 (all characteristics below CC2 threshold)
- Category: II (CC1 → I or II per Table A.1)

### м.р.з.п. Rates (Historical Reference)

- 2025: [to be updated from budget law]
- 2024: 7100 грн. (approximate - verify current)
- 2023: 6700 грн. (approximate - verify current)

**NOTE:** Always verify current м.р.з.п. rate from latest Ukrainian State Budget Law before conversion.

---

## Personal Notes

### Observations About ДSТУ-Н Б В.1.2-16:2013

**Strengths:**

- Clear classification tables (Table 1, Table A.1)
- Explicit formulas (5.1, 5.2)
- Conservative principle codified (choose highest class)

**Ambiguities to watch:**

- N₂ calculation not explicitly defined (typically 30-50% of N₁, but depends on object type)
- Cultural heritage "significance" (місцевого vs національного) - subjective without clear criteria
- Transport impact assessment - requires context about infrastructure criticality

**Common User Questions:**

- "How to determine N₂?" → Depends on object: residential ~50%, industrial ~30-40%, public ~70-80%
- "Which α coefficient for mixed-use?" → Choose highest (conservative), or weighted average if justified
- "м.р.з.п. rate source?" → State Budget Law, updated annually

**Integration with Other Standards:**

- ДБН А.2.2-3:2014 → CC calculation goes in Том 1 Розділ 5
- ДБН В.1.2-14:2009 → General safety principles (referenced by ДСТУ)
- КМУ № 373/2021 → Critical infrastructure may trigger CC3 automatically

---

## Continuous Improvement

### Areas to Enhance

**Calculation Accuracy:**

- Build library of validated calculation examples
- Document edge cases and their resolutions
- Track coefficient justification patterns

**User Experience:**

- Refine interactive mode explanations based on feedback
- Improve scenario comparison clarity
- Optimize report format for PKD integration

**Knowledge Base:**

- Keep м.р.з.п. rates current
- Track standard updates/amendments
- Document integration patterns with other ДБН standards
