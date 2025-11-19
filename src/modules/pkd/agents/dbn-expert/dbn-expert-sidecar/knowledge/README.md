# Maksym's Knowledge Base

This folder contains domain-specific ДБН standards for ПКД validation.

## Contents

**Symlinks to knowledge-base/** (will be created in Phase 11 - Post-Creation):

### ДБН Standards (7 files):

1. DBN-A.2.1-1-2014.md - Інженерні вишукування
2. DBN-A.2.2-3-2014.md - Структура та зміст ПКД ⭐⭐⭐ CORE
3. DBN-V.1.1-7-2016.md - Пожежна безпека
4. DBN-V.2.5-23-2010.md - Електрообладнання
5. DBN-V.2.5-39-2008.md - Теплові мережі, диспетчеризація
6. DBN-V.2.5-67-2013.md - Теплопостачання
7. KMU-373-2021.md - Кібербезпека критичної інфраструктури

### ДСТУ Standards (2 files):

8. DSTU-B-A.2.4-7-2009.md - Оформлення креслень
9. DSTU-N-B-V.1.2-16-2013.md - Клас CC1

### Reference Matrix (1 file):

10. standards-matrix.md - Tom × Standard mapping з priorities

**Total: 10 файлів**

---

## Usage

Agent loads these files during validation commands:

- `validate-structure` → DBN-A.2.2-3-2014.md
- `check-compliance` → All standards + matrix
- `check-reference` → Specific standard lookup
- `find-standard` → Full-text search across all files
- `list-requirements` → Specific standard + matrix

---

## Important

**Symlinks will be created AFTER agent YAML generation** (Phase 11 - Post-Creation Checklist).

See: DBN_EXPERT_CREATION_PLAN.md Phase 11 for symlink commands.
