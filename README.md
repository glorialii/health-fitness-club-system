### COMP 3005 Final Project
## Health & Fitness Club Management System
Group Members: Alex Bon & Gloria Li

This project is our final project for COMP 3005
We built a CLI-based Health & Fitness Club Management System that uses PostgreSQL for the backend and Python (psycopg2) for the application layer

The system supports the three main roles required in the specs:

- Member: register/login, update profile, track metrics, view goals, and dashboard summaries
- Trainer: set availability and look up member progress
- Admin: room/class scheduling feature

## Course requirements included:

PostgreSQL DB w DDL.sql + DML.sql
Minimum 4 Member operations, 2 Trainer operations, and 2 Admin operations (we might ahve exceeded this)
A separate write-up with ERD, Relational Mapping, and Normalization (2NF/3NF) stored under /docs

1. Tech Stack

-Python
-PostgreSQL
-psycopg2 (DB connection)

Text-based CLI (menu-driven)

2. Project Structure
Final Project
│  README.md                  # Project overview + how to run
│
├── sql
│   ├── DDL.sql               # Create tables + constraints
│   └── DML.sql               # data (members, trainers...)
│
├── app
│   ├── app.py                # Main CLI entry point
│   ├── auth.py               # Login + registration
│   ├── member.py             # Member operations (metrics, goals, profile)
│   ├── trainer.py            # Trainer ops (availability, lookup)
│   ├── admin.py              # Admin ops (rooms, classes)
│   ├── db.py                 # DB connection + resetDB()
│   ├── state.py              # sesh tracking
│   └── __pycache__/          # python cache files
│
└── docs
    ├── ERD.pdf               # entities + relationships
    ├── Normalization.pdf     # 2NF/3NF proof (table + conclusion)
    ├── Mapping.pdf           # ER -> relational schema mapping
    └── Report.pdf            # short summary + assumptions


3. how 2 run the project

Make sure PostgreSQL is installed and running.
Create a database, name it "Final Project"

Run the DDL and DML scripts:
\i sql/DDL.sql;
\i sql/DML.sql;

Install 'pip install psycopg2' in the terminal

Run the CLI: (MAKE SURE U ARE IN THE FOLDER)
python app/app.py

4. Test Accounts (for demo)

Admin Examples
Email: admin@gmail.com
Password: administrator

Member Examples (username / password)
(pls refer to DML for more accounts)

gloria@gmail.com / gloria

alex@live.ca / alex

Trainer Examples
george.koh@healthnfitness.com / george
gloria.li@healthnfitness.com / gloria

5. Documentation (under /docs)

The following files are included in SUBMISSION:
ERD.pdf: entity sets, relationships, cardinalities
Normalization.pdf: full 2NF/3NF proof (table + conclusion)
Mapping.pdf: ER → relational mapping
Report.pdf: short summary, assumptions, and design notes