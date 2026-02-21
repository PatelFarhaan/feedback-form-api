# Feedback Form

A simple feedback collection web application built with Flask. Users submit their feedback via a web form, data is stored in a database, and an email notification is sent to the administrator upon each submission.

## Tech Stack

- **Language:** Python 3
- **Framework:** Flask
- **Database:** SQLAlchemy (supports SQLite, PostgreSQL, MySQL)
- **Email:** SMTP (smtplib)
- **Frontend:** HTML, CSS

## Features

- Clean feedback submission form with email and experience fields
- Duplicate email detection to prevent repeat submissions
- Email notifications to administrators on new feedback
- Persistent storage with SQLAlchemy ORM
- Responsive UI with custom CSS styling

## Prerequisites

- Python 3.7+
- pip

## Installation & Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Feedback-Form
   ```

2. **Create and activate a virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your actual values
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

   The app will be available at `http://localhost:5000`.

## Environment Variables

| Variable             | Description                      | Example                   |
|----------------------|----------------------------------|---------------------------|
| `SECRET_KEY`         | Flask secret key                 | `a-random-secret-string`  |
| `DATABASE_URI`       | Database connection string       | `sqlite:///feedback.db`   |
| `SMTP_HOST`          | SMTP server host                 | `smtp.gmail.com`          |
| `SMTP_PORT`          | SMTP server port                 | `587`                     |
| `SMTP_USERNAME`      | SMTP email address               | `your-email@gmail.com`    |
| `SMTP_PASSWORD`      | SMTP email password/app key      | `your-app-password`       |
| `NOTIFICATION_EMAIL` | Recipient for notifications      | `admin@example.com`       |

## Project Structure

```
Feedback-Form/
├── app.py              # Application entry point with routes and models
├── requirements.txt    # Python dependencies
├── .env.example        # Environment variable template
├── Dockerfile          # Docker configuration
├── Makefile            # Common development commands
├── src/
│   ├── index.html      # Feedback form page
│   └── success.html    # Success confirmation page
└── static/
    └── main.css        # Application styles
```

## API Endpoints

| Method | Endpoint   | Description                          |
|--------|------------|--------------------------------------|
| GET    | `/`        | Feedback form page                   |
| POST   | `/success` | Submit feedback and send notification|

## License

This project is licensed under the MIT License.
