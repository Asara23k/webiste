# Design Guidelines: Professional Email Marketing Platform

## Design Approach
**System-Based Approach**: Drawing from Carbon Design System and Fluent Design principles for enterprise data-heavy applications. This is a **utility-focused productivity tool** requiring clarity, efficiency, and information density optimization.

## Core Design Principles
- **Data First**: Information hierarchy optimized for quick scanning and decision-making
- **Professional Efficiency**: Minimal friction, maximum clarity in controls and feedback
- **Dense but Organized**: Embrace information density while maintaining visual breathing room
- **Status-Driven**: Clear visual feedback for system states (running, paused, validating, errors)
- **Enterprise Reliability**: Solid, trustworthy visual language

## Typography System

**Font Stack**: System fonts for performance
- Primary: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif
- Monospace: 'Courier New', 'Monaco', monospace (for code, logs, technical data)

**Type Scale**:
- **Page Headers**: 28px/700 - Main page titles
- **Section Headers**: 20px/600 - Card and section titles  
- **Subsection Headers**: 16px/600 - Component group labels
- **Body Text**: 14px/400 - Primary content, form labels
- **Secondary Text**: 13px/400 - Metadata, timestamps, helper text
- **Small Text**: 12px/400 - Captions, technical details
- **Micro Text**: 11px/400 - Dense data tables, inline stats

**Line Heights**: 1.5 for body text, 1.2 for headings, 1.8 for code blocks

## Layout System

**Spacing Units**: Tailwind scale focused on 2, 4, 8, 12, 16, 20, 24, 32 for consistency

**Page Structure**:
- Fixed sidebar: 260px width
- Main content: Full remaining width with max-w-7xl container
- Standard page padding: px-8 py-6
- Card spacing: gap-6 for card grids

**Grid Patterns**:
- Stats cards: 4-column grid (desktop), 2-column (tablet), 1-column (mobile)
- Management tables: Single column, full width with horizontal scroll if needed
- Dashboard metrics: 3-4 column responsive grid
- Form layouts: 2-column for related fields, single column for complex inputs

## Component Library

### Navigation
- **Sidebar**: Fixed left navigation with icon + label format
- Active state: Border-left accent + background treatment
- Grouping: Subtle dividers between logical sections
- Server status widget: Integrated at top of sidebar

### Dashboard Components

**Stat Cards**:
- Large numerical display (36-48px) as focal point
- Label below number (11px uppercase, letter-spacing)
- Progress bars: 6-8px height with smooth transitions
- Percentage/metadata below bar (10-11px)
- Subtle gradient backgrounds for visual hierarchy

**Campaign Controls**:
- Primary action buttons: 14px text, 10px 20px padding
- Icon + text combination for clarity
- Button groups with 8px gap
- State indicators (running, paused) with icon animations

**Real-time Logs**:
- Monospace font for technical accuracy
- Max height with scroll: 400-500px
- Timestamp prefix for each entry (11px)
- Auto-scroll to latest with manual override
- Severity-based visual treatment

### Data Tables

**Structure**:
- Header row: 12px uppercase text, 600 weight, subtle background
- Data rows: 14px regular text, 12px vertical padding
- Alternating row backgrounds for readability (optional subtle treatment)
- Hover state: Clear background shift
- Inline actions: Right-aligned, icon buttons (16px)

**Column Organization**:
- Critical data left-aligned
- Numerical data right-aligned
- Status badges center-aligned in dedicated column
- Action column always rightmost

### Forms & Inputs

**Input Fields**:
- Height: 40px for standard inputs
- Padding: 10px 14px
- Border: 1px solid with focus state
- Labels: 14px/500, 8px margin-bottom
- Helper text: 13px below input

**Textareas**:
- Monospace for technical content (SMTP configs, code, logs)
- Minimum height: 400px for primary editors
- Line numbers for code/config (optional)
- Syntax validation feedback inline

**Dropdowns/Selects**:
- Match input height (40px)
- Clear icon affordance for interaction
- Grouped options with visual separation

### Status & Feedback

**Alert Banners**:
- 12px padding vertical, 16px horizontal
- Icon + message format
- Auto-dismiss after 5 seconds
- Multiple alerts stack with 8px gap

**Progress Indicators**:
- Linear bars: 24-30px height for primary progress
- Percentage overlay on bar when space allows
- Status text below bar (13px)
- Animated transitions (0.3s ease)

**Badges**:
- 6px 12px padding
- 12px text, 600 weight
- Border-radius: 4px
- States: success, warning, error, info, neutral

### Special Components

**SMTP Validation Display**:
- Multi-column row layout
- Geographic flags (16x12px) with country codes
- Validation status badge prominent
- Expandable error details on click

**Campaign Phase Indicator**:
- Large phase banner when in resend/special modes
- 2px border treatment
- Icon + phase name + metrics grid
- Progress visualization

## Visual Hierarchy & Spacing

**Page Rhythm**:
- Page header: mb-8
- Section spacing: mb-6 between major sections
- Card internal padding: p-6
- Subsection spacing: mb-4

**Information Density**:
- Embrace density in data tables and logs
- Provide breathing room in action areas and controls
- Use background treatments to create visual groups without adding spacing

## Responsive Behavior

**Breakpoints**:
- Mobile: < 768px - Single column, stacked layout
- Tablet: 768px-1024px - 2-column where appropriate
- Desktop: > 1024px - Full multi-column layouts

**Mobile Adaptations**:
- Sidebar collapses to hamburger menu
- Stat cards stack to single column
- Tables become scrollable cards
- Button groups wrap or convert to dropdown

## Animations & Transitions

**Purposeful Motion Only**:
- Loading states: Subtle spinner or skeleton screens
- State changes: 0.3s ease transitions
- Progress bars: Smooth width transitions
- NO decorative animations
- Focus on functional feedback

## Images

**No Hero Images**: This is a utility application - no marketing imagery needed

**Functional Graphics**:
- Country flags: 16x12px for geographic data
- Status icons: 16-20px for inline indicators  
- Logo: 30px height in sidebar header
- Charts/graphs: Use when data benefits from visualization

## Accessibility

- Focus indicators: 2px outline on all interactive elements
- Sufficient contrast ratios for all text
- Keyboard navigation throughout
- Screen reader labels on icon-only buttons
- Form validation: Inline error messages below fields