# Esa Unggul University Library System

A web-based library system for Esa Unggul University, built with **Flask** and **MySQL** using the **Scrum** method. It replaces manual, paper-based borrowing with a digital flow for members and library staff.

This project is the subject of my first-author paper:

> **Rancang Bangun Sistem Perpustakaan Web Universitas Esa Unggul dengan Metode Scrum untuk Pengelolaan Digital**
> *Jurnal Informatika: Jurnal Pengembangan IT*, Vol. 10 No. 2, 2025 (SINTA 3)

**Results:** all **35 black-box test scenarios passed**, and borrowing transactions ran about **60% more efficiently** than the manual process.

## Features

**Members**
- Register, log in, change or recover password
- Browse the book catalogue
- Borrow and return books, view borrowing details
- Check late-return fines (*denda*)

**Library staff**
- Separate staff login and dashboard
- Manage books, members and staff (CRUD)
- Confirm borrowing and returns
- Set borrowing reminders for members

## Tech stack

| Layer    | Tools                                  |
| -------- | -------------------------------------- |
| Backend  | Python, Flask, Flask-MySQLdb           |
| Database | MySQL (XAMPP)                          |
| Frontend | HTML, CSS, Jinja2 templates            |
| Method   | Scrum, OOP, black-box testing          |

## Database

Six tables (`perpus.sql`): `anggota` (members), `buku` (books), `peminjaman` (borrowing), `pengembalian` (returns), `staff` and `staffreminder`.

## Running locally

1. Start MySQL (e.g. XAMPP), create a database named `perpus` and import `perpus.sql`.
2. Install dependencies:
   ```bash
   cd Sistem_Perpustakaan
   python -m venv .venv
   .venv\Scripts\activate        # Windows  (macOS/Linux: source .venv/bin/activate)
   pip install -r requirements.txt
   ```
3. Check the MySQL settings at the top of `main.py` (default: `localhost`, `root`, no password).
4. Run the app and open `http://localhost:5000`:
   ```bash
   python main.py
   ```

## Project structure

```
Sistem_Perpustakaan/
├── main.py          # main Flask app (members + staff)
├── main3.py, main_m.py   # other versions of the app
├── library.py       # Tkinter desktop prototype
├── templates/       # Jinja2 pages
└── static/          # CSS and images
perpus.sql           # database schema
```

## Author

**Fayza Azzahra** · [GitHub](https://github.com/ffyzhra) · [LinkedIn](https://www.linkedin.com/in/ffyzhra)
