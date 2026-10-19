# Cplusplus-program-CS340
# CS 340 Client Server Development

## Project Overview

For this project, I developed an interactive dashboard for Grazioso Salvare to identify shelter dogs that match search-and-rescue training profiles. The application uses Python, MongoDB, Dash, Plotly, and Dash Leaflet.

The dashboard includes filters for Water Rescue, Mountain or Wilderness Rescue, and Disaster or Individual Tracking. A Reset option restores the unfiltered data. The interactive table, breed distribution chart, and selected animal map help users explore the results.

This repository contains the final dashboard code, the reusable CRUD Python module, and the Project Two README Word document.

## Writing Maintainable, Readable, and Adaptable Programs

I write maintainable programs by separating responsibilities, using descriptive names, and organizing repeated operations into reusable functions. Comments and documentation explain the purpose of the code and how its components work together.

The CRUD Python module from Project One demonstrates this approach. It handles MongoDB connections and database operations separately from the dashboard interface. In Project Two, the dashboard calls the module's read method with query dictionaries instead of repeating database access code inside each widget.

This separation made it easier to test queries, investigate problems, and update the interface without changing the database module. It also kept the dashboard callbacks focused on responding to user input and displaying results.

I could reuse the CRUD module in another dashboard, a reporting script, or a web service that needs access to the shelter database. Its configurable connection settings also provide a starting point for working with another MongoDB collection. A future improvement would be to load credentials from environment variables rather than placing the course training credentials in the application code.

## Approaching Problems as a Computer Scientist

I approach problems by translating the client's goals into smaller requirements that I can implement and test. For Grazioso Salvare, this meant turning rescue profiles into database filters based on animal type, breed, sex, and age. I checked the query results before connecting those filters to the dashboard controls.

I then tested how the components worked together. Selecting a rescue profile needed to update the table and breed chart, while selecting a table row needed to update the map. I also checked empty results and confirmed that Reset cleared table filters and restored the starting state.

Compared with a smaller assignment focused on one function, this project required me to think about the complete path from stored data to user interaction. A correct database query was only one part of the solution; the interface also needed to make the results understandable and keep the widgets consistent.

For future client projects, I would clarify the required data fields and filtering rules early, inspect the quality of the available data, and build the application in stages. I would continue using reusable database operations and tests for both normal and unexpected inputs. As the dataset grows, I would also evaluate indexes and server-side pagination to keep queries and the interface responsive.

## What Computer Scientists Do and Why It Matters

Computer scientists turn practical problems into systems that process information and support useful decisions. Their work includes understanding requirements, organizing data, choosing appropriate tools, testing behavior, and making software understandable to the people who use and maintain it.

For a company like Grazioso Salvare, this dashboard can reduce the time spent manually searching shelter records. Staff can select a rescue profile, compare matching animals, examine breed distributions, and view the location associated with a selected record.

The dashboard supports an initial screening process rather than deciding whether an animal is suitable for training. Staff still need to evaluate health, behavior, availability, and other factors that the filters do not establish. Presenting the available data clearly helps them focus their attention and make better-informed follow-up decisions.

## Running the Project

The dashboard requires the course MongoDB dataset, the CRUD Python module, the logo image, and the Python dependencies listed in requirements.txt.

Open ProjectTwoDashboard.ipynb in the configured Codio environment and run the notebook from the directory containing the supporting files. The accompanying Project Two README Word document provides setup instructions, screenshots, tool explanations, and testing details.
