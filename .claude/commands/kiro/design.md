# Generate AI-Friendly Design Document

Second step in the Kiro workflow pipeline. Transforms structured requirements into a comprehensive technical design document that serves as the blueprint for implementation.

## Scope and Role

### Your Role

You are a software architect. Your responsibility is to create a detailed technical design based on the requirements document. Focus on HOW the system will be implemented, including architecture, components, data models, and technical decisions.

### Prerequisites

- A requirements.md file must exist in .kiro/specs/PROJECT_NAME/
- Read the requirements document thoroughly before generating the design

### Out of Scope

- **Task Breakdown**: Do not create development tasks or user stories
- **Code Implementation**: Focus on design, not actual code
- **Project Management**: No timelines, resource allocation, or sprint planning
- **Requirements Changes**: Do not modify or add requirements

The task breakdown phase (kiro-tasks.md) will handle work decomposition based on your design document.

## Process

1. **Read Requirements**: Load the requirements.md file from the project directory
2. **Analyze Requirements**: Understand all functional and non-functional requirements
3. **Design Architecture**: Create high-level architecture with components and data flow
4. **Define Components**: Detail each component's purpose, interfaces, and responsibilities
5. **Model Data**: Define data structures, schemas, and API contracts
6. **Plan Error Handling**: Design error scenarios and recovery strategies
7. **Consider Security**: Address authentication, authorization, and data protection
8. **Choose Technology**: Select appropriate languages, frameworks, and tools based on requirements
9. **Save Document**: Create .kiro/specs/PROJECT_NAME/design.md for the task phase

## Key Principles

- **Completeness**: Address every requirement with a technical solution
- **Modularity**: Design loosely coupled, highly cohesive components
- **Scalability**: Consider future growth and performance requirements
- **Maintainability**: Prioritize clear interfaces and separation of concerns
- **Security**: Apply security best practices and principle of least privilege
- **Testability**: Design for unit, integration, and end-to-end testing

## Output Template

````markdown
# Design Document

## Overview

[3-5 sentences describing the system architecture, key technology choices, and how the solution addresses the requirements]

## Architecture

### High-Level Architecture

```mermaid
[Architecture diagram showing components and data flow]
```

### Component Flow

[Numbered list describing the flow of data/control through the system]

## Components and Interfaces

### 1. [Component Name]

**File**: `path/to/component`

- **Purpose**: [Description]
- **Responsibilities**: [List key responsibilities]
- **Interfaces**: [Define public APIs/methods]

[Repeat for each major component]

## Data Models

### [Model Name]

```[language]
[Interface or schema definition in chosen language]
```

[Repeat for each data model]

## API Specifications

### [API Endpoint/Service]

- **Endpoint**: [Path or service name]
- **Method**: [HTTP method or RPC type]
- **Request**: [Request structure]
- **Response**: [Response structure]
- **Errors**: [Possible error conditions]

[Repeat for each API]

## Technology Stack

### Runtime and Languages

- **Primary Language**: [Language and version]
- **Runtime**: [Runtime environment]
- **Package Manager**: [Package management tool]

### Key Dependencies

- **[Category]**: [Library/framework] - [Purpose]
  [List major dependencies by category]

### Development Tools

- **Linting**: [Tool and configuration]
- **Testing**: [Testing framework]
- **Building**: [Build tool if applicable]

## Error Handling

### [Error Category]

- **Scenarios**: [When these errors occur]
- **Detection**: [How errors are detected]
- **Response**: [How system responds]
- **Recovery**: [Recovery mechanisms]

[Repeat for each error category]

## Security Considerations

### Authentication and Authorization

[Describe auth mechanisms and permission models]

### Data Protection

[Describe how sensitive data is handled]

### API Security

[Describe API security measures]

## Testing Strategy

### Unit Tests

[Describe unit testing approach and coverage goals]

### Integration Tests

[Describe integration testing approach]

### End-to-End Tests

[Describe E2E testing approach]

## Configuration

### Environment Variables

```
[List all environment variables with descriptions]
```

### Configuration Files

[Describe configuration file formats and locations]

## Deployment and Operations

### Deployment Architecture

[Describe how the system will be deployed]

### Monitoring and Logging

[Describe monitoring and logging strategies]

### Maintenance

[Describe maintenance considerations]
````
