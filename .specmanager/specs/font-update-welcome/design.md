# Design: Font Update Welcome

---

# Roboto Typography System Implementation

## Overview
This design document outlines how to implement the Roboto font family across the project, starting with updating the .welcome class while establishing a reusable typography system for future consistency.

## Architecture
The implementation uses Google Fonts CDN to load Roboto with multiple font weights, ensuring optimal performance and compatibility. The typography system is structured through CSS classes and semantic HTML elements.

### Components
#### Google Fonts Import
Loads the Roboto font family from Google Fonts CDN with preconnect optimizations for performance

**File:** `index.html`

**Responsibilities:**
- Ensure Roboto font is available before CSS rules apply
- Optimize network requests with preconnect and prefetch links
- Support multiple font weights for flexibility

#### Typography CSS Classes
CSS classes that define typography rules using Roboto font family

**File:** `css/style.css`

**Responsibilities:**
- Define .welcome class with Roboto font
- Provide fallback fonts for browser compatibility
- Establish base typography rules for consistency

## Design Decisions

### Font Loading Method: Google Fonts

**Decision:** Use Google Fonts CDN to load Roboto with preconnect optimization

**Rationale:** Google Fonts is reliable, provides multiple weights, has excellent browser support, and is already used in the project (Freehand and M PLUS 1p). The preconnect and prefetch links optimize performance by establishing early connections to the font CDN.

### Font Weights to Load

**Decision:** Load Roboto in weights 300, 400, 700 (Light, Regular, Bold)

**Rationale:** These are the most common weights needed for typography hierarchy. Regular (400) is essential for body text, Bold (700) for headings and emphasis, and Light (300) for secondary content.

### Fallback Font Stack

**Decision:** Use 'Roboto, sans-serif' as the font stack

**Rationale:** If Roboto fails to load, the system font will gracefully degrade to the default sans-serif, ensuring readability. This provides resilience against network failures.

### HTML Import Location

**Decision:** Add Roboto import to the existing Google Fonts link in the <head> section

**Rationale:** Consolidates all font imports in one place, reducing HTTP requests and making font management easier. The preconnect links already exist, so we're extending the current setup.

### CSS Class Strategy

**Decision:** Update .welcome class with Roboto font while preserving other style properties

**Rationale:** The .welcome class currently uses Freehand font. Changing only the font-family preserves the layout, sizing, and alignment while achieving the typography requirement.
