# Design: font change

---

# Change .welcome Class Font to Roboto

## Overview
Update the font styling for the .welcome class in the main stylesheet to use the Roboto font family instead of the current font.

## Architecture
This is a simple CSS styling change that modifies the font-family property of a single CSS class selector.

### Components
#### Main Stylesheet
The main CSS stylesheet containing the .welcome class rule

**File:** `style.css`

**Responsibilities:**
- Contains the .welcome CSS class definition
- Currently specifies the existing font family
- Will be modified to use Roboto font

## Design Decisions

### Font Selection

**Decision:** Change the font-family property of .welcome class to 'Roboto'

**Rationale:** Meets the explicit requirement to change the .welcome class font to Roboto

### Implementation Approach

**Decision:** Modify the existing .welcome CSS rule by updating or replacing the font-family declaration

**Rationale:** Straightforward CSS modification requires minimal changes to the stylesheet

### Font Import

**Decision:** Assume Roboto is already available (either through system fonts, CDN, or existing imports). If not present, add appropriate @import statement

**Rationale:** Allows flexibility depending on current project setup without blocking the change
