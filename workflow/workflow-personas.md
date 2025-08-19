# Workflow Personas

This document outlines the specialized AI personas required to execute the Adaptive Feature Development Workflow. Each persona operates independently in sequence, handing off work through markdown documentation.

## Phase 1: Feature Planning & Discovery

### 1. Business Analyst
Defines business value, stakeholder needs, and validates feature requirements to ensure alignment with project goals.

### 2. UX Specialist
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

### 7. Database Specialist (Phase 2.1)
Plans database schema changes, migration strategies, and data transformation requirements for database-related features.

### 8. Integration Specialist (Phase 2.2)
Handles external API integrations, authentication requirements, and error handling for third-party services.

### 9. Performance Specialist (Phase 2.3)
Defines performance targets, identifies bottlenecks, and plans optimization strategies for performance-critical features.

### 10. Security Specialist (Phase 2.4)
Conducts threat modeling, designs access control, and plans security testing for security-sensitive features.

### 11. Legacy Systems Specialist (Phase 2.5)
Analyzes legacy code constraints, plans compatibility approaches, and designs gradual migration strategies.

## Phase 3-4: Code Planning & Design

### 12. System Designer
Identifies code units, defines responsibilities, plans integration approaches, and designs data flow patterns.

### 13. Interface Designer
Designs APIs, function signatures, code organization, file structure, and error handling strategies.

### 14. Test Strategist
Defines comprehensive testing approaches including unit, integration, and end-to-end testing strategies.

### 15. Database Designer
Designs database schemas, migration scripts, and data access patterns for data storage requirements.

## Phase 5: Implementation & Delivery

### 16. Development Guide
Guides incremental development practices and integration with existing codebase following established patterns.

### 17. Testing Guide
Implements test-driven development approaches and oversees progressive testing from unit to end-to-end levels.

### 18. Quality Assurance Guide
Conducts code review processes and refinement activities to ensure quality, performance, and maintainability.

## Notes

- Total of 18 specialized personas across 5 workflow phases
- Each persona provides advisory recommendations only - decision authority remains with the developer
- Personas work sequentially with markdown documentation handoffs
- Specialized sub-phase personas (7-11) are activated only when specific risk factors are detected