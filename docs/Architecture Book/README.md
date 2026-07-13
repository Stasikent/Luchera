# Architecture Book «Лучера»

> **Техническая архитектура единой цифровой экосистемы сопровождения специалистов лучевой диагностики.**

Architecture Book является продолжением Product Book.

Если Product Book отвечает на вопрос **«Что мы строим?»**, то Architecture Book отвечает на вопрос **«Как мы будем это строить?»**.

Документ определяет технические принципы реализации платформы, организацию компонентов системы, взаимодействие модулей и правила разработки.

Architecture Book предназначен для:

- архитекторов;
- backend-разработчиков;
- frontend-разработчиков;
- ML/AI-разработчиков;
- DevOps-инженеров;
- тестировщиков;
- новых участников команды.

---

# Связь с Product Book

Architecture Book реализует архитектурные решения, основанные на Product Book.

```text
Product Book
      │
      ▼
Architecture Book
      │
      ▼
Implementation
```

Product Book определяет требования к продукту.

Architecture Book определяет способы их реализации.

Изменения архитектуры не должны противоречить:

- миссии продукта;
- принципам платформы;
- доменной модели;
- пользовательским сценариям;
- функциональным требованиям.

---

# Статус

Architecture Book разрабатывается после завершения Product Book v1.0.

На текущий момент документ определяет:

- архитектурные принципы;
- общую архитектуру системы;
- технологический стек;
- логическую модель данных;
- архитектуру приложения;
- архитектуру API;
- архитектуру интеллектуальной подсистемы;
- архитектуру пользовательского интерфейса;
- инфраструктуру;
- безопасность;
- процесс разработки.

---

# Структура

## Часть I. Архитектурные основы

Определяет фундаментальные технические решения платформы.

- [01 Architecture Principles](01_Architecture_Principles.md)
- [02 System Architecture](02_System_Architecture.md)
- [03 Technology Stack](03_Technology_Stack.md)

---

## Часть II. Архитектура данных и приложения

Описывает внутреннее устройство платформы.

- [04 Data Model](04_Data_Model.md)
- [05 Database Design](05_Database_Design.md)
- [06 Application Architecture](06_Application_Architecture.md)
- [07 API Architecture](07_API_Architecture.md)
- [08 Intelligence Architecture](08_Intelligence_Architecture.md)
- [09 Frontend Architecture](09_Frontend_Architecture.md)

---

## Часть III. Эксплуатация

Определяет правила эксплуатации и сопровождения платформы.

- [10 Deployment](10_Deployment.md)
- [11 Security Architecture](11_Security_Architecture.md)
- [12 Development Workflow](12_Development_Workflow.md)

---

# Архитектурные принципы

При проектировании платформы используются следующие принципы:

- Domain First;
- Module First;
- Shared Knowledge;
- Loose Coupling;
- High Cohesion;
- Evolutionary Architecture;
- Technology Independence;
- API First;
- Security by Design;
- Observability;
- Simplicity.

---

# Общая архитектура

```text
                     Platform
                         │
                         ▼
                    Knowledge
               ┌────────┴────────┐
               ▼                 ▼
         Education          Practice
               └────────┬────────┘
                        ▼
      Professional Development
                        ▼
                     Career
```

Platform предоставляет общие сервисы.

Knowledge является центральным модулем платформы.

Все остальные пользовательские модули используют общую доменную модель и единую базу знаний.

---

# Документация проекта

Полная документация включает:

- Product Book;
- Architecture Book;
- Use Cases;
- Functional Requirements;
- Decision Log;
- Architecture Decision Records (ADR);
- Glossary;
- Style Guide.

Все документы должны использовать единую терминологию и оставаться согласованными между собой.

---

# Развитие архитектуры

Архитектура развивается эволюционно.

Значимые технические решения фиксируются в ADR.

Изменения архитектуры сопровождаются обновлением соответствующих разделов Architecture Book.

---

# Следующий этап

После завершения Architecture Book начинается реализация MVP.

При разработке должны соблюдаться:

- Product Book;
- Architecture Book;
- Decision Log;
- ADR;
- Style Guide.

---

> **Architecture Book является единым источником технической архитектуры платформы «Лучера» и определяет принципы её реализации.**