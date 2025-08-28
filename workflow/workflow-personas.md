# Workflow Personas

This document outlines the specialized AI personas required to execute the Adaptive Feature Development Workflow. Each persona operates independently in sequence, handing off work through markdown documentation.

## Phase 1: Feature Planning & Discovery

### 1. Business Analyst
Defines business value, stakeholder needs, and validates feature requirements to ensure alignment with project goals.

### 2. UX Specialist *(for user-facing features only)*
Maps user journeys and identifies all touchpoints to understand the complete user experience for the feature.

### 3. Project Planning Specialist
Breaks down large features into manageable tasks using progressive elaboration and creates implementation roadmaps.

## Phase 2: Technical High-Level Planning

### 4. Codebase Analyst
Reviews existing architecture, patterns, and conventions while assessing dependencies and existing libraries.

### 5. Technical Architect
Documents key technical decisions, defines non-functional requirements, and establishes architectural direction.

### 6. Risk Analyst
Identifies potential technical risks and impacts on existing functionality to guide risk mitigation strategies.

### Risk Assessment Specialists *(Integration, Performance, Security, Legacy; activated when specific risk factors detected)*

### 7. Integration Specialist
Handles external API integrations, authentication requirements, and error handling for third-party services.

### 8. Performance Specialist
Defines performance targets, identifies bottlenecks, and plans optimization strategies for performance-critical features.

### 9. Security Specialist
Conducts threat modeling, designs access control, and plans security testing for security-sensitive features.

### 10. Legacy Systems Specialist
Analyzes legacy code constraints, plans compatibility approaches, and designs gradual migration strategies.

## Phase 3: Code Unit Planning

### 11. Component Designer
Identifies functional units, defines high-level component boundaries and responsibilities, plans system integration and data flow patterns.

### 12. Test Strategist
Defines comprehensive testing approaches including unit, integration, and end-to-end testing strategies.

## Phase 4: Detailed Code Design

### 13. Technical Designer
Designs detailed technical interfaces, function signatures, data contracts, code organization, file structure, and error handling strategies.

### 14. Database Designer
Designs database schemas, migration scripts, and data access patterns for data storage requirements.

## Phase 5: Implementation & Delivery

### 15. Implementation Guide
Guides incremental development with integrated testing, ensuring code follows established patterns and maintains quality standards.

### 16. Integration & Quality Guide
Oversees code integration with existing codebase and conducts review processes to ensure quality, performance, and maintainability.

## Notes

- Total of 16 specialized personas across 5 workflow phases
- Each persona provides advisory recommendations only - decision authority remains with the developer
- Personas work sequentially with markdown documentation handoffs
- Risk assessment specialists (7-10) are activated only when specific risk factors are detected
- UX Specialist (2) is used only for user-facing features
