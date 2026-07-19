<!-- ====================================================================== -->
<!-- File: docs/27_CSS_GUIDE.md -->
<!-- ====================================================================== -->

# CSS Development Guide

Version 2.0

---

# Purpose

This document defines CSS standards for Google Apps Script Enterprise Applications using Tailwind CSS and modern UI practices.

The objective is to create:

- Modern SaaS interface
- Consistent visual design
- Responsive layouts
- Reusable styling patterns
- Maintainable frontend code

---

# CSS Philosophy

The project follows:

```
Utility First

+

Design System

+

Component Based Styling

+

Responsive First
```

---

# CSS Technology Stack

Recommended:

```
Tailwind CSS

+

CSS Variables

+

Modern Browser CSS
```

---

# Styling Architecture

```text
Design Tokens

↓

Theme Configuration

↓

Components

↓

Pages

↓

Application
```

---

# CSS File Structure

Recommended:

```
styles/

├── tailwind.html

├── variables.css

├── components.css

├── utilities.css

└── themes.css
```

---

# Tailwind CSS Standard

Use:

✓ Utility classes

✓ Responsive modifiers

✓ Dark mode classes

✓ Reusable components

Avoid:

✗ Large custom CSS files

✗ Duplicate styles

---

# Example

Good:

```html
<div
class="
rounded-xl
shadow-md
p-6
bg-white
dark:bg-gray-900
">
</div>
```

---

Bad:

```html
<div class="custom-box">
</div>
```

with:

```css
.custom-box{

padding:20px;

}
```

---

# Design Tokens

Define:

- Colors
- Spacing
- Typography
- Radius
- Shadows

---

Example:

```css
:root{

--primary-color:#2563eb;

--radius-card:16px;

}
```

---

# Color System

## Primary

Used for:

- Main buttons
- Active navigation
- Important actions

---

## Secondary

Used for:

- Supporting information
- Secondary actions

---

## Status Colors

| Color | Usage |
|-|-|
| Green | Success |
| Yellow | Warning |
| Red | Error |
| Blue | Information |

---

# Theme Configuration

Example:

```javascript
tailwind.config={


darkMode:"class",


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

# Dark Mode Standard

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
dark:bg-gray-800
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

# Typography Scale

| Class | Usage |
|-|-|
| text-4xl | Main heading |
| text-2xl | Section title |
| text-xl | Card title |
| text-base | Body |
| text-sm | Description |

---

# Spacing System

Use:

8px spacing scale.

Example:

```
p-2

p-4

p-6

p-8
```

---

# Layout System

Recommended:

Flexbox:

```html
<div
class="
flex
items-center
justify-between
">

</div>
```

---

Grid:

```html
<div
class="
grid
grid-cols-1
md:grid-cols-3
">

</div>
```

---

# Container Standard

Desktop:

```
max-w-7xl
```

Mobile:

```
w-full
```

---

# Component Styling Rules

Every component requires:

- Normal state
- Hover state
- Active state
- Disabled state
- Loading state

---

# Button Styling

Primary:

```html
<button
class="
bg-blue-600
text-white
px-4
py-2
rounded-xl
hover:bg-blue-700
">

Save

</button>
```

---

# Card Styling

Standard:

```html
<div
class="
bg-white
dark:bg-gray-900
rounded-2xl
shadow
p-6
">

</div>
```

---

# Input Styling

Standard:

```html
<input
class="
w-full
border
rounded-xl
px-4
py-2
focus:ring-2
"
/>
```

---

# Table Styling

Required:

- Header style
- Row hover
- Responsive container

---

Example:

```html
<div
class="
overflow-x-auto
">

<table>

</table>

</div>
```

---

# Modal Styling

Recommended:

```
Fixed overlay

Centered card

Backdrop blur
```

---

Example:

```html
<div
class="
fixed
inset-0
bg-black/50
">

</div>
```

---

# Animation Standard

Use subtle animation.

Recommended:

```
150ms - 300ms
```

---

Example:

```html
<div
class="
transition
duration-200
">

</div>
```

---

# Loading Animation

Example:

```html
<div
class="
animate-pulse
">

Loading

</div>
```

---

# Hover Effects

Use:

- Color change
- Shadow change
- Scale slightly

Example:

```html
hover:shadow-lg
```

---

# Responsive Design Rules

Always design:

```
Mobile First

↓

Tablet

↓

Desktop
```

---

# Breakpoints

| Device | Tailwind |
|-|-|
| Mobile | Default |
| Tablet | md |
| Desktop | lg |
| Large | xl |

---

# Mobile Optimization

Required:

- Large touch targets
- Simple layout
- Collapsible navigation

---

# Accessibility CSS

Must include:

Focus:

```css
focus:ring-2
```

---

Contrast:

Ensure readable text.

---

# CSS Performance Rules

Avoid:

- Heavy animations
- Huge selectors
- Duplicate utilities

---

Use:

- Reusable classes
- Component patterns
- Tailwind utilities

---

# Component CSS Documentation

Template:

```markdown
# Component Name


Purpose:


Classes Used:


Responsive:


States:


Dark Mode:
```

---

# CSS Review Checklist

## Design

- [ ] Consistent colors
- [ ] Correct spacing
- [ ] Typography standard

---

## Responsive

- [ ] Mobile tested
- [ ] Tablet tested
- [ ] Desktop tested

---

## Accessibility

- [ ] Focus state
- [ ] Contrast
- [ ] Keyboard support

---

## Performance

- [ ] No duplicate CSS
- [ ] Optimized styles

---

# GitHub Copilot CSS Prompt

```
Act as Senior UI Engineer.

Review this CSS/Tailwind implementation.

Analyze:

1. Design consistency
2. Responsive behavior
3. Accessibility
4. Performance
5. Maintainability

Suggest improvements.

Follow CSS_GUIDE.md.
```

---

# Copilot UI Styling Prompt

```
Create a modern SaaS UI component.

Requirements:

- Tailwind CSS
- Responsive
- Dark mode
- Accessible
- Clean spacing
- Professional design

Follow project Design System.
```

---

# Final CSS Quality Gate

Before Production:

```
Design Review

↓

Responsive Test

↓

Accessibility Test

↓

Performance Check

↓

Release
```

---

# End of CSS Development Guide
