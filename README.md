Expense Tracker
A web-based Expense Tracker built with Python and Django. It lets users record everyday expenses, review transaction history, and understand spending through date-based summaries, category totals, and charts.
Features
- Add expenses with a name, amount, and category.
- View transaction history with the date, name, category, and amount.
- Edit and delete expenses when a transaction needs to be updated or removed.
- See total spending across all saved expenses.
- Review spending summaries for the last 7 days, 30 days, and 365 days.
- View daily totals to understand spending over time.
- Compare category-wise spending.
- Visualize expenses with interactive doughnut, line, and bar charts.
- Responsive dark dashboard styled with Tailwind CSS and custom CSS.
Tech Stack
Technology	Purpose
Python	Main programming language
Django	Web framework, routing, forms, ORM, and admin
SQLite	Database
HTML and CSS	Page structure and styling
Tailwind CSS	Utility-based styling, loaded through its browser CDN
JavaScript	Dashboard interactions and chart data
Chart.js	Expense visualizations


Project Structure
expensetracker/
└── mysite/
    ├── manage.py
    ├── db.sqlite3
    ├── mysite/
    │   ├── settings.py
    │   ├── urls.py
    │   ├── asgi.py
    │   └── wsgi.py
    └── myapp/
        ├── migrations/
        ├── templates/
        │   └── myapp/
        │       ├── base.html
        │       ├── index.html
        │       └── edit.html
        ├── admin.py
        ├── forms.py
        ├── models.py
        ├── urls.py
        └── views.py
Getting Started
1. Install Python
Install a supported Python version. The project was created with Django 6, so Python 3.12 or newer is recommended.

Check your installation:
python --version
2. Clone the repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
Replace the URL and repository name with your own GitHub details.
3. Open the Django project directory
cd mysite
4. Create and activate a virtual environment
Windows (Command Prompt):
python -m venv .venv
.venv\Scripts\activate
Windows (PowerShell):
python -m venv .venv
.\.venv\Scripts\Activate.ps1
macOS / Linux:
python3 -m venv .venv
source .venv/bin/activate
5. Install Django
python -m pip install --upgrade pip
python -m pip install "Django>=6.0,<7.0"
6. Apply database migrations
python manage.py migrate
7. Start the development server
python manage.py runserver
Open http://127.0.0.1:8000/ in your browser.

Stop the server with Ctrl + C.
Note: Tailwind CSS and Chart.js are loaded from CDNs, so an internet connection is needed for those frontend assets.

How to Use
1. Open the dashboard in your browser.
2. Enter an expense name, amount, and category in the Add Expense form.
3. Submit the form to save the expense.
4. Scroll to All Expenses to view, modify, or delete saved records.
5. Review the overview cards, daily totals, category breakdown, and charts to understand your spending.
Data Model
Each expense record contains:
Field	Description
name	Name or description of the expense
amounts	Expense amount, stored as an integer
category	Category assigned to the expense
date	Date and time automatically recorded when the record is saved


The application uses Django's ORM to store and query expense records in SQLite.
Important Notes
- This is a learning/personal project and is configured for local development, not production deployment.
- The current project settings have DEBUG = True, an empty ALLOWED_HOSTS, and a development secret key. Review Django's deployment checklist and configure environment variables, allowed hosts, HTTPS, and production settings before deploying publicly.
- The dashboard currently uses a basic expense form; authentication and per-user expense separation are not implemented.
- The amount field is an integer, so decimal amounts are not supported by the current model.
- If you create a fresh database, run python manage.py migrate before starting the server.
- Do not commit a local virtual environment, personal database data, or real secret keys to a public repository.
Future Improvements
- Add user registration and login, with expenses separated by account.
- Support decimal currency amounts and currency formatting.
- Add search, filters, and date-range reports.
- Add monthly budgets and budget-limit alerts.
- Export expense reports to CSV or PDF.
- Improve form validation and add automated tests.
- Prepare secure production settings and deploy the application.
Contributing
Suggestions and improvements are welcome.
1. Fork the repository.
2. Create a branch for your change.
3. Make and test your changes.
4. Submit a pull request with a clear description.
License
No license has been specified yet. Add a LICENSE file before presenting the project as open source.
