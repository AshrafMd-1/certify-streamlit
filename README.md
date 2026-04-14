# Certify

> **Archived** — This project has been archived due to the deprecation of **Deta Base** and **Deta Drive**, which are no longer supported. The application is no longer functional in its current state.

**Certify** is a Streamlit-based web application for generating and distributing personalized certificates. It lets organizers manage events, upload participant lists, design certificate templates, and lets participants download their own certificates — all from a browser.

---

## Features

- **Authentication** — Secure login system for organizers
- **Event Management** — Create and manage events with a name and description
- **Participant Upload** — Upload participants via CSV, preview and edit the list before saving
- **Certificate Templates** — Upload PNG/JPG certificate templates per event
- **Certificate Customization** — Visually position and style the participant name on the certificate (font size, color, X/Y position, horizontal alignment)
- **Self-Service Download** — Participants can find their event, select their name, preview, and download their certificate

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend / App | [Streamlit](https://streamlit.io) |
| Image Processing | [Pillow](https://python-pillow.org) |
| Data Manipulation | [Pandas](https://pandas.pydata.org) |
| Database & Storage | [Deta Base + Deta Drive](https://deta.space) *(deprecated)* |
| Font | Great Vibes (TTF) |

## Project Structure

```
certify-streamlit/
├── app.py                      # Login page (entry point)
├── pages/
│   ├── profile.py              # Organizer profile
│   ├── create_event.py         # Create a new event
│   ├── add_participants.py     # Upload participants CSV
│   ├── add_template.py         # Upload certificate template image
│   ├── customise_certificate.py # Visually configure name placement
│   ├── view_event.py           # View event details
│   ├── edit_profile.py         # Edit organizer profile
│   ├── change_password.py      # Change password
│   ├── about.py                # About page
│   └── get_certificate.py      # Public page for participants to get certificates
├── config/
│   ├── db.py                   # Deta Base/Drive connection
│   └── menu.py                 # Navigation menu
├── utils/
│   ├── common.py               # Shared utilities
│   ├── css.py                  # Custom CSS
│   └── event.py                # Event helpers
├── font/
│   └── GreatVibes-Regular.ttf  # Certificate font
├── requirements.txt
└── .streamlit/config.toml
```

## Why It's Archived

Certify was built on [Deta Space](https://deta.space)'s free database (`Deta Base`) and file storage (`Deta Drive`). Deta deprecated these services, making the backend non-functional. A migration to an alternative backend (e.g., Supabase, Firebase, or a self-hosted database) would be required to revive the project.

## License

This project is archived and provided as-is for reference purposes.
