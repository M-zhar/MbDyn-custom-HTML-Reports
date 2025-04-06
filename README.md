# MbDyn-custom-HTML-Reports
MbDyn  custom HTML reports.The generator allows you to mix static HTML content with embedded Python code for dynamic section generation. The Python code must be enclosed between the preprocessing directives:


This directory contains a lightweight generator for custom HTML reports.

The generator allows you to mix static HTML content
with embedded Python code for dynamic section generation.
The Python code must be enclosed between the preprocessing directives:


#beginpreprocess

and

#endpreprocess

This allows you to automate repetitive structures such as tables, cards,
or repeated sections using Python loops or logic.

You can define HTML-safe variables using:
HTMLVar(name, value)


or constant variables with:
ConstHTMLVar(name, value)

These variables can be used within Python code to maintain consistency
and simplify changes across the report. When used inside dynamic content,
expressions involving these variables are injected as-is for better clarity.

The generated HTML file is printed to standard output.
You can redirect it to a file or serve it through any static server.

Refer to the sample templates provided in the examples/ directory
to understand usage patterns and best practices.

python HTMLReportGen.py input_template.html

(Example: python HTMLReportGen.py quarterly_summary.html)

This tool works with Python 3+.
Suggestions for enhancements, themes, or bug fixes are welcome!

By default, the generator includes the Python logic blocks
in the final HTML for transparency. To exclude them, run:

python HTMLReportGen.py input_template.html off
Accepted values for disabling logic blocks: false, no, off, 0.
They are case-insensitive and accept abbreviations.

<html>
  <head><title>Team Overview</title></head>
  <body>
    <h1>Team Members</h1>

    #begincode
    team = ['Alice', 'Bob', 'Charlie']
    for member in team:
        print(f"<p>{member}</p>")
    #endcode

  </body>
</html>


<html>
  <head><title>Team Overview</title></head>
  <body>
    <h1>Team Members</h1>

    <p>Alice</p>
    <p>Bob</p>
    <p>Charlie</p>

  </body>
</html>



