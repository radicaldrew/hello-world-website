# Requirements: Font Update Welcome

---

# Typography System Update - Roboto Font Integration

## Overview
Update the project's typography system to use Roboto as the primary font family. This includes replacing the current Freehand font used in the .welcome class with Roboto, importing Roboto from Google Fonts, and establishing a consistent typography foundation for the website.

## Goals
- Replace the .welcome class font from Freehand to Roboto
- Add Roboto font import from Google Fonts
- Establish a consistent, scalable typography system for future UI elements
- Maintain or improve readability and visual hierarchy
- Ensure cross-browser compatibility

## Requirements

### 1. Font Integration

#### 1.1 Import Roboto from Google Fonts
Add Google Fonts preconnect links and stylesheet link to import Roboto font family with necessary weights (400, 700) into the HTML document.

**Priority:** must-have

**Acceptance Criteria:**
- [ ] Google Fonts preconnect links are added to the HTML head
- [ ] Roboto font is imported with weights 400 (regular) and 700 (bold)
- [ ] Font preload is optimized for performance
- [ ] Stylesheet loads before custom CSS

#### 1.2 Remove unused font imports
Remove or retain existing font imports (Freehand and M+PLUS1p) based on whether they are still used elsewhere in the project.

**Priority:** should-have

**Acceptance Criteria:**
- [ ] Unused font imports are identified
- [ ] Freehand font import is removed if not used in other elements
- [ ] Only required fonts are loaded to optimize performance

### 2. Welcome Class Styling

#### 2.1 Update .welcome class to use Roboto
Change the font-family property of the .welcome class from Freehand to Roboto with appropriate fallback fonts.

**Priority:** must-have

**Acceptance Criteria:**
- [ ] Font-family is set to: 'Roboto', sans-serif
- [ ] Roboto font displays correctly on all major browsers
- [ ] Fallback to sans-serif is available if font fails to load
- [ ] Existing styling (font-size, text-align, font-weight) is preserved

#### 2.2 Verify .welcome styling is preserved
Ensure all other CSS properties of the .welcome class remain unchanged (font-size: 78px, text-align: center, font-weight: 400).

**Priority:** must-have

**Acceptance Criteria:**
- [ ] Font size remains 78px
- [ ] Text alignment remains center
- [ ] Font weight remains 400
- [ ] Image styling (.welcome img) remains unchanged

### 3. Typography System Foundation

#### 3.1 Define base typography variables/classes
Create a foundation for consistent typography across the site by establishing base font families and properties that can be reused.

**Priority:** should-have

**Acceptance Criteria:**
- [ ] Base body font-family is set to Roboto with fallback
- [ ] Consistent font stack is applied to base elements
- [ ] Typography can be easily extended for future components
- [ ] Base styles do not negatively impact existing h1 and .welcome styling

### 4. Testing & Validation

#### 4.1 Visual verification of Roboto font
Verify that Roboto font displays correctly in the .welcome paragraph element with proper rendering and readability.

**Priority:** must-have

**Acceptance Criteria:**
- [ ] Roboto font renders without distortion
- [ ] Text remains readable at 78px size
- [ ] Font renders consistently across Chrome, Firefox, Safari, and Edge

#### 4.2 Performance verification
Ensure font loading does not negatively impact page load time or visual stability (CLS).

**Priority:** should-have

**Acceptance Criteria:**
- [ ] Font loads without blocking page render
- [ ] No layout shift occurs when font loads (CLS optimization)
- [ ] Page performance remains acceptable
