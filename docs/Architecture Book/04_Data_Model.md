# Data Model

Data Model описывает логическую модель данных платформы «Лучера».

Документ определяет основные сущности системы, их взаимосвязи и правила организации данных.

Data Model основана на Domain Model Product Book и не зависит от конкретной системы управления базами данных.

---

# Назначение

Логическая модель данных используется для:

- проектирования базы данных;
- разработки Backend;
- проектирования API;
- построения интеллектуальных сервисов;
- обеспечения целостности данных.

---

# Основные группы сущностей

Модель данных разделена на несколько логических областей.

```text
Platform

Knowledge

Education

Practice

Professional Development

Career
```

Каждая область содержит собственные сущности и использует общую доменную модель.

---

# Platform

Platform содержит общие сущности платформы.

Основные сущности:

- User
- Role
- Organization
- Group
- Profile
- Notification
- File
- Search Query
- Audit Event

---

# Knowledge

Knowledge является центральной частью модели данных.

Основные сущности:

- Knowledge Asset
- Knowledge Asset Type
- Category
- Tag
- Source

Knowledge используется всеми пользовательскими модулями.

---

# Education

Education использует объекты базы знаний.

Основные сущности:

- Educational Program
- Learning Module
- Assignment
- Assessment
- Attempt
- Learning Progress

---

# Practice

Practice содержит сущности профессиональной деятельности.

Основные сущности:

- Professional Task
- Clinical Case
- Medical Image
- Professional Document
- Professional Situation
- Work Template

---

# Professional Development

Основные сущности:

- Competency
- Development Plan
- Educational Activity
- Accreditation
- Professional Portfolio

---

# Career

Основные сущности:

- Career Goal
- Career Opportunity
- Career Profile
- Career Path

---

# Общие принципы

## Единый идентификатор

Каждая сущность имеет собственный уникальный идентификатор.

---

## Версионность

Объекты базы знаний должны поддерживать хранение нескольких редакций.

---

## История изменений

Изменения значимых сущностей должны сохраняться.

---

## Связи

Связи между сущностями являются явными.

Использование неявных связей не допускается.

---

## Независимость

Каждая группа сущностей должна иметь минимальное количество зависимостей от остальных областей модели.

---

# Основные связи

```text
Organization
        │
        ▼
User
        │
        ▼
Learning Progress
        │
        ▼
Educational Program
        │
        ▼
Knowledge Asset
        │
 ┌──────┼─────────┐
 ▼      ▼         ▼
Category Tag   Source
        │
        ▼
Clinical Case
        │
        ▼
Professional Document
        │
        ▼
Competency
        │
        ▼
Professional Portfolio
        │
        ▼
Career Goal
```

---

# Правила развития модели

При добавлении новых сущностей необходимо соблюдать следующие требования.

- новая сущность должна относиться к существующей логической области;
- повторное использование существующих сущностей предпочтительнее создания новых;
- изменения не должны нарушать совместимость существующей модели;
- связи должны оставаться явными.

---

# Связь с документацией

Data Model используется при разработке:

- Backend Architecture;
- API Architecture;
- AI Architecture;
- Database Design.

Domain Model Product Book является единственным источником предметной модели.

Data Model является технической интерпретацией Domain Model.