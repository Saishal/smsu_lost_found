# SMSU Lost & Found 🔍
A centralized Lost & Found portal for SMSU students and faculty to report, search, and reclaim lost items safely and easily.

## Tech Stack
* **Backend:** Python, Flask, SQLAlchemy
* **Frontend:** Jinja2 HTML templates with static CSS & JS served from the `static/` folder
* **Security & Middleware:**
  * Flask-WTF (CSRF protection)
  * Flask-Login (session auth)
  * Werkzeug (password hashing, secure file uploads)
  * Email Validator

## Project Structure

```
smsu-lost-found/
├─ templates/
│  ├─ base.html             # Shared layout with nav & notifications
│  ├─ index.html            # Landing page with recent items
│  ├─ browse.html           # Search & filter all listings
│  ├─ report.html           # Report a lost or found item
│  ├─ item_detail.html      # Item view with claim flow
│  ├─ dashboard.html        # User's reported & claimed items
│  └─ admin_dashboard.html  # Admin controls & moderation
├─ static/                  # CSS, JS, and uploaded images
├─ models.py                # SQLAlchemy models (User, Item, Claim, Notification)
├─ forms.py                 # WTForms (Login, Register, ReportItem, Search)
├─ app.py                   # Flask app entry point & route handlers
├─ config.py                # App configuration
├─ create_admin.py          # CLI script to seed an admin user
├─ requirements.txt
└─ .gitignore
```
