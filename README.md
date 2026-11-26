# SYP_analysis

Modified_combined_normalized ----> Alums
Modified_combined_normalised_attendees ----> Attendees

# Student Enrollment Flow Analysis

Interactive Sankey diagrams that show how undergraduate students move through university programs and departments, and how gender breaks down within them (2015-2023).

## Overview

University enrollment data is hard to read as a table. This project turns it into **Sankey diagrams**, flow charts where the width of each band shows how many students are in each path. The goal is to see which programs students end up in, how those programs map to departments, and what gender representation looks like in engineering and technical fields.

## Key Questions

- Which programs do undergraduate students finish in?
- How do programs roll up into broader departments?
- How does gender representation differ across departments such as Electrical Engineering, Mechanical Engineering, and Computer Science and IT?

## Tech Stack

- **Python**
- **pandas** for data cleaning and transformation
- **Plotly** for interactive Sankey diagrams
- **Jupyter Notebook**

## What the Notebook Does

1. **Loads and cleans the data**: fixes malformed column names and filters to 2015-2023.
2. **Groups majors into departments**: maps ~150 major codes into 11 broader departments (for example, `EEE` → Electrical Engineering).
3. **Builds exploratory diagrams**: Gender → Program, Year → Level, Year → Gender.
4. **Isolates undergraduates**: keeps `UG` students only.
5. **Finds each student's final major**: sorts records by year and keeps the last entry per student ID, so no one is counted twice.
6. **Creates department-level views**: Department → Program → Gender diagrams for Electrical, Mechanical, and Computer Science and IT, with counts shown in each node label.
