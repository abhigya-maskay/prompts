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

### Risk Assessment Specialists *(activated when specific risk factors detected)*

### 7. Database Specialist
Plans database schema changes, migration strategies, and data transformation requirements for database-related features.

### 8. Integration Specialist
Handles external API integrations, authentication requirements, and error handling for third-party services.

### 9. Performance Specialist
Defines performance targets, identifies bottlenecks, and plans optimization strategies for performance-critical features.

### 10. Security Specialist
Conducts threat modeling, designs access control, and plans security testing for security-sensitive features.

### 11. Legacy Systems Specialist
Analyzes legacy code constraints, plans compatibility approaches, and designs gradual migration strategies.

## Phase 3: Code Unit Planning

### 12. Component Designer
Identifies functional units, defines high-level component boundaries and responsibilities, plans system integration and data flow patterns.

### 13. Test Strategist
Defines comprehensive testing approaches including unit, integration, and end-to-end testing strategies.

## Phase 4: Detailed Code Design

### 14. Technical Designer
Designs detailed technical interfaces, function signatures, data contracts, code organization, file structure, and error handling strategies.

### 15. Database Designer
Designs database schemas, migration scripts, and data access patterns for data storage requirements.

## Phase 5: Implementation & Delivery

### 16. Implementation Guide
Guides incremental development with integrated testing, ensuring code follows established patterns and maintains quality standards.

### 17. Integration & Quality Guide
Oversees code integration with existing codebase and conducts review processes to ensure quality, performance, and maintainability.

## Notes

- Total of 17 specialized personas across 5 workflow phases
- Each persona provides advisory recommendations only - decision authority remains with the developer
- Personas work sequentially with markdown documentation handoffs
- Risk assessment specialists (7-11) are activated only when specific risk factors are detected
- UX Specialist (2) is used only for user-facing features