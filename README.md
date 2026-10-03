
# Factory Downtime Tracking System

A centralized, real-time **Factory Downtime Tracking System** designed to monitor, log, and analyze production line interruptions. This system helps manufacturing plants minimize operational delays, identify root causes of equipment failure, and improve Overall Equipment Effectiveness (OEE).

## 🚀 Features

*   **Real-Time Downtime Logging:** Quick reporting of machine stops by operators.
*   **Categorized Root Causes:** Classification of downtime (e.g., mechanical failure, electrical issues, material shortage, scheduled maintenance).
*   **Live Dashboard:** Real-time visualization of active downtimes and machine statuses.
*   **Analytics & Reporting:** Generates insights on Mean Time to Repair (MTTR), Mean Time Between Failures (MTBF), and total lost production hours.
*   **Role-Based Access Control (RBAC):** Distinct interfaces and permissions for Operators, Maintenance Technicians, and Plant Managers.

## 🛠️ Tech Stack

*   **Frontend:** HTML5, CSS3, JavaScript (or specify framework like React / Vue)
*   **Backend:** Node.js / Python (Flask/Django) / C# (.NET)
*   **Database:** PostgreSQL / MySQL / MongoDB
*   **Deployment:** Docker / AWS / Local Server

## 📦 Installation & Setup

Follow these steps to get the project running locally.

### Prerequisites

Ensure you have the following installed:
*   [Node.js](https://nodejs.org) (v18 or higher) OR [Python](https://python.org) (v3.10 or higher)
*   [Database Client] (e.g., MySQL, PostgreSQL)

### Step-by-Step Guide

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd factory-downtime-system
   ```

2. **Install dependencies:**
   ```bash
   # For Node.js projects
   npm install
   
   # For Python projects
   pip install -r requirements.txt
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the root directory and add your configurations:
   ```env
   PORT=5000
   DATABASE_URL=your_database_connection_string
   JWT_SECRET=your_secret_key
   ```

4. **Initialize the Database:**
   ```bash
   # Run migrations if applicable
   npm run db:migrate 
   # or
   python manage.py migrate
   ```

5. **Start the application:**
   ```bash
   npm start
   # or
   python app.py
   ```
   The application should now be running at `http://localhost:5000`.

## 🖥️ Usage

1. **Operators:** Log a new downtime event immediately when a machine stops, selecting the machine ID and the initial symptom.
2. **Technicians:** Acknowledge the downtime event, update the status to "In Repair," and log the resolution details once fixed.
3. **Managers:** Access the analytics dashboard to review weekly/monthly downtime trends and download CSV/PDF reports.

## 📊 Database Schema (Core Tables)

*   `Users`: Stores information for operators, technicians, and managers.
*   `Machines`: Contains list of factory assets, assembly lines, and locations.
*   `DowntimeLogs`: Captures `start_time`, `end_time`, `reason_code`, `machine_id`, and `logged_by`.

## 🤝 Contributing

Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request.
