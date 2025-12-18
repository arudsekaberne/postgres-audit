# Postgres-Audit

## 🚀 Overview
postgres-audit is a Python-based tool designed to audit PostgreSQL logs and generate comprehensive reports. It automates the process of extracting, processing, and reporting on PostgreSQL audit logs, making it easier to monitor and maintain your database systems.

## ✨ Features
- **Automated ETL**: Automatically processes PostgreSQL audit logs.
- **Email Notifications**: Sends email notifications for completed batches.

## 🛠️ Tech Stack
- **Programming Language**: Python
- **Libraries and Tools**:
  - `smtplib`: Email sending
  - `pytz`: Timezone handling
  - `paramiko`: SSH connections
  - `jinja2`: Template rendering
  - `pandas`: DataFrame operations
  - `sqlalchemy`: Database interactions
  - `tabulate`: Pretty printing DataFrames

## 📦 Installation

### Prerequisites
- Python 3.8+
- PostgreSQL
- SSH access to the server

### Quick Start
```bash
# Clone the repository
git clone https://github.com/arudsekaberne/postgres-audit.git

# Navigate to the project directory and set up environment variables in .env file
cd postgres-audit

# Run the audit job automatically
python main.py --auto
```

## 🔧 Configuration
- **Environment Variables**: Set up your database and SSH credentials in the `.env` file.
- **SQL Scripts**: Customize the SQL scripts in the `dependencies/sql` directory to fit your specific needs.
- **Email Notifications**: Configure the SMTP settings in the `.env` file to send email notifications.
  
## 🎯 Usage

### Basic Usage
```python
# Example: Running the audit job manually
python main.py
```

## 📁 Project Structure
```
postgres-audit/
├── .env
├── main.py
├── vault.py
├── dependencies/
│   ├── __init__.py
│   ├── assets/
│   │   ├── __init__.py
│   │   └── pgaudit_email_template.html
│   ├── sql/
│   │   ├── 1_stg_postgre_log.sql
│   │   ├── 2_stg_pgaudit_session_log.sql
│   │   ├── 3_lnd_postgre_log.sql
│   │   ├── 4_lnd_pgaudit_session_log.sql
│   │   └── 5_lnd_postgre_log_run.sql
│   ├── utilities/
│   │   ├── __init__.py
│   │   ├── credential.py
│   │   ├── dataframe.py
│   │   ├── environment.py
│   │   ├── outlook.py
│   │   ├── postgre.py
│   │   ├── ssh.py
│   │   └── validation.py
├── requirements.txt
└── README.md
```
