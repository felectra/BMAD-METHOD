# IEC 62443 Series - Industrial Automation and Control Systems Security

**Status:** International Standard (Reference for KRTM)
**Organization:** IEC (International Electrotechnical Commission)
**Application in Ukraine:** Voluntary (best practice; КМУ 373 є обов'язковим)
**Latest updates:** 2018-2023 (series continuously updated)

## Series Overview

IEC 62443 - це серія стандартів для кібербезпеки промислових систем автоматизації та управління (IACS - Industrial Automation and Control Systems).

**Структура серії:**

- **IEC 62443-1-x:** Загальні концепції, терміни, метрики
- **IEC 62443-2-x:** Політики та процедури (для операторів)
- **IEC 62443-3-x:** Системні вимоги (проектування систем)
- **IEC 62443-4-x:** Вимоги до компонентів (пристрої, програми)

## Key Standards in Series

### IEC 62443-2-1: Security Program Requirements

- Створення програми кібербезпеки для IACS
- Оцінка ризиків
- Політики та процедури

### IEC 62443-3-3: System Security Requirements

- **Security Levels (SL):**
  - **SL1:** Захист від випадкових загроз
  - **SL2:** Захист від цілеспрямованих атак з обмеженими ресурсами (типово для KRTM)
  - **SL3:** Захист від складних атак з розширеними ресурсами
  - **SL4:** Захист від державних акторів (military-grade)

- **Foundational Requirements (FR):**
  - FR1: Identification and Authentication Control (IAC)
  - FR2: Use Control (UC)
  - FR3: System Integrity (SI)
  - FR4: Data Confidentiality (DC)
  - FR5: Restricted Data Flow (RDF)
  - FR6: Timely Response to Events (TRE)
  - FR7: Resource Availability (RA)

### IEC 62443-3-2: Security Risk Assessment

- Методологія оцінки ризиків для IACS
- Зонування (Zones and Conduits)
- Threat modeling

### IEC 62443-4-2: Technical Security Requirements for Components

- Вимоги до embedded devices (Edge Nodes, sensors, actuators)
- Secure development lifecycle
- Hardening вимоги

## Key Concepts

### Zones and Conduits Model

- **Zone** - логічне угруповання активів з подібними вимогами безпеки
  - Приклад для KRTM: Zone 1 (65 котелень), Zone 2 (ЦДП), Zone 3 (Internet DMZ)
- **Conduit** - канал зв'язку між зонами з контрольованим доступом
  - Приклад для KRTM: VPN-тунелі між котельнями та ЦДП

### Defense in Depth

Багаторівневий захист:

1. **Physical Security** - фізичний доступ до обладнання
2. **Network Security** - firewall, VPN, segmentation
3. **Host Security** - hardening, antivirus, patch management
4. **Application Security** - RBAC, input validation, logging
5. **Data Security** - encryption at rest and in transit

## KRTM Usage

**Target Security Level for KRTM: SL2**

Обґрунтування:

- Муніципальна критична інфраструктура (теплопостачання)
- Потенційні атаки з обмеженими ресурсами (скриптові атаки, ransomware)
- НЕ стратегічний об'єкт (military-grade SL3/SL4 не потрібен)

**Zones for KRTM:**

1. **Zone 1 (Field Level):** 65 котелень, датчики, лічильники
   - Security: Фізичний контроль доступу, Modbus RTU (не шифрований, але локальний)
2. **Zone 2 (Edge Level):** ThingsBoard IoT Gateway nodes
   - Security: VPN client, MQTT TLS, certificate auth
3. **Zone 3 (Control Level):** ThingsBoard ЦДП, бази даних
   - Security: Firewall, MFA, RBAC, centralized logging
4. **Zone 4 (Enterprise/DMZ):** External integrations (опціонально)
   - Security: DMZ firewall, reverse proxy

**Conduits for KRTM:**

- **C1:** Modbus RS-485 (котельня → Edge Node) - локальний, фізично захищений
- **C2:** VPN-тунелі (Edge Nodes → ЦДП) - encrypted, authenticated
- **C3:** HTTPS/API (диспетчерські станції → ThingsBoard) - TLS 1.3+, MFA

**Foundational Requirements Implementation:**

- **FR1 (IAC):** Унікальні токени/сертифікати для кожного Edge Node, MFA для диспетчерів
- **FR2 (UC):** RBAC в ThingsBoard (admin, dispatcher, operator, read-only)
- **FR3 (SI):** CIS hardening, automated updates, integrity monitoring
- **FR4 (DC):** TLS 1.3+ для MQTT, encryption at rest для баз даних (опціонально)
- **FR5 (RDF):** Firewall rules, network segmentation, VPN enforcement
- **FR6 (TRE):** Centralized logging, SIEM/Grafana alerts, incident response plan
- **FR7 (RA):** HA configuration для ЦДП, 7-day buffer на Edge Nodes, DDoS mitigation

## Compliance Notes

**For KRTM Project:**

- ✅ IEC 62443 - voluntary (best practice)
- ✅ КМУ 373 - обов'язковий (гармонізований з IEC 62443 SL2)
- ✅ Reference IEC 62443 в Section 6 (Cybersecurity) TZ

**Documentation:**

- Зонування (Zones and Conduits diagram) - у Section 6.2 TZ
- Security risk assessment - у IRP document
- Threat model - у Architecture Decision Record

## Official Source

- **IEC Webstore:** https://webstore.iec.ch/ (paid standards)
- **ISA/IEC 62443:** https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
- **Free overview:** ISA publications and whitepapers

## Cross-references

- КМУ № 373 - український equivalent (обов'язковий)
- ISO/IEC 27001 - IT security management (complementary)
- NIST Cybersecurity Framework - alternative framework (USA)
- IEC 60870-5-104 - telecontrol protocol (часто використовується з IEC 62443)

---

**Created:** 2025-11-11 15:10:00 EET
**Maintainer:** Mary (Business Analyst)
**KRTM Relevance:** HIGH (best practice reference; КМУ 373 обов'язковий)
**Target SL:** SL2 (для KRTM)
**Last verified:** 2025-11-11
