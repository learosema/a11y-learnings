# Accountability for Testing

## Testing Should Be an Integral Part of the Development Life Cycle

Testing for accessibility is often treated as an afterthought and left to be conducted at the end of a project. However, reserving testing for accessibility until the end of the development lifecycle can be costly and significantly increase the time and cost of completing a project.

Testing for accessibility must be taken seriously throughout all of the major stages of the development process — especially during the design and build/creation phases of the process — to avoid costly mistakes that don't reveal themselves until the testing phase.

### The Planning and Design Phase

When accessibility is taken into account while designing web content and user interactions, many accessibility issues that commonly ripple through the development lifecycle can be avoided.

From the planning and design phase of the web development process, developers should receive accessibility annotations based on the accessibility standards and best practices the project plans to abide by.

The annotations should point out what to do in order to ensure an accessible user experience (e.g., color choices, alternative text for images, heading levels, link text, form labels and error messages, visual focus colors, user interactions and keyboard functionality).

Testing also needs to be considered early on in this stage. Those responsible for testing should start to define the scope of the tests and develop and write tests based on the accessibility requirements defined in the planning phase.

Even the design annotations and design requirements can be used to develop tests for the project. Developing tests this early will increase the chance of catching and fixing critical accessibility issues.

### The Build/Creation Phase

The build/creation phase of the development process plays a significant part when it comes to testing for accessibility. During this phase, developers should be conducting automated tests to check their code as they're writing their code.

Unit tests, integration tests, and tools like aXe can aid in catching a number of accessibility issues before they reach the production environment (see the Automated Testing Tools section of this course for more information). In an ideal situation, issues that can be caught by automated tests should never be caught during the actual testing phase — which should focus on comprehensive manual testing and QA.

In addition to automated tests, developers should at least test their content for keyboard accessibility and should test custom widgets with screen readers.

Testing of custom widgets is especially critical since developers are creating the functionality basically from scratch. Accessibility errors that can be caught during this phase can be addressed quickly when developers embrace testing as part of the normal development process. Errors can and will slip by, though, so the actual testing phase still needs to be completed.

### The Testing Phase

The testing phase of the development process should verify if the accessibility requirements for the project were met and validate the automated tests run by developers. During the testing phase, the tests that were created during the planning phase should be conducted using automated testing and manual testing methods.

Roles that can conduct testing may include expert accessibility team members, a quality assurance team trained in accessibility, developers with accessibility knowledge, and users who have disabilities (using real users to evaluate the user experience). Everything from front-end markup and programming, to text content, to multimedia content should be evaluated during the testing phase as defined by the scope of the tests.

Once testing is complete, findings should be reported in a detailed format that allows even those with little or no accessibility knowledge to fix the issue. Accessibility defects should be explained in specifics and in a manner that makes sense to the stakeholders receiving the reports.
