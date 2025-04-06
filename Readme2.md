HTML Report Generator – 12 Week Project Plan

🌟 Project Overview

A lightweight Python preprocessor to dynamically generate HTML reports using embedded Python code blocks. Users can inject Python logic within HTML templates to generate content such as lists, tables, and custom layouts with control flow.

🌟 Goals

Build a Python-based tool to parse HTML templates with embedded Python logic.

Enable users to define variables and control flow within HTML using #begincode and #endcode.

Allow toggling between showing or hiding code blocks in the final report.

Add support for loops, variables, and string manipulation inside HTML.

Ensure compatibility with both basic and advanced HTML templates.

Create user-friendly documentation and examples.

Add syntax highlighting (optional) for embedded Python code blocks using Pygments.

Make the tool work cross-platform (Windows/Linux/Mac).

Implement modular folder structure for easy integration.

Create a template theme for polished HTML output.

Publish the tool as open-source on GitHub.

Prepare a sample showcase (template + report output).

📅 Milestones / Timeline

Week 1–2: Initialization

I. Tool Base Setup

Define project structure (HTMLReportGen.py, examples/, themes/, etc.).

Implement #begincode → Python interpreter → output injection logic.

Handle simple print() output into HTML.

Week 3–4: Core Features

II. Variable Handling and Code Visibility

Add HTMLVar() and ConstHTMLVar() helper functions.

Add optional argument to hide code blocks (off | no | false | 0).

Output redirection via contextlib.redirect_stdout().

⏳ Midterm Evaluation

Working prototype of preprocessor

Sample HTML input/output

Command-line interface functional

Supports dynamic content via Python logic

Week 5–6: Testing & Examples

III. Robustness & Examples

Create multiple sample templates in examples/.

Add error handling (e.g., invalid Python blocks).

Add unit tests to validate generated HTML output.

Week 7–8: Enhancements

IV. Syntax Highlighting & Themes

Integrate Pygments for optional syntax highlighting.

Create base CSS theme in /themes/style.css.

Allow light/dark theme switching in output reports.

⏳ Final Evaluation

Full-featured HTML report generator

Customizable themes, code toggle

Complete documentation & examples

GitHub repository with MIT License

🎓 Deliverables

HTMLReportGen.py: Main preprocessor script

examples/: Working template samples

themes/style.css: Styling for output

README.md: Full documentation

LICENSE: MIT License

Optional Pygments support for syntax highlighting

