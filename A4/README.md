# Assignment 4

## **1. Mody AI - Draw Together**

DrawTogether focuses on helping beginner and hobbyist artists learn through guided reflection and inspiration from related works, rather than evaluation or external judgment.

We received 2 evaluations.

## **2. Merged Violations**

### **H1 - Visibility of System Status**

- Unclear selection logic in category selection (checkbox vs single choice) - Severity 2
- Feedback text does not clearly reference the currently displayed drawing - Severity 2
- Required vs optional input fields are not indicated in upload flow - Severity 2

### H2 - Match Between System and Real World

- Use label in photo confirmation is ambiguous - Severity 2

### H3 - User Control and Freedom

- Feedback prompt only offers Yes (no way to decline) - Severity 3
- Navigation back behavior is inconsistent - Severity 3
- Popup for photo source has no cancel/exit option - Severity 3

### H4 - Consistency and Standards

- Back button shows current page name instead of destination page - Severity 2

### H6 - Recognition Rather Than Recall

- Drawing thumbnails show only image and date, no name or category - Severity 2

### H7 - Flexibility and Efficiency of Use

- User cannot create custom drawing categories - Severity 2
- No search function in Progress for large drawing collections - Severity 3
- Camera interface lacks standard options (flash, switch camera, gallery shortcut) - Severity 2
- Image carousel always opens at first drawing instead of tapped one - Severity 2

### H8 - Aesthetic and Minimalist Design

- Redundant Back and Cancel buttons on same screen - Severity 1

## **3. Selected Prototype**

We selected the phone prototype as the base for the medium-fidelity version for the following reasons:

- It received more detailed and actionable heuristic feedback, especially regarding navigation, user control, and efficiency.
- A mobile format is more aligned with the usage context of our project, since users are expected to upload drawings, take photos, and revisit progress frequently in everyday environments.

At this stage, no features are moved from the other prototype, as all core interactions are already present in the phone version. Instead, we focus on refining control, clarity, and flexibility based on the violations.

## 4. Interactive Prototype

You can reach the interactive prototype via the following link: https://www.figma.com/design/xBDSD3Scp8Cblzibf7plxw/MODY-AI---A4?node-id=0-1&m=dev&t=0b0O88n5FlyUjqNl-1

We created medium-fidelity versions of the following two screens in Figma:

**Screen 1 - Home Screen** 

- It is the most frequent entry point of the application.
- It directly connects all three core tasks.
- It supports fixing:
    - H3 (User Control - navigation clarity)
    - H4 (Consistency of back behavior)
    - H1 (System understanding of where the user is)

**Screen 2 - Progress Page**

- It accumulated the highest number of severity 3 violations:
    - H7 (No search function)
    - H3 (Forced feedback prompt)
    - H3 (Confusing back behavior)

## 5. Plans

For the high-fidelity prototype, we plan to resolve all severity 3 violations and as many severity 2 violations as possible, as required by the assignment. The fixes will directly build on the issues identified in the heuristic evaluations.

### **Fixes for Severity 3 Violations (High Priority)**

**H3 - User Control and Freedom**

- The forced feedback popup will be redesigned to include clear options such as “Yes,” “No,” and “Maybe later”, so users are never pushed into an action unwillingly.
- Back navigation will be standardized across the application. The back button will always lead to the previous logical screen, not reset the navigation flow.
- The photo source popup (camera / gallery) will include a visible Cancel or Close (X) option so users are never trapped inside a modal.

**H7 - Flexibility and Efficiency of Use**

- A search bar will be added to the Progress section to allow users to search drawings by name, date, or category.

### Fixes for Severity 2 Violations (Medium Priority)

**H1 - Visibility of System Status**

- Required input fields in the upload screen will be clearly marked using placeholders or visual indicators.
- Feedback text in the Progress section will dynamically update to match the currently visible drawing.

**H2 - Match Between System and the Real World**

- The ambiguous “Use” button in the photo confirmation flow will be renamed to “Confirm,” “Select,” or “Upload” to reflect common mobile design standards.

**H6 - Recognition Rather Than Recall**

- Drawing thumbnails in the Progress grid will show at least the drawing name (and optionally the category) to allow easy recognition without opening each item.

**H7 - Flexibility and Efficiency**

- Users will be able to create and manage custom categories instead of being restricted to predefined ones.
- The drawing detail view will open directly to the selected drawing, instead of always starting from the first image in the carousel.

### Fixes for Severity 1 Violations (Low Priority)

**H8 - Aesthetic and Minimalist Design**

- Redundant navigation elements such as having both Back and Cancel on the same screen will be reduced to a single, consistent control.

### Excluded Violations

The following violations were excluded from the hi-fi implementation plan, as they were based on misunderstandings or intentional design decisions:

**Excluded from H1**

- Unclear selection logic in category selection (checkbox vs single choice)
    - Reason: The design already uses checkboxes to explicitly represent multi-selection. No ambiguity exists.

**Excluded from H4**

- Back button shows current page name instead of destination page
    - Reason: The evaluator misinterpreted the page title as the back button label. The back button is icon-only. And we will already fix the back navigaiton issue on H3.

**Excluded from H7**

- Camera interface lacks standard options (flash, switch camera, gallery shortcut)
    - Reason: The app intentionally delegates image capture to the native phone camera application for simplicity and reliability.

### Overall Hi-Fi Direction

The hi-fi prototype will focus on:

- Stronger user control
- Clearer system feedback
- Improved efficiency for repeated use
- Better alignment with mobile design standards