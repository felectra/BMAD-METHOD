# KRTM Standards Library

**Purpose:** Quick reference для всіх стандартів, що застосовуються в проєкті KRTM (Криворіжтепломережа Centralized Dispatch System).

**Owner:** Mary (Business Analyst)
**Created:** 2025-11-11 15:25:00 EET
**Last Updated:** 2025-11-11 15:25:00 EET

---

## 📋 Quick Navigation

### Ukrainian Building Standards (ДБН)

| Standard                                      | Title                                   | Status | KRTM Relevance                                    |
| --------------------------------------------- | --------------------------------------- | ------ | ------------------------------------------------- |
| [ДБН А.2.2-3:2014](dbn/DBN-A.2.2-3-2014.md)   | Склад та зміст проектної документації   | Діючий | ⭐ CRITICAL (основа структури томів)              |
| [ДБН В.1.1-7-2016](dbn/DBN-V.1.1-7-2016.md)   | Пожежна безпека                         | Діючий | ⭐ HIGH (обов'язковий розділ Том 2)               |
| [ДБН В.2.5-67:2013](dbn/DBN-V.2.5-67-2013.md) | Опалення, вентиляція та кондиціонування | Діючий | ⭐ CRITICAL (domain standard для теплопостачання) |
| [КМУ № 373 (2021)](dbn/KMU-373-2021.md)       | Кібербезпека критичної інфраструктури   | Діючий | ⭐ CRITICAL (може бути обов'язковим)              |

### Ukrainian Technical Standards (ДСТУ)

⚠️ **Зверніть увагу:** ДСТУ Б Д.1.1-1:2013 скасовано 01.11.2021 та замінено
НАСТАНОВА №281.

| Standard                                           | Title                                       | Status        | KRTM Relevance                             |
| -------------------------------------------------- | ------------------------------------------- | ------------- | ------------------------------------------ |
| [ДСТУ Б А.2.4-7:2009](dstu/DSTU-B-A.2.4-7-2009.md) | Основні вимоги до проектної документації    | Діючий        | ⭐ CRITICAL (оформлення томів і креслень)  |
| [ДСТУ Б Д.1.1-1:2013](dstu/DSTU-B-D.1.1-1-2013.md) | ~~Правила визначення вартості будівництва~~ | ❌ DEPRECATED | Скасовано 01.11.2021 (див. НАСТАНОВА №281) |

### GOST Standards (ЄСКД)

| Standard                                   | Title                 | Status | KRTM Relevance                                   |
| ------------------------------------------ | --------------------- | ------ | ------------------------------------------------ |
| [ГОСТ 2.104-2006](gost/GOST-2.104-2006.md) | Основні написи (ЄСКД) | Діючий | MEDIUM (reference; ДСТУ Б А.2.4-7 має пріоритет) |

### Методичні документи Мінрегіону (Настанови)

| Standard                                                 | Title                                            | Status | KRTM Relevance                  |
| -------------------------------------------------------- | ------------------------------------------------ | ------ | ------------------------------- |
| [НАСТАНОВА №281 (2021)](nastanova/NASTANOVA-281-2021.md) | Визначення вартості будівництва (з Змінами №1-4) | Діючий | ⭐ CRITICAL (Том 4 - кошториси) |

### International Standards (Reference)

| Standard                                                  | Title                           | Status    | KRTM Relevance                                 |
| --------------------------------------------------------- | ------------------------------- | --------- | ---------------------------------------------- |
| [IEC 62443 Series](international/IEC-62443-series.md)     | Industrial Cybersecurity        | Reference | ⭐ HIGH (best practice; КМУ 373 harmonized)    |
| [IEC 60870-5-104](international/IEC-60870-5-104.md)       | Telecontrol Protocol            | Reference | MEDIUM (interoperability; не primary protocol) |
| [ISO/IEC 27001:2022](international/ISO-IEC-27001-2022.md) | Information Security Management | Reference | ⭐ HIGH (self-assessment framework)            |

---

## 🗺️ Standards Matrix

Див. **[standards-matrix.md](standards-matrix.md)** для mapping стандартів до томів проєкту.

**Quick Overview:**

- **Том 1** (ЗПЗ): ДБН А.2.2-3, ДСТУ Б А.2.4-7
- **Том 2** (Основні рішення): ДБН В.1.1-7, ДБН В.2.5-67, КМУ 373, IEC 62443,
  ISO 27001
- **Том 3** (Креслення): ДСТУ Б А.2.4-7, ГОСТ 2.104
- **Том 4** (Кошториси): НАСТАНОВА №281 (2021) ⚠️
- **Том 5** (РД): ДСТУ Б А.2.4-7

---

## 📁 Directory Structure

```
pkd/00-metadata/standards/
├── README.md                    # Цей файл (index + navigation)
├── standards-matrix.md          # Tom X needs Standard Y mapping
├── TZ-Section-10-References.md  # TZ Section 10 reference document
├── dbn/                         # ДБН стандарти
│   ├── DBN-A.2.2-3-2014.md
│   ├── DBN-V.1.1-7-2016.md
│   ├── DBN-V.2.5-67-2013.md
│   └── KMU-373-2021.md
├── dstu/                        # ДСТУ стандарти
│   ├── DSTU-B-A.2.4-7-2009.md
│   └── DSTU-B-D.1.1-1-2013.md  (⚠️ DEPRECATED - скасовано 01.11.2021)
├── gost/                        # ГОСТ/ЄСКД стандарти
│   └── GOST-2.104-2006.md
├── nastanova/                   # Методичні документи Мінрегіону
│   ├── README.md
│   ├── NASTANOVA-281-2021.md
│   ├── compliance-matrix-tom4.md
│   └── amendments/
│       ├── Zmina-1-2022.md
│       ├── Zmina-2-2022.md
│       ├── Zmina-3-2023.md
│       └── Zmina-4-2024.md
└── international/               # International standards (reference)
    ├── IEC-62443-series.md
    ├── IEC-60870-5-104.md
    └── ISO-IEC-27001-2022.md
```

---

## 🎯 How to Use This Library

### For Team Members

**Scenario 1: "Який стандарт використовувати для креслень?"**
→ Перейти до [ДСТУ Б А.2.4-7:2009](dstu/DSTU-B-A.2.4-7-2009.md) → Section "KRTM Usage" → "Templates для KRTM"

**Scenario 2: "Які вимоги кібербезпеки?"**
→ Перейти до [КМУ № 373](dbn/KMU-373-2021.md) та [IEC 62443](international/IEC-62443-series.md)

**Scenario 3: "Як оформити титульну сторінку тому?"**
→ [ДСТУ Б А.2.4-7:2009](dstu/DSTU-B-A.2.4-7-2009.md) → Section "Templates to Extract" → `templates/title-page-template.md`

**Scenario 4: "Які стандарти для Том 2?"**
→ Перейти до [standards-matrix.md](standards-matrix.md) → Том 2

**Scenario 5: "Як створити кошториси для Том 4?"**
→ Перейти до [НАСТАНОВА №281 (2021)](nastanova/NASTANOVA-281-2021.md) →
Compliance matrix → Tom 3 BOM

### For Document Authors

При створенні тому:

1. Перевірити **standards-matrix.md** для списку relevant standards
2. Прочитати quick reference для кожного стандарту
3. Натиснути "Official Source" для full text (якщо потрібно)
4. Задокументувати compliance в розділі документу

---

## 🔍 Quality Criteria

Кожен standard quick reference містить:

- ✅ **Status:** Діючий/Скасований (verified on e-construction.gov.ua)
- ✅ **ЄДЕССБ Registration:** BN01:xxxx (for ДБН/ДСТУ)
- ✅ **Complete package:** Main doc + ALL attachments
- ✅ **Terminology extracted:** Official roles, positions, terms
- ✅ **KRTM Usage:** Які томи/розділи використовують цей standard
- ✅ **Cross-references:** Зв'язки з іншими standards
- ✅ **Official Source:** Links to full text

---

## 📚 Official Sources

### Primary Sources (Verified)

- **ЄДЕССБ Portal:** https://e-construction.gov.ua/ (ДБН/ДСТУ database)
- **Legislation Portal:** https://zakon.rada.gov.ua/ (ЗУ, КМУ)
- **Radnuk.com.ua:** https://radnuk.com.ua/ (кошторисні норми)

### International Standards (Paid)

- **IEC Webstore:** https://webstore.iec.ch/
- **ISO Webstore:** https://www.iso.org/store.html

---

## 🔄 Maintenance

**Update Frequency:**

- Review standards status: **Quarterly** (перевірка на e-construction.gov.ua)
- Add new standards: **As needed** (коли team виявляє нові requirements)
- Update KRTM usage notes: **Per Tom** (при створенні кожного тому)

**Owner:** Mary (Business Analyst)
**Review Team:** Winston (Lead), shmitz (PO)

---

## 📊 Statistics

**Total Standards Documented:** 11

- ДБН: 4
- ДСТУ: 2 (1 deprecated)
- ГОСТ: 1
- Настанови: 1 (NEW)
- International: 3

**Coverage by Tom:**

- Том 1: 2 standards
- Том 2: 5 standards
- Том 3: 2 standards
- Том 4: 2 standards (НАСТАНОВА №281 + ДБН А.2.2-3)
- Том 5: 1 standard

---

**Next Steps:**

1. ✅ Standards library created
2. ⏳ Create [standards-matrix.md](standards-matrix.md) (detailed Tom mapping)
3. ⏳ Extract templates to `../templates/` (title-page, drawing-stamp)
4. ⏳ Update TZ Section 10 with references

---

**Related Documents:**

- Master Plan: `pkd/00-metadata/master-plan-34-days.md` (Week 3 Mary на standards)
- Beads Issue: `krtm-z1k` (Звірка термінології та ролей)
- Input: `pkd/00-metadata/inputs/20251109-shmitz-cost-standards.md`

---

**Version:** 1.0.0
**Created:** 2025-11-11 15:25:00 EET
**Maintainer:** Mary (Business Analyst)
