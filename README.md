# Modeling and Analysis

A collection of five mini-projects demonstrating progressive object-oriented modeling concepts in Java - from basic OOP fundamentals through advanced inheritance patterns and UML constraints to database persistence with JPA/Hibernate.

Built as part of the **Modeling and Analysis of Information Systems (MAS)** course at the Polish-Japanese Academy of Information Technology (PJAIT).

## Mini-Projects Overview

### MP1 - Object Attributes & Extents

Covers foundational OOP attribute types and in-memory object management.

**Concepts demonstrated:**
- Required, optional, and repeatable attributes
- Composite attributes (`LocalDateTime`)
- Derived/calculated attributes (e.g., forbidden products based on allergies)
- Class-level (static) attributes and methods
- Extent management - tracking all instances of a class
- Object serialization and deserialization for persistence

### MP2 - Associations & Relationships

Models various types of object relationships with bidirectional synchronization.

**Concepts demonstrated:**
- Composition (whole–part): `Menu` → `MenuItem`
- Many-to-many with attributes: `Recipe` ↔ `Ingredient` (with quantity and unit)
- Many-to-many regular: `Recipe` ↔ `Equipment`
- Qualified association: `MenuItem` → `Recipe` (qualified by recipe name)
- Bidirectional association management

### MP3 - Advanced Inheritance Patterns

Explores non-trivial inheritance scenarios beyond standard single inheritance.

**Concepts demonstrated:**
- **Multiple inheritance** - `Amphibian` extends `Car` and implements `Sailable`, using delegation
- **Overlapping inheritance** - `Building` can simultaneously be `Residential` and/or `Commercial`, tracked via `EnumSet`
- **Dynamic inheritance** - `RentalSpace` can change its role at runtime between `Retail` and `Office`
- **Multiaspect inheritance** - `Record` hierarchy with `DigitalRecord` and `VinylRecord` subtypes, each with distinct attributes
- **Polymorphism** across all patterns

### MP4 - UML/OCL Constraints

Implements common UML relationship constraints in Java.

| Constraint | Example | Description |
|---|---|---|
| `{unique}` | `Player` | Enforces unique nicknames across all instances |
| `{subset}` | `Company` | Chairpersons must be a subset of stakeholders |
| `{ordered}` | `Bookshelf` | Books maintain insertion order |
| `{bag}` | `Olympics` ↔ `Sportsperson` | Allows duplicate, unordered entries |
| `{own}` | `Planner` | Exclusive ownership of events, no time overlaps |
| `{xor}` | `Citizen` | Either immunity or sentences, never both |
| Attribute constraint | `AirConditioner` | Temperature restricted to [18, 26] range |

### MP5 - JPA & Database Persistence

Maps object models to a relational database using Jakarta Persistence and Hibernate ORM.

**Concepts demonstrated:**
- Simple entity mapping with `@Entity`, `@Id`, `@GeneratedValue`
- One-to-many bidirectional relationships (`Driver` ↔ `Car`)
- Inheritance hierarchy persistence (`Record` → `DigitalRecord` / `VinylRecord`)
- JPQL queries for retrieving persisted entities
- Hibernate auto-schema generation

**Tech stack:** Maven, Hibernate 6, MySQL, JUnit 5

## Tech Stack

- **Language:** Java
- **Build:** Maven (MP5)
- **Persistence:** Hibernate 6 / Jakarta Persistence API (MP5)
- **Database:** MySQL (MP5)
- **Testing:** JUnit 5
- **Annotations:** JetBrains null-safety annotations
