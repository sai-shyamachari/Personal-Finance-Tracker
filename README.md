# Personal-Finance-Tracker
A privacy-focused financial dashboard built with Tailwind CSS and JavaScript, featuring local data persistence, debt management, and automated PDF report generation.

## 📌 Project Overview

Managing personal finances requires a clear distinction between daily spending and money owed to or by others. XpenseFlow provides a streamlined, local-first interface to manage these two "buckets" of money without the need for a complex backend or database.

1. Dual-Entry System: Separate modules for "Daily Logs" (general spending/income) and "Pending Entries" (tracking money lent to or borrowed from people).

2. Dynamic Balance Logic: Automatically calculates your real-time wallet balance by factoring in starting capital, credits, expenses, and pending debts.

3. Budget Guardrail: Visual progress bar that tracks monthly spending against a user-defined budget, changing color as you approach your limit.

4. Interactive Calendar: A custom-built calendar interface to filter transactions and view historical data by specific dates.

5. PDF Report Engine: Integrated one-click export to generate Weekly or Monthly financial summaries for offline record-keeping.

6. Privacy-First: All data is stored exclusively in the browser's localStorage, ensuring your financial data never leaves your device.


## 🛠️ Tech Stack

Frontend: HTML5, Tailwind CSS (via CDN)

Scripting: Vanilla JavaScript (ES6+)

Libraries: jsPDF (PDF Generation), Google Fonts (Inter)

Storage: Browser LocalStorage API

## 🚀 How to run this project?

Since this project is built using Vanilla web technologies, it does not require a complex installation:

1. Clone the Repository:

git clone https://github.com/sai-shyamachari/xpenseflow.git
cd xpenseflow

2. Run the Application:

Simply double-click the index2.html file to open it in your preferred web browser (Chrome, Edge, or Brave recommended).

3. Initial Setup:

Enter your name, starting balance, and monthly budget in the welcome modal to begin tracking.


## 📁 File Structure

xpenseflow/

├── XpenseFlow.html      # Main application file (HTML, CSS, and JS)

├── README.md        # Project documentation

└── .gitignore       # Standard git ignore file


## 📊 Data Management Logic

The application utilizes a specific state management pattern to ensure data integrity across sessions:

State Object: A centralized JSON object stores generalTransactions and pendingTransactions separately.

Debt Logic: "I Gave" (Money you will get back) is treated as a temporary reduction in your current wallet, while "I Took" (Money you will give back) is treated as a temporary increase.

Persistence: Every action (adding or deleting a transaction) triggers the saveState() function, which stringifies the current data into a single localStorage key (exp_v3_fixed).

## ✍️ Author & Contact

Name: Sai Shyam Achari

GitHub: https://github.com/sai-shyamachari

LinkedIn: www.linkedin.com/in/sai-shyam-achari-5870a0373

Email: saishyamachari@gmail.com
