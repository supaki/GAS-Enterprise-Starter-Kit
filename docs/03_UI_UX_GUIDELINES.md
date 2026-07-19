<!-- ====================================================================== -->
<!-- File: docs/03_UI_UX_GUIDELINES.md -->
<!-- ====================================================================== -->

# UI / UX Guidelines

Version 2.0

---

# Purpose

Define a consistent design system for all pages.

Every screen must look like part of the same SaaS application.

---

# Design Philosophy

Inspired by

- Google Workspace
- Notion
- Linear
- Vercel
- Supabase
- Stripe Dashboard

Characteristics

- Clean
- Modern
- Minimal
- Professional
- Spacious
- Fast

---

# Design Principles

- Consistency
- Simplicity
- Accessibility
- Readability
- Responsive
- Reusability

---

# Layout

```text
+------------------------------------------------+
| Navbar                                         |
+-----------+------------------------------------+
| Sidebar   |                                    |
|           | Dashboard Content                  |
|           |                                    |
|           | Cards                              |
|           | Charts                             |
|           | Tables                             |
|           |                                    |
+-----------+------------------------------------+
```

---

# Color Palette

| Name | Color |
|------|--------|
| Primary | #2563EB |
| Secondary | #14B8A6 |
| Success | #16A34A |
| Warning | #F59E0B |
| Danger | #DC2626 |
| Info | #0284C7 |
| Background | #F8FAFC |
| Surface | #FFFFFF |
| Border | #E5E7EB |
| Text | #111827 |

Dark Mode

| Name | Color |
|------|--------|
| Background | #111827 |
| Surface | #1F2937 |
| Border | #374151 |
| Text | #F9FAFB |

---

# Typography

Font

Preferred

- Inter
- Roboto
- Noto Sans Thai

Heading

- Bold
- Large

Body

- Medium

Caption

- Small

---

# Border Radius

Cards

16px

Buttons

12px

Inputs

12px

Dialogs

20px

---

# Shadows

Use soft shadows.

Avoid heavy shadows.

---

# Spacing

Use 8px grid.

Examples

8

16

24

32

40

48

---

# Buttons

Primary

Filled

Secondary

Outlined

Danger

Red

Icon Button

Rounded

Loading Button

Supported

---

# Forms

Every form must include

- Label
- Placeholder
- Validation
- Required Indicator
- Error Message
- Helper Text

---

# Tables

Support

- Search
- Sort
- Filter
- Pagination
- Responsive
- Sticky Header
- Empty State

---

# Dashboard Cards

Each card contains

- Icon
- Title
- Value
- Trend
- Color Indicator

---

# Charts

Use Chart.js

Supported

- Bar
- Line
- Pie
- Doughnut
- Area

---

# Notifications

Use Toast

Top Right

Auto Close

Success

Warning

Error

Info

---

# Dialogs

Use Modal

Support

- Confirm
- Delete
- Edit
- Preview

---

# Sidebar

Support

- Collapse
- Expand
- Nested Menu
- Icons
- Active Menu
- Badge

---

# Navbar

Contains

- Logo
- Search
- Notifications
- User Profile
- Theme Switch

---

# Loading

Use

Skeleton

Spinner

Progress Bar

Never leave blank screens.

---

# Empty State

Include

Illustration

Title

Description

Action Button

---

# Responsive Breakpoints

| Device | Width |
|---------|------|
| Mobile | <640px |
| Tablet | 640–1024px |
| Desktop | >1024px |

---

# Accessibility

Support

- Keyboard Navigation
- Focus State
- Screen Readers
- Color Contrast
- ARIA Labels

---

# Animation

Smooth

150–250 ms

Avoid excessive animation.

---

# Tailwind CSS Rules

Prefer Utility Classes.

Avoid custom CSS unless necessary.

Group repeated styles into reusable components.

---

# Best Practices

✓ Consistent spacing

✓ Consistent typography

✓ Responsive layout

✓ Reusable components

✓ Dark Mode support

✓ Accessible UI

✓ Fast rendering

---

# GitHub Copilot Prompt

Generate reusable Tailwind CSS components.

Do not duplicate HTML.

Follow the design system.

Ensure every page looks like the same application.

---

# Checklist

- Responsive
- Accessible
- Dark Mode
- Reusable Components
- Consistent Colors
- Consistent Typography
- Mobile Friendly
- Modern SaaS Appearance
