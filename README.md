# JUnit TDD & Mockito Project

This repository is a solution to an assignment on the topic of **JUnit**, demonstrating the application of Test-Driven Development (TDD) practices, unit testing with JUnit 5, and the use of Mockito for creating mock objects.

## Project Description

The project is a Skills Management System that allows linking people with their professional skills, evaluating proficiency levels and work experience.

## Architecture

The project is built using a three-layer architecture:

- **Model Layer** - domain models (Person, Skill, SkillSet)
- **Repository Layer** - data access layer with in-memory implementation
- **Service Layer** - application business logic

## Main Components

### Models

- **Person** - represents a person with name, surname, and email
- **Skill** - represents a skill with name and domain
- **SkillSet** - links Person and Skill, contains proficiency level (1-10) and years of experience

### Repository

- **SkillSetRepository** (interface) - contract for data operations
- **InMemorySkillSetRepository** - in-memory storage implementation

### Service

- **SkillSetService** - business logic for skills management

## Testing

The project is fully covered with tests demonstrating various aspects of testing:

### Unit Tests for Models

- Testing equals() contract (reflexivity, symmetry, transitivity, consistency)
- Testing hashCode() contract (consistency, agreement with equals)
- Validation of business rules through isValid() method
- Rating calculation and determination of "good" skills

### Unit Tests for Repository

- CRUD operations (add, getAll, remove)
- Search by various criteria (by Person, by Skill, by combination)
- Handling "not found" cases

### Unit Tests for Service with Mockito

- Mocking dependencies (SkillSetRepository)
- Verifying interactions with mock objects
- Testing business logic in isolation
- Using verify() to check method calls

## Technologies

- **Java 21**
- **JUnit 5** (Jupiter) - testing framework
- **Mockito 5** - library for creating mock objects
- **Maven** - project build system

## Project Structure
```
src/
├── main/java/org/example/
│   ├── model/              # Domain models
│   ├── repository/         # Repository interfaces
│   │   └── impl/          # Repository implementations
│   └── service/           # Business logic
└── test/java/
    ├── model/             # Model tests
    ├── repository/impl/   # Repository tests
    └── service/           # Service tests (with Mockito)
```

## Key Concepts Demonstrated

1. **Test-Driven Development (TDD)** - development through testing
2. **Unit Testing** - isolated component testing
3. **Mocking** - using mock objects for test isolation
4. **Contract Testing** - testing equals() and hashCode() contracts
5. **Defensive Programming** - data validation and edge case handling

