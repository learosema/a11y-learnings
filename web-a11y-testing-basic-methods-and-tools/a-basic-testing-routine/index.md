# A Basic Testing Routine

## Introduction

The whole point of web accessibility testing is to find issues or barriers that users with disabilities might run into while they surf the web. The discoveries testers make should provide developers and designers with recommendations, so improvements can be made to the overall user experience of the product, application, or web site.

In order for the process of evaluating your web pages or applications for accessibility to bear fruit and become a useful indicator for your projects, you will need to either replicate an existing web accessibility testing methodology like the one presented in this module, or develop your own. Adopting such a methodology is crucial when it comes to integrating consistency in the process. True web accessibility conformance does not happen by accident — you need a process.

A methodology such as this one provides some of the foundational pieces required to achieve a consistent process and consistent results:

### 1. Determine the Scope for Testing

- Determine how many pages will be evaluated, selecting representative pages, choosing which conformance level to evaluate against, etc.

### 2. Conduct Tests

- Automated Tests: Use a specific tool or tools to find issues that can be found automatically and report those as a foundation for the work to come in the manual testing phase.
- Manual Tests: Following the suggested methodologies in this section, go through a series of tests using different tools to find issues in the page or application that is being tested. The recommended routine for manual testing is:
  - Input: Keyboard
  - Input: Touch
  - Visual Presentation
  - Alternative Text
  - Audio and Video
  - Semantics and Document Structure
  - Forms
  - Dynamic Content
  - Custom Widgets

### 3. Document All Findings in an Accessibility Report Format

- Bring all the findings together into a comprehensive and usable format that allows stakeholders to remediate the issues found based on recommendations provided.

### 4. Plan for Remediation

- Use testing results to prioritize issues to remediate based on things like business value, risk, severity, etc.

### 5. Conduct Regression Testing

- Re-run previously run tests to check whether program behavior has changed and whether previously fixed faults have re-emerged.

## In this Section:

- Run an Automated Check
- Screen Reader Resources
- Test for Keyboard Accessibility
  - Enabling Keyboard Access on a Mac
  - Tab Focusability and Tab Order
  - Keyboard Functionality
  - Keyboard Functionality with Screen Reader On
  - Visual Focus Indicator
  - Effective Focus Management (Form Validation, Dialogs, AJAX, Etc.)
  - Keyboard Traps
- Test for Touch Device Accessibility
  - Touch Target Size
  - Touch Functionality
  - Touch Functionality with Screen Reader On
- Test for Meaning Conveyed with Color
- Test Alt Text Quality
- Test Video/Audio Accessibility
- Test for Landmarks
- Test for Headings
- Test Link Text Quality
- Test Form Labels and Instructions
- Test Form Validation
- Testing Custom Widgets
