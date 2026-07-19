<!-- ====================================================================== -->
<!-- File: docs/36_AI_AGENT_OPERATION_GUIDE.md -->
<!-- ====================================================================== -->

# AI Agent Operation Guide

Version 2.0

Enterprise AI-Assisted Development Operations Documentation

---

# Purpose

This document defines how to effectively use AI coding agents such as GitHub Copilot Agent throughout the software development lifecycle.

The objectives are:

- Improve AI collaboration
- Maintain consistent development quality
- Reduce development errors
- Improve productivity
- Preserve project knowledge
- Enable continuous AI-assisted improvement

This guide is designed for:

- Developers
- Technical Leads
- Project Owners
- GitHub Copilot Agent Users
- AI-Assisted Development Teams

---

# AI Agent Philosophy

AI Agent is not a replacement for developers.

AI Agent acts as:

- Development Assistant
- Architecture Assistant
- Code Reviewer
- Testing Assistant
- Documentation Assistant
- Knowledge Management Assistant

Human developers remain responsible for:

- Final decisions
- Architecture approval
- Security approval
- Production deployment

---

# AI Agent Operating Model

```text
Human

↓

Requirement

↓

AI Analysis

↓

AI Recommendation

↓

Human Decision

↓

AI Implementation

↓

Human Review

↓

Release

AI Agent Working Principles
1. Understand Before Creating

AI Agent must:

Read project documentation
Understand architecture
Review existing code
Follow project rules
2. Follow Existing Patterns

AI Agent should:

Reuse existing components
Follow naming conventions
Maintain consistency
Avoid unnecessary redesign
3. Explain Important Decisions

AI Agent should explain:

Why this approach
Alternative options
Risks
Trade-offs
Required AI Context Files

Before development, AI Agent should read:

.github/

├── copilot-instructions.md

├── copilot-context.md

└── copilot-rules.md

and:

docs/

├── PROJECT_RULES.md

├── 30_AI_CONTEXT.md

├── 31_COPILOT_AGENT_GUIDE.md

├── 32_PROMPT_TEMPLATES.md

├── 33_SECURITY_GUIDE.md

├── 34_DEPLOYMENT_GUIDE.md

└── 35_DEVELOPMENT_WORKFLOW.md
AI Agent Initialization Process

When starting a task:

Load Context

↓

Understand Requirement

↓

Analyze Impact

↓

Create Plan

↓

Confirm Approach

↓

Implement
AI Agent First Prompt

Use:

You are the AI Development Agent for this project.

Before making changes:

1. Read repository instructions.
2. Understand architecture.
3. Review existing implementation.
4. Identify affected files.
5. Create implementation plan.

Do not modify code until the plan is clear.
Requirement Analysis Workflow
Step 1 — Understand Request

AI Agent should identify:

Business objective
User needs
Expected result
Constraints
Step 2 — Analyze Impact

Review:

Frontend
Backend
Database
API
Security
Testing
Documentation
Requirement Analysis Prompt
Analyze this requirement.

Requirement:

[DESCRIPTION]

Return:

Business Goal

User Impact

Affected Components

Required Changes

Risks

Implementation Plan
Development Workflow With AI Agent
Requirement

↓

Analysis

↓

Planning

↓

Code Generation

↓

Review

↓

Testing

↓

Documentation

↓

Release
AI Agent Code Generation Rules

Before generating code:

Check:

Existing architecture
File structure
Coding standards
Security rules
Performance requirements
Code Generation Prompt
Generate implementation.

Feature:

[FEATURE]

Follow:

Existing Architecture

Coding Standards

Security Rules

Performance Guidelines

Include:

Affected Files

Implementation Details

Testing Approach
AI Agent Code Review Process

AI Agent should review generated code.

Review:

Architecture
Correct location
Proper separation
Reusable design
Security
Validation
Authorization
Data protection
Performance
Efficiency
Resource usage
Scalability
Quality
Readability
Maintainability
Documentation
Code Review Prompt
Review this implementation.

Analyze:

Architecture

Security

Performance

Code Quality

Testing

Return:

Problems

Severity

Recommendation
AI Agent Testing Workflow

AI Agent should assist:

Test planning
Test case creation
Bug analysis
Regression testing
Testing Prompt
Create testing strategy.

Feature:

[FEATURE]

Include:

Unit Test

Integration Test

Security Test

Performance Test

UAT Scenario
AI Agent Debugging Workflow
Error

↓

Analyze

↓

Find Root Cause

↓

Recommend Fix

↓

Validate Solution
Debugging Prompt
Debug this issue.

Error:

[ERROR]

Context:

[DETAIL]

Analyze:

Root Cause

Affected Component

Solution

Prevention
AI Agent Security Workflow

AI Agent must always consider:

Authentication
Authorization
Input Validation
Data Protection
Secrets Management
Security Review Prompt
Perform security review.

Check:

Authentication

Authorization

Data Exposure

Input Validation

Secrets

Audit Logging

Return security recommendations.
AI Agent Documentation Workflow

Documentation should be updated when:

New feature created
Architecture changed
API changed
Business rule changed
Documentation Prompt
Update documentation.

Change:

[DESCRIPTION]

Update:

Architecture

Usage Guide

API

Configuration

Examples
AI Agent Decision Management

Important decisions should be recorded.

Architecture Decision Record Prompt
Create decision record.

Decision:

[DECISION]

Include:

Context

Options

Chosen Solution

Reason

Impact

Future Consideration
AI Agent Session Workflow

Recommended session:

1. Load Context

2. Explain Goal

3. Ask AI for Plan

4. Review Plan

5. Approve Implementation

6. Review Output

7. Test

8. Document
Prompt Engineering Guidelines

Good prompts include:

Context

Explain system background.

Objective

Define expected outcome.

Constraints

Specify rules.

Output Format

Define response structure.

Prompt Template
Context:

[PROJECT_CONTEXT]

Goal:

[OBJECTIVE]

Constraints:

[RULES]

Task:

[ACTION]

Expected Output:

[FORMAT]
AI Agent Collaboration Roles

AI Agent can simulate roles:

Software Architect

Focus:

Design
Trade-offs
Scalability
Backend Developer

Focus:

Logic
APIs
Data
Frontend Developer

Focus:

UI
UX
Components
QA Engineer

Focus:

Testing
Quality
Security Engineer

Focus:

Risks
Protection
Multi-Agent Review Prompt
Review this feature using multiple roles:

Software Architect

Backend Developer

Frontend Developer

QA Engineer

Security Engineer

Return combined recommendations.
AI Agent Knowledge Management

Project knowledge should be continuously updated.

Update:

AI Context
Rules
Architecture
Documentation
Prompt Library
Knowledge Update Workflow
New Knowledge

↓

Review

↓

Document

↓

Update Context

↓

Improve Future AI Work
AI Agent Performance Improvement

Measure:

Development speed
Error reduction
Code quality
Documentation quality
Reusable knowledge
AI Retrospective Prompt
Perform AI development retrospective.

Analyze:

What AI did well

What needs improvement

Common mistakes

Process improvements

Future recommendations
AI Agent Operation Checklist
Before Task
 Context loaded
 Requirement understood
 Architecture reviewed
 Rules checked
During Development
 Plan created
 Code reviewed
 Security considered
 Tests created
After Development
 Documentation updated
 Changes reviewed
 Knowledge updated
 Release prepared
AI Agent Best Practices

Always:

✓ Provide context

✓ Use structured prompts

✓ Review AI output

✓ Maintain documentation

✓ Combine AI and human judgment

✓ Improve prompts over time

Never:

✗ Accept output without review

✗ Allow uncontrolled changes

✗ Share secrets

✗ Ignore security

✗ Replace architecture decisions with AI guesses

AI Agent Quick Reference
Task	Recommended Action
New Feature	Analyze → Plan → Implement
Bug Fix	Diagnose → Fix → Test
Refactor	Review → Improve → Validate
Security	Analyze → Protect → Test
Deployment	Verify → Release → Monitor
Documentation	Update → Review → Maintain
End of AI Agent Operation Guide
