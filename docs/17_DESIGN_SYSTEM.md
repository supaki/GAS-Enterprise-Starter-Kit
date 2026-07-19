<!-- ====================================================================== -->
<!-- File: docs/17_DESIGN_SYSTEM.md -->
<!-- ====================================================================== -->

# Design System

Version 2.0

---

# Purpose

This document defines the design system standard for creating modern SaaS-level user interfaces.

The objective is to ensure:

- Consistent visual identity
- Professional UI quality
- Reusable components
- Faster development
- Better user experience

---

# Design Philosophy

The application follows:

- Modern SaaS Design
- Minimal Interface
- Clean Layout
- Data First Approach
- Responsive Everywhere

---

# Design Principles

## 1. Consistency

All pages must use:

- Same spacing
- Same typography
- Same components
- Same interaction patterns

---

## 2. Simplicity

Avoid:

- Unnecessary decoration
- Complex navigation
- Overloaded screens

---

## 3. User Focus

Every screen must answer:

```
What is important?

What action should user take?
```

---

# UI Architecture

```text
Application

↓

Layout System

↓

Page

↓

Section

↓

Component

↓

Element
```

---

# Design Tokens

Design tokens are reusable UI values.

Example:

```javascript
const DESIGN = {

spacing:{
small:"8px",
medium:"16px",
large:"24px"
},

radius:{
card:"16px",
button:"12px"
}

}
```

---

# Color System

## Primary Color

Used for:

- Main buttons
- Active states
- Links

Example:

```
Primary

Blue
```

---

## Secondary Color

Used for:

- Supporting actions
- Information

---

## Status Colors

| Status | Usage |
|-|-|
| Success | Completed |
| Warning | Attention |
| Error | Failed |
| Info | Information |

---

# Dark Mode

All components must support:

```
Light Mode

Dark Mode
```

---

Example:

```html
<div
class="
bg-white
dark:bg-gray-900
text-gray-900
dark:text-white
">

Content

</div>
```

---

# Typography System

Recommended:

Font:

```
Inter
```

Fallback:

```
system-ui
```

---

# Font Scale

| Type | Size |
|-|-|
| Heading 1 | 32px |
| Heading 2 | 24px |
| Heading 3 | 20px |
| Body | 16px |
| Small | 14px |

---

# Text Rules

Use:

- Short sentences
- Clear labels
- Action verbs

Avoid:

- Technical wording for users
- Long paragraphs

---

# Spacing System

Use 8px rule.

Example:

```
4px

8px

16px

24px

32px

48px
```

---

# Layout System

Standard:

```
Sidebar

+

Main Content
```

Example:

```text
--------------------------------

Sidebar

        Header

        Content

        Footer

--------------------------------
```

---

# Container Rules

Desktop:

```
max-width:
1280px
```

Mobile:

```
100%
```

---

# Card Design

Standard Card:

```text
------------------

Icon

Title

Value

Description

Action

------------------
```

---

Example:

Dashboard KPI:

```
Total Users

12,540

+15%
```

---

# Border Radius

Recommended:

| Component | Radius |
|-|-|
| Button | 12px |
| Card | 16px |
| Modal | 20px |
| Input | 12px |

---

# Shadow System

Use subtle shadows.

Example:

```
shadow-sm

shadow-md

shadow-lg
```

Avoid heavy shadows.

---

# Button System

## Primary

Main action.

Example:

```
Save
Create
Submit
```

---

## Secondary

Alternative.

Example:

```
Cancel
Back
```

---

## Danger

Destructive action.

Example:

```
Delete
Remove
```

---

# Form Design

Every input requires:

- Label
- Placeholder
- Validation
- Error message

---

Example:

```text
Email

[____________]

Invalid email format
```

---

# Table Design

Requirements:

- Search
- Filter
- Pagination
- Sorting
- Responsive

---

# Dashboard Standard

Dashboard contains:

## Header

```
Welcome User
```

---

## KPI Section

Example:

```
Users

Revenue

Orders

Reports
```

---

## Analytics Section

Charts:

- Line
- Bar
- Doughnut

---

## Activity Section

Recent actions:

```
User created report

5 minutes ago
```

---

# Navigation Design

Sidebar:

Contains:

- Logo
- Menu
- Active state
- User profile

---

# Menu Rules

Maximum:

```
7 main menus
```

Use:

Submenu for more items.

---

# Icon System

Recommended:

- Lucide Icons
- Material Icons

Rules:

- Same icon style
- Same size
- Clear meaning

---

# Responsive Rules

Breakpoints:

| Device | Size |
|-|-|
| Mobile | <640px |
| Tablet | 640-1024px |
| Desktop | >1024px |

---

# Mobile Design

Must support:

- Touch interaction
- Collapsible menu
- Responsive tables
- Large buttons

---

# Accessibility

Follow:

WCAG principles.

Requirements:

- Good contrast
- Keyboard navigation
- Screen reader support
- Clear focus state

---

# Animation Rules

Use:

- Small transitions
- Loading animation
- Smooth interaction

Avoid:

- Excessive animation

---

Example:

```css
transition:
all 0.2s ease;
```

---

# Tailwind CSS Configuration

Recommended:

```javascript
module.exports = {

theme:{

extend:{

colors:{

primary:"#2563eb"

}

}

}

}
```

---

# Component Design Rules

Every component must:

- Be reusable
- Have clear purpose
- Support responsive
- Support dark mode
- Have documentation

---

# UI Review Checklist

## Visual

- [ ] Consistent spacing
- [ ] Correct typography
- [ ] Proper colors
- [ ] Modern appearance

---

## UX

- [ ] Clear navigation
- [ ] Easy actions
- [ ] Good feedback

---

## Responsive

- [ ] Mobile support
- [ ] Tablet support
- [ ] Desktop support

---

# GitHub Copilot UI Prompt

```
Act as Senior SaaS UI/UX Designer.

Create UI based on this Design System.

Requirements:

- Tailwind CSS
- Modern SaaS style
- Responsive
- Dark mode
- Reusable components
- Accessibility

Follow DESIGN_SYSTEM.md exactly.
```

---

# Final Design Approval

Before release:

```
UI Review

↓

UX Testing

↓

Responsive Testing

↓

Accessibility Check

↓

Approve
```

---

# End of Design System
