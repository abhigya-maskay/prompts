# Adaptive Feature Development Workflow

## Phase 1: Feature Planning & Discovery
- **Epic/Feature Definition**: Define business value, stakeholder needs, and high-level scope
- **Feature Decomposition**: Break large features into smaller, manageable tasks that can be implemented incrementally
- **User Flow Mapping**: Map the user journey and identify all touchpoints for the feature
- **Progressive Elaboration**: Start with high-level requirements, refine details as understanding grows
- **Requirements Validation**: Ensure feature requirements are clear, testable, and aligned with project goals

### Decision Point 1: Complexity & Scope Assessment
**Evaluate feature complexity to determine workflow path:**

**- Simple Path** (Single file/component, no DB changes, no external deps)
- Skip to Phase 4: Detailed Code Design
- Reduced documentation requirements

**- Standard Path** (Multiple files, possible DB changes, standard integrations)
- Continue to Phase 2: Technical High-Level Planning

**- Complex Path** (Multiple systems, major DB changes, external integrations, performance implications)
- Continue to Phase 2 with enhanced risk assessment
- Additional validation checkpoints

## Phase 2: Technical High-Level Planning
- **Codebase Analysis**: Review existing architecture, patterns, and conventions in the project
- **Technical Decision Documentation**: Document key technical choices and their rationale
- **Non-functional Requirements**: Define performance, security, and maintainability requirements for the feature
- **Dependency Assessment**: Identify existing libraries, services, and APIs that will be used or affected
- **Risk & Impact Assessment**: Identify potential technical risks and impacts on existing functionality

### Decision Point 2: Risk Assessment
**Evaluate technical risks to determine additional phases needed:**

**High-Risk Factors Detected:**
- **Database Schema Changes** - Branch to Phase 2.1: Migration Planning
- **External API Integrations** - Branch to Phase 2.2: Integration Spike
- **Performance-Critical Code** - Branch to Phase 2.3: Performance Planning
- **Security-Sensitive Areas** - Branch to Phase 2.4: Security Review
- **Legacy System Modifications** - Branch to Phase 2.5: Legacy Analysis

**- Low Risk**: Continue to Phase 3: Code Unit Planning
**- High Risk**: Complete relevant risk-specific phases first

### Phase 2.1: Migration Planning *(If database changes detected)*
- **Schema Design**: Plan table structures, indexes, and constraints
- **Migration Strategy**: Design backward-compatible migration steps
- **Data Migration**: Plan data transformation and validation
- **Rollback Planning**: Design rollback strategy for failed migrations

### Phase 2.2: Integration Spike *(If external APIs involved)*
- **API Research**: Study external API documentation and limitations
- **Proof of Concept**: Build minimal integration to validate approach
- **Error Handling**: Plan for API failures, rate limits, and timeouts
- **Authentication**: Design secure API key management

### Phase 2.3: Performance Planning *(If performance-critical)*
- **Performance Requirements**: Define specific performance targets
- **Bottleneck Analysis**: Identify potential performance bottlenecks
- **Optimization Strategy**: Plan caching, indexing, and optimization approaches
- **Performance Testing**: Design performance test scenarios

### Phase 2.4: Security Review *(If security-sensitive)*
- **Threat Modeling**: Identify potential security threats and vulnerabilities
- **Access Control**: Design authentication and authorization requirements
- **Data Protection**: Plan encryption, sanitization, and secure storage
- **Security Testing**: Design security test scenarios

### Phase 2.5: Legacy Analysis *(If modifying legacy systems)*
- **Legacy Code Review**: Understand existing patterns and constraints
- **Impact Analysis**: Map all dependencies and side effects
- **Compatibility Planning**: Ensure new code works with legacy patterns
- **Gradual Migration**: Plan incremental modernization approach

## Phase 3: Code Unit Planning
- **Code Unit Identification**: Identify all functional units needed (services, endpoints, UI components, utilities, tests)
- **Responsibility Definition**: Define clear responsibilities and interfaces for each code unit
- **Integration Planning**: Plan how new code integrates with existing systems (APIs, database, external services)
- **Data Flow Design**: Map data transformations and storage requirements
- **Testing Strategy**: Define unit, integration, and end-to-end testing approach for the feature

## Phase 4: Detailed Code Design
- **API/Interface Design**: Define function signatures, class interfaces, and data contracts
- **Code Organization**: Plan file structure, module organization, and naming conventions
- **Database Design**: Design schema changes, migrations, and data access patterns
- **Error Handling Strategy**: Plan exception handling, validation, and user feedback mechanisms
- **Implementation Sequence**: Define the order of implementation to minimize blocking dependencies

## Phase 5: Implementation & Delivery
- **Incremental Development**: Implement in small, working increments following the planned sequence
- **Test-Driven Development**: Write tests alongside implementation to ensure quality
- **Code Integration**: Integrate new code with existing codebase following established patterns
- **Progressive Testing**: Unit → Integration → End-to-end testing as implementation progresses
- **Code Review & Refinement**: Self-review code for quality, performance, and maintainability

## Cross-Cutting Practices (Throughout All Phases)
- **Documentation as Code**: Keep design decisions and technical notes close to the code
- **Code Quality Standards**: Follow existing project conventions and maintain consistent style
- **Performance Awareness**: Consider performance implications of design and implementation choices
- **AI-Assisted Development**: Leverage AI tools for code generation, testing, and debugging while maintaining quality
- **Security Mindset**: Consider security implications throughout planning and implementation

## Notes
This workflow is designed for individual developers working on features within a single repository. It emphasizes thorough planning and incremental implementation while maintaining code quality and integration with existing systems. The workflow scales from small feature additions to large feature implementations or modifications to existing functionality.
