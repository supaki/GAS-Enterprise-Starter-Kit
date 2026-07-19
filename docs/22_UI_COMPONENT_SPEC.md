<!-- ====================================================================== -->
<!-- File: docs/22_UI_COMPONENT_SPEC.md -->
<!-- ====================================================================== -->

# UI Component Specification

Version 2.0

---

# Purpose

This document defines the standard UI component specification for GAS Enterprise Applications.

The objective is to create:

- Reusable UI components
- Consistent SaaS interface
- Faster development
- Maintainable frontend code
- Better collaboration with GitHub Copilot Agent

---

# UI Component Philosophy

All UI components must follow:

```
Reusable

+

Responsive

+

Accessible

+

Configurable

+

Consistent
```

---

# Component Architecture

```text
Application

↓

Layout Components

↓

Page Components

↓

Feature Components

↓

UI Components

↓

Elements
```

---

# Component Naming Convention

Format:

```
ComponentName
```

Examples:

```
UserCard

DataTable

SearchBox

ConfirmModal

KpiCard
```

---

# Component Folder Structure

Recommended:

```
components/

├── layout/

│   ├── Sidebar.html

│   ├── Navbar.html


├── ui/

│   ├── Button.html

│   ├── Card.html

│   ├── Modal.html


├── forms/

│   ├── Input.html

│   ├── Select.html


├── data/

│   ├── Table.html

│   ├── Pagination.html
```

---

# Component Standard

Every component must define:

```markdown
Component Name:

Purpose:

Input:

Output:

Events:

States:

Responsive Behavior:
```

---

# Layout Components

---

# 1. Application Layout

Purpose:

Main application container.

Structure:

```text
--------------------------------

Sidebar

        Navbar

        Content Area

--------------------------------
```

---

Example:

```html
<div class="flex">

<aside>
Sidebar
</aside>


<main>

Content

</main>


</div>
```

---

# 2. Sidebar Component

Purpose:

Application navigation.

Required:

- Logo
- Menu
- Active state
- Collapse mode

---

Example:

```text
Dashboard

Users

Reports

Settings
```

---

# 3. Navbar Component

Purpose:

Top navigation.

Contains:

- Page title
- Notification
- User profile
- Theme switch

---

# UI Components

---

# Button Component

## Purpose

User action trigger.

---

# Button Types

| Type | Usage |
|-|-|
| Primary | Main action |
| Secondary | Alternative |
| Danger | Delete |
| Ghost | Minimal |

---

Example:

```html
<button
class="
px-4
py-2
rounded-xl
bg-blue-600
">

Save

</button>
```

---

# Button States

Must support:

- Default
- Hover
- Loading
- Disabled

---

Example:

```
Saving...
```

---

# Card Component

Purpose:

Display information.

---

Structure:

```text
----------------

Header

Content

Footer

----------------
```

---

Example:

Dashboard KPI:

```
Users

12,500

+10%
```

---

# KPI Card Component

Purpose:

Display metrics.

Required:

- Title
- Value
- Icon
- Trend

---

Example:

```json
{
"title":"Users",
"value":12500,
"trend":"+15%"
}
```

---

# Input Component

Purpose:

Collect user data.

Required:

- Label
- Placeholder
- Validation
- Error state

---

Example:

```html
<label>
Email
</label>

<input
type="email"
/>
```

---

# Input States

| State | Display |
|-|-|
| Normal | Default |
| Focus | Highlight |
| Error | Message |
| Disabled | Locked |

---

# Select Component

Purpose:

Choose option.

Requirements:

- Search support
- Clear selection
- Validation

---

# Checkbox Component

Used for:

- Permission
- Settings
- Agreement

---

# Switch Component

Used for:

- Enable/Disable
- Feature toggle

Example:

```
Dark Mode

[ ON ]
```

---

# Modal Component

Purpose:

Display dialog.

---

Structure:

```text
-----------------

Title

Content


Cancel

Confirm

-----------------
```

---

# Modal Types

| Type | Usage |
|-|-|
| Confirm | Confirm action |
| Form | Data entry |
| Information | Message |

---

# Toast Notification Component

Purpose:

Temporary message.

Types:

```
Success

Error

Warning

Info
```

---

Example:

```
✓ Saved successfully
```

---

# Data Components

---

# Data Table Component

Purpose:

Display records.

Required:

- Header
- Sorting
- Search
- Pagination
- Actions

---

Structure:

```text
------------------------------------------------

Name     Email       Role      Action

------------------------------------------------
```

---

# Table Features

Support:

- Loading
- Empty state
- Error state

---

# Pagination Component

Purpose:

Navigate large data.

Example:

```
< 1 2 3 4 >
```

---

# Search Component

Requirements:

- Debounce
- Clear button
- Loading indicator

---

Example:

```text
Search users...

[__________]
```

---

# Chart Components

Supported:

- Line Chart
- Bar Chart
- Doughnut Chart

---

# Chart Rules

Must have:

- Title
- Legend
- Tooltip
- Responsive size

---

# Loading Components

---

# Skeleton Loader

Used during:

- API loading
- Dashboard loading

---

Example:

```
████████

██████
```

---

# Empty State Component

When no data:

Example:

```
No records found

Create your first item
```

---

# Error State Component

Example:

```
Unable to load data

Retry
```

---

# Form Component Standard

Form must include:

```text
Form Title

↓

Input Fields

↓

Validation

↓

Submit Button

↓

Result Message
```

---

# Component Documentation Template

Use:

```markdown
# Component Name


## Purpose


## Props


## Events


## Example


## States


## Responsive Behavior
```

---

# Tailwind CSS Rules

Use:

✓ Utility classes

✓ Responsive modifiers

✓ Dark mode classes

Avoid:

✗ Inline styles

✗ Duplicate CSS

---

Example:

```html
<div
class="
bg-white
dark:bg-gray-900
rounded-xl
shadow
p-6
">
</div>
```

---

# Accessibility Rules

Every component should support:

- Keyboard navigation
- Focus state
- ARIA labels
- Screen reader

---

# Component Review Checklist

## Design

- [ ] Consistent style
- [ ] Correct spacing
- [ ] Responsive

---

## Code

- [ ] Reusable
- [ ] Clean structure
- [ ] Documented

---

## UX

- [ ] Loading state
- [ ] Error state
- [ ] Feedback message

---

# GitHub Copilot Component Prompt

```
Act as Senior Frontend Engineer.

Create a reusable SaaS UI component.

Requirements:

- Tailwind CSS
- Responsive design
- Dark mode
- Accessibility
- Reusable structure
- Clear documentation

Follow UI_COMPONENT_SPEC.md.
```

---

# Component Refactoring Prompt

```
Review this UI component.

Improve:

- Reusability
- Performance
- Accessibility
- Responsive behavior
- Code quality

Do not change business logic.
```

---

# Final Component Approval

Before adding component:

```
Design Review

↓

Code Review

↓

Accessibility Check

↓

Component Library Update
```

---

# End of UI Component Specification
