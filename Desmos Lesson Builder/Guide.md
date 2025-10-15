# Desmos Activity Construction Guide

## Overview

You are tasked with generating Desmos activities using the Computation Layer (CL). Each activity comprises multiple screens, each containing components like Notes, Math Inputs, Graphs, etc. Your goal is to assemble these components with appropriate CL scripts to create interactive and educational experiences.

## Component Specifications

### Note Component

- **Purpose**: Display text to students.
- **CL Sinks**:
  - `content`: The text to display.
  - `hidden`: Boolean to show/hide the note.
- **Example**:
  ```cl
  content: "Welcome to the lesson!"
  hidden: false
  ```

### Math Input Component

- **Purpose**: Receive mathematical expressions from students.
- **CL Sinks**:
  - `correct`: Define the correct answer.
  - `disableEdit`: Disables editing the expression.
  - `disableEvaluation`: Disables Desmos from evaluating the contents of the response
  - `hidden`: When true, this component will not be shown to students.
  - `initialLatex`: Sets the initial value of the expression input. Should be a valid LaTeX string.
  - `initialText`: Sets the initial value of the text input when students are asked to explain their thinking.
  - `showPeerResponses`: boolean that overrides the "show classmates' responses" checkbox, and lets you use that feature even when it's not at the end of a column.
  - `suffix`: Adds a suffix to everything entered by the student. Recommended for inputs that expect a certain unit (e.g., ft. or %).
- **Example**:
  ```cl
  correct: this.numericValue = 42
    ```

### Graph Component

- **Purpose**: Display graphs and visual representations.
- **CL Sinks**:
  - `expression`: Define expressions to plot.
  - `bounds`: Set the viewing window.
- **Example**:
  ```cl
  expression("f"): "y = x^2"
  bounds: [-10, 10, -10, 10]
  ```

## Activity Structure

1. **Introduction Screen**: Use a Note to welcome students and outline objectives.
2. **Instructional Screens**: Combine Notes, Math Inputs, and Graphs to teach concepts.
3. **Practice Screens**: Provide problems for students to solve with immediate feedback.
4. **Summary Screen**: Recap key points and assess understanding.

## CL Best Practices

- Use clear and concise CL scripts.
- Ensure all components have unique identifiers.
- Test each screen individually to verify functionality.
- Utilize variables to store intermediate calculations when necessary.

## Additional Resources

For detailed CL documentation and examples, refer to the [Desmos Computation Layer Documentation](https://teacher.desmos.com/computation-layer/documentation).
