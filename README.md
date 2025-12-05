# Fintech-Portfolio-Project – Power BI Dashboard
A fully interactive **Power BI dashboard** to monitor fintech product development projects – from high-level portfolio health to detailed task and milestone tracking.  The report is built on a fictional fintech company that manages multiple payment solutions (InstantPay, OpenBank API, Tap-to-Pay POS, etc.) across different regions and departments.

## 📁 Repository Structure

```text
.
├── README.md
├── /pbix
│   └── Fintech_Project_Portfolio.pbix
├── /data
│   ├── Fintech_Projects_Challenge32_Dataset.xlsx
│   └── World Flags_Dataset_Addition.xlsx
└── /images
    ├── page1_overview.png
    ├── page2_timeline.png
    └── page3_details.png
🎯 Project Objective

Goal:
Use project, task, employee, and milestone data to answer:

Are fintech projects delivered on time and within budget?

Which departments, regions, and project managers perform best?

Where do we see delays, blocked work, or budget overruns?

How do experience level & hourly rates affect project cost?

Which task statuses or phases cause the most rework/delay?

The dashboard is designed for Project Managers / PMO / Delivery Leads in a fintech organization.

📊 Dashboard Pages
1️⃣ Project Overview

High-level portfolio view.

Key features:

KPI cards

Total Projects

Total Planned Budget vs Actual Budget

Total Net Benefit

Project Duration (days)

Average Completion %

Visuals

Total Actual vs Planned Budget (gauge / donut)

Hours Efficiency by Department

Total Planned vs Actual Hours + Variance %

Milestone Completion Trend by Month

Task Status Distribution

Completed / In Progress / Blocked / On Hold / Not Started

Slicers

Project

Department

City / Country

Status

Year / Month

2️⃣ Project Timeline

Time-oriented view focusing on durations, delivery performance, and milestones.

Key features:

KPI cards:

Project Duration (Days)

Average Project Duration

Delayed Projects

Average Delay (Days)

On-Time Delivery %

Visuals:

Project Duration Timeline (bar chart / pseudo-Gantt)

Project Delivery Performance (scatter: Duration vs Completion %, colored by Status)

Milestone Table with:

ProjectID, MilestoneName, Year, Quarter, Month, Day, Status

Conditional formatting for milestone status

3️⃣ Project Details

Drill-through page for deep dive into a single project.

Table columns (example):

ProjectID

DepartmentID

ProjectManagerID

ProductName

RiskLevel

StartDate

EndDate

ActualBudget (EUR)

Completion %

Status

Formatting:

Status color rules:

Completed → 🟩 #4CAF50

In Progress → 🔵 #2196F3

On Track → 🔷 #03A9F4

Delayed → 🔴 #F44336

Not Started → ⚪ #9E9E9E

Completion % conditional formatting:

≥ 80% → Green

50–80% → Orange

< 50% → Red

Drill-through:

Right-click a project on Page 1 or 2 → Drill through → Project Details

Page 3 filters automatically to the selected ProjectID.

🧱 Data Model

Fact tables:

Projects

Tasks

Milestones

Dimension tables:

Employees

Departments

Date Dim (calculated table)

Banderas (Country flags / codes – optional)

Core relationships:

Projects[ProjectID] 1 ─── * Tasks[ProjectID]

Projects[ProjectID] 1 ─── * Milestones[ProjectID]

Departments[Department_ID] 1 ─── * Projects[DepartmentID]

Employees[EmployeeID] 1 ─── * Tasks[AssignedTo (EmployeeID)]
🎨 Design & UX

Left navigation sidebar with:

Dashboard Home

Project Overview

Project Timeline

Project Details

Sidebar color: #4356C9

Background: soft light (#F5F7FF)

Consistent typography (Segoe UI / Inter)

Card-based layout with shadows and rounded corners

Slicers embedded in the sidebar (Year, Project Type, Department)

🚀 How to Use This Report

Clone / Download this repo:

git clone https://github.com/<your-username>/<your-repo-name>.git


Open the .pbix file in Power BI Desktop.

Ensure the data source paths for the Excel files in /data are correct
(if needed, go to: Transform Data → Data source settings → Change Source).

Refresh the report:

Home → Refresh

Interact with the report:

Use the sidebar buttons or page tabs to navigate between pages.

Use slicers to filter by Year, Department, Project Type, Project, etc.

Drill through from Overview/Timeline → Project Details by right-clicking a project.

🛠 Tech Stack

Power BI Desktop

Data source: Excel (.xlsx)

Modeling: Star schema with fact/dimension tables

DAX for measures & calculated tables

Custom visuals: native Power BI visuals (no marketplace visuals required)

🚧 Possible Improvements

Add RLS (Row Level Security) by department or region

Add predictive metrics (risk of delay, forecasted budget)

Integrate with live sources (SQL, Databricks, APIs)

Add bookmarks for different personas: PM, Finance, Leadership

Add tooltips pages for deeper hover insights

👤 Author

👤 BASTIPADU ARAVINDTEJA Aspiring Data Analyst
📧 Contact: aravindtejaprabha@gmail.com,9515748927
🌐 GitHub: itsmeprabha75
🌐Linkedin: www.linkedin.com/in/aravintejaprabha75

If you liked this project or have feedback, feel free to connect with me on LinkedIn or open an issue / PR in this repo. 😊
