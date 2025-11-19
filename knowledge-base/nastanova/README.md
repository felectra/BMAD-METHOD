# Настанови Мінрегіону - Consolidated Index

**Category:** Методичні документи Міністерства розвитку громад та територій
України
**Scope:** Кошторисні норми та правила визначення вартості будівництва

---

## Документи у цій директорії

### 1. НАСТАНОВА №281 (2021) - Визначення вартості будівництва

**Файл:** [NASTANOVA-281-2021.md](NASTANOVA-281-2021.md)

**Status:** ✅ Діючий з 2021-11-01
**Офіційна назва:** "Настанова з визначення вартості будівництва"
**Наказ Мінрегіону:** № 281 від 01.11.2021

**Заміняє:** ДСТУ Б Д.1.1-1:2013 (скасовано)

**Зміни (Amendments):**

- ✅ Зміна №1 - Наказ № 67 від 30.04.2022
- ✅ Зміна №2 - Наказ № 244 від 01.12.2022
- ✅ Зміна №3 - Наказ № 854 від 22.09.2023
- ✅ Зміна №4 - Наказ № 243 від 20.03.2024

**KRTM Usage:** ⭐ CRITICAL - Основа для Том 4 (Кошториси)

**Основні розділи:**

- Локальні кошториси (Section 3)
- Об'єктні кошториси (Section 4)
- Зведений кошторисний розрахунок (Section 5)
- Коефіцієнти та індекси (Section 6, оновлено Змінами)

---

## Compliance Matrix

**Файл:** [compliance-matrix-tom4.md](compliance-matrix-tom4.md)

**Purpose:** Трасування вимог НАСТАНОВА №281 до розділів Том 4 (Кошториси)

**Mapping:**

- НАСТАНОВА Section → Том 4 Section
- Amendments №1-4 → Application points
- Tom 3 BOM integration (18.3M UAH база)

**Status:** PENDING (очікування документів від shmitz)

---

## Amendments (Зміни)

Детальна документація кожної зміни зберігається у директорії `amendments/`:

### Зміна №1 (30.04.2022)

**Файл:** [amendments/Zmina-1-2022.md](amendments/Zmina-1-2022.md) (pending)

**Що оновлено:**

- Регіональні коефіцієнти
- Коригування на інфляцію 2022 року

### Зміна №2 (01.12.2022)

**Файл:** [amendments/Zmina-2-2022.md](amendments/Zmina-2-2022.md) (pending)

**Що оновлено:**

- Розцінки на матеріали (воєнний час)
- Коефіцієнти для воєнного стану

### Зміна №3 (22.09.2023)

**Файл:** [amendments/Zmina-3-2023.md](amendments/Zmina-3-2023.md) (pending)

**Що оновлено:**

- Розцінки на електротехнічні роботи
- Коефіцієнти для IT-обладнання

### Зміна №4 (20.03.2024)

**Файл:** [amendments/Zmina-4-2024.md](amendments/Zmina-4-2024.md) (pending)

**Що оновлено:**

- Актуалізація розцінок 2024 року
- Коефіцієнти для Дніпропетровської області

**Note:** Файли Змін будуть створені після отримання документів від shmitz.

---

## KRTM Project Integration

### Том 4 Структура (базується на НАСТАНОВА №281)

**Директорія:** `pkd/05-koshtorysy/`

**Розділи:**

1. **5.1 Локальні кошториси** (НАСТАНОВА Section 3)
   - Типовий Edge Node (обладнання, монтаж, ПНР)
   - Множення × 65 котелень
   - ЦДП (сервери, мережа, UPS, Frigate NVR)

2. **5.2 Об'єктний кошторис** (НАСТАНОВА Section 4)
   - Зведення всіх локальних кошторисів
   - ЦДП + 65 Edge Nodes

3. **5.3 Зведений кошторисний розрахунок** (НАСТАНОВА Section 5)
   - Загальна вартість будівництва системи
   - Верифікація: сума локальних = об'єктний = зведений

### База для розрахунків

**Tom 3 Consolidated BOM:**

- **Файл:** `pkd/04-specyfikatsii/4.6-consolidated-bom.md`
- **Вартість обладнання:** 18,342,726 грн з ПДВ

**До вартості обладнання додати:**

- Монтажні роботи (%)
- ПНР (%)
- Накладні витрати (коефіцієнт)
- Плановий прибуток (коефіцієнт)
- ПДВ (якщо не включено)

---

## Timeline (KRTM Project)

**Тиждень 1-2 (10-21.11.2025):**

- [x] Створити структуру nastanova/ (Mary)
- [x] Документувати НАСТАНОВА №281 (quick reference)
- [x] Створити compliance matrix
- [ ] Отримати документи від shmitz (БЛОКЕР)
- [ ] Вивчити методику кошторисування
- [ ] Підготувати шаблони

**Тиждень 3 (24-30.11.2025):**

- [ ] Створити Том 4 (Mary)
- [ ] Розрахувати вартість будівництва
- [ ] Верифікація compliance

---

## Official Sources

- **Законодавча база:** <https://zakon.rada.gov.ua/>
- **Кошторисні норми:**
  <https://radnuk.com.ua/pravova-baza/koshtorysni-normy-ukrainy-nastanova-z-vyznachennia-vartosti-budivnytstva-z-urakhuvanniam-zmin-1-2-3-4/>
- **ЄДЕССБ портал:** <https://e-construction.gov.ua/>

---

## Cross-references

**Standards Library:**

- Parent: [standards/README.md](../README.md)
- Deprecated: [dstu/DSTU-B-D.1.1-1-2013.md](../dstu/DSTU-B-D.1.1-1-2013.md)
- Related: [dbn/DBN-A.2.2-3-2014.md](../dbn/DBN-A.2.2-3-2014.md) (structure
  для Том 4)

**Project Documents:**

- Том 4: [pkd/05-koshtorysy/README.md](../../../05-koshtorysy/README.md)
- Tom 3 BOM: [pkd/04-specyfikatsii/4.6-consolidated-bom.md](../../../04-specyfikatsii/4.6-consolidated-bom.md)
- Input: [pkd/00-metadata/inputs/20251109-shmitz-cost-standards.md](../../inputs/20251109-shmitz-cost-standards.md)

---

**Created:** 2025-11-12 16:00:00 EET
**Maintainer:** Mary (Business Analyst)
**Last updated:** 2025-11-12
**Status:** Структура створена, очікування документів від shmitz
