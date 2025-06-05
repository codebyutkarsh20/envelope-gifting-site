# Gift Recommendation Web App - Frontend Concept

This document outlines a proposed UI/UX for a single-page web app that helps users obtain gift ideas based on recipient details.

## Layout Overview
- **Header** with simple title and tagline.
- **Form container** with progress indicator and sections for each question.
- **Submit button** at the bottom to trigger gift recommendations.
- **Results area** displayed below the form after submission.

## Form Fields and UI Components
1. **Relationship with Recipient** – Dropdown: `Friend`, `Family`, `Colleague`, `Partner`, `Other`.
2. **Occasion** – Dropdown: `Birthday`, `Anniversary`, `Graduation`, `Holiday`, `Other`.
3. **Recipient's Age Group** – Radio buttons: `Child 0–12`, `Teenager 13–19`, `Adult 20–64`, `Senior 65+`.
4. **Interests or Hobbies** – Multiselect tags: `Sports`, `Reading`, `Technology`, `Fashion`, `Music`, `Art`, `Travel`, `Other`.
5. **Personality Type** – Radio buttons: `Outgoing/Extroverted`, `Introverted/Reserved`, `Creative/Artistic`, `Practical/Down-to-Earth`.
6. **Budget Range** – Dropdown: `Under $25`, `$25–$50`, `$50–$100`, `Over $100`.

## Visual Styling
- **Color scheme:** Soft background (#f9f9f9) with accent color (#0275d8) for buttons and progress steps.
- **Typography:** Clean sans-serif font (e.g., `Helvetica`, `Arial`).
- **Spacing:** Each field grouped with ample margin for readability.
- **Buttons:** Rounded corners, filled accent color for primary action (`Submit`).
- **Progress indicator:** Step dots or numeric steps at top; highlight current section.

## Guidance and Validation
- Mark fields as **required** to ensure all questions are answered.
- Use tooltip icons (`?`) next to labels with short explanations (e.g., "Choose all hobbies that apply").
- Disable **Submit** until all fields are completed.

## User Flow
1. User opens the page and sees a short intro and the six-step form.
2. As they fill each field, the progress indicator updates.
3. On **Submit**, the form is validated and replaced by a loading state.
4. Once results are ready, display **4–5 gift suggestions** in card format with images and links.

## Component Hierarchy
```
Page
 ├─ Header
 ├─ FormContainer
 │   ├─ RelationshipDropdown
 │   ├─ OccasionDropdown
 │   ├─ AgeGroupRadios
 │   ├─ InterestsMultiselect
 │   ├─ PersonalityRadios
 │   ├─ BudgetDropdown
 │   └─ SubmitButton
 └─ ResultsArea (hidden until submission)
```

This layout keeps all required questions on one page while guiding the user step by step. It minimizes scrolling, provides clear call-to-action, and presents results in a dedicated area so users can easily review the recommendations.

