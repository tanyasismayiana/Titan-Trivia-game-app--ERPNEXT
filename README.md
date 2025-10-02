🧠 Titan Trivia

A fun and interactive quiz game built on the Frappe Framework, where players answer randomly generated questions, track their scores, and receive leaderboard updates via email.

🚀 Features

🎲 Random Question Generator – serves unique questions to each player

✅ Answer Validation – instantly checks if the selected answer is correct

📊 Score Tracking – records correct and incorrect answers

🏆 Leaderboard System – ranks players by performance and sends email updates

📧 Email Notifications – players receive leaderboard standings in their inbox

📈 Reports Dashboard – shows game summary and question stats

🏗️ Tech Stack
Component	Technology
Framework	Frappe Framework

Language	Python, JavaScript
Frontend	Frappe UI, Jinja Templates
Database	MariaDB / MySQL
Email Service	Frappe’s Email Queue System
⚙️ Installation & Setup

Create a new bench

bench init titansoft-games
cd titansoft-games


Create a new site

bench new-site titan.localhost


Get ERPNext (optional)

bench get-app erpnext
bench --site titan.localhost install-app erpnext


Get this app

bench get-app titans_trivia https://github.com/<your-username>/titans_trivia.git
bench --site titan.localhost install-app titans_trivia


Start the server

bench start


Access the game
Visit:

http://titan.localhost


and enjoy playing 🎮

🧩 Game Flow

Player logs in or signs up.

A random question is displayed.

Player selects an answer → system validates instantly.

The result (✅ correct / ❌ wrong) appears in a Frappe popup.

When the player closes the popup, the page refreshes with a new question.

All responses are recorded in the Quiz History doctype.

A leaderboard email is generated and sent periodically.

📂 Project Structure
titans_trivia/
│
├── api/                    # Python API methods (quiz logic, scoring)
├── public/                 # Static JS, CSS, images
├── templates/              # HTML / Jinja templates
├── www/                    # Web pages (quiz interface)
├── quiz_api.py             # Main quiz endpoints
├── leaderboard_email.py    # Email leaderboard generator
├── hooks.py                # App hooks and schedulers
└── config/                 # App configuration

🧠 Core Doctypes
Doctype	Description
Quiz Question	Stores question text and options (A–D)
Quiz Answer	Tracks player’s selected answer
Quiz History	Records all played questions with correctness info
📧 Leaderboard Emails

A background job (leaderboard_email.py) runs periodically to:

Collect all player scores

Generate leaderboard rankings

Send each player their position by email

🔮 Future Improvements

Add categories (sports, tech, general knowledge, etc.)

Add multiplayer mode

Introduce time limits and streak bonuses

Improve UI with animations and progress bars

🧑‍💻 Developer

Built with ❤️ by Tanya
A Frappe & ERPNext enthusiast learning full-stack app development using the Frappe Framework.

📝 License

This project is licensed under the MIT License — feel free to fork, modify, and contribute.
