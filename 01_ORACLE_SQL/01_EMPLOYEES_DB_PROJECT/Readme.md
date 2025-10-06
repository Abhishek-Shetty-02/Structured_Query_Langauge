# 🧑‍💼 HR Database Project

Welcome to the HR Database — a comprehensive relational database designed to manage and analyze human resources data across global operations. This schema is ideal for organizations seeking to streamline employee records, job roles, departmental structures, and geographic hierarchies.

# 📦 Overview

The HR database consists of several interconnected tables that represent key entities in a corporate HR system:

⦁	Employees

⦁	Departments

⦁	Jobs

⦁	Job_History

⦁	Locations

⦁	Countries

⦁	Regions

Each table is structured to support robust queries, data integrity, and scalable HR analytics.

# 🗃️ Table Descriptions

# 👥 Employees

Stores details about each employee.

⦁	employee_id (PK)

⦁	first_name, last_name

⦁	email, phone_number

⦁	hire_date

⦁	job_id (FK → Jobs)

⦁	salary, commission_pct

⦁	manager_id (FK → Employees)

⦁	department_id (FK → Departments)

# 🏢 Departments

Represents organizational departments.

⦁	department_id (PK)

⦁	department_name

⦁	manager_id (FK → Employees)

⦁	location_id (FK → Locations)

# 💼 Jobs

Defines job roles and salary ranges.

⦁	job_id (PK)

⦁	job_title

⦁	min_salary, max_salary

# 📜 Job_History

Tracks employee job changes over time.

⦁	employee_id (PK, FK → Employees)

⦁	start_date, end_date

⦁	job_id (FK → Jobs)

⦁	department_id (FK → Departments)

# 📍 Locations

Details physical office locations.

⦁	location_id (PK)

⦁	street_address, postal_code

⦁	city, state_province

⦁	country_id (FK → Countries)

# 🌍 Countries

Represents countries where the company operates.

⦁	country_id (PK)

⦁	country_name

⦁	region_id (FK → Regions)

# 🗺️ Regions

Defines global regions.

⦁	region_id (PK)

⦁	region_name

# 🔗 Relationships

Regions → Countries → Locations → Departments → Employees → Jobs
                                       ↘︎ Job_History ↙︎

This schema supports complex joins and queries such as:

⦁	Employee tenure and job transitions

⦁	Departmental salary analysis

⦁	Geographic distribution of offices and staff

⦁	Managerial hierarchies
