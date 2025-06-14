# Music Database – Client-Server Application in Python

This project implements a client-server application in Python to manage a simple music database, including users, bands, and albums. The system allows adding, removing, and displaying records using custom commands through a terminal-based client interface.

## 📌 Project Objective

To practice client-server communication and database integration using Python sockets and SQLite.

## 🧱 Architecture

- **Client (`client/client.py`)**: Sends commands to the server via TCP sockets.
- **Server (`server/server.py`)**: Receives and processes commands using an internal SQLite database.
- **Database (`server/ad14.db`)**: Stores users, bands, and albums.
- **SQL Schema (`server/ad14.sql`)**: Initializes the database structure.
- **Helper Module (`server/sqlite.py`)**: Handles SQL operations internally.

## 🔧 Technologies Used

- Python 3.x
- SQLite
- `socket` module
- Command-line interface

## 🚀 How to Run

1. Start the server:
```bash
cd server
python3 server.py
```

2. In another terminal, run the client:
```bash
cd client
python3 client.py
```

3. Use one of the following commands:

### Add:
- `ADD USER <username> <password> <name>`
- `ADD BANDA <genre> <name> <year>`
- `ADD ALBUM <band_id> <name> <album_year>`
- `ADD RATING <user_id> <album_id> <rating>` (rating = M, m, S, B, MB)

### Remove:
- `REMOVE USER <user_id>`
- `REMOVE BANDA <band_id>`
- `REMOVE ALBUM <album_id>`
- `REMOVE ALL USERS | BANDAS | ALBUNS`
- `REMOVE ALL ALBUNS_B <band_id>`
- `REMOVE ALL ALBUNS_U <user_id>`
- `REMOVE ALL ALBUNS <rating>`

### Show:
- `SHOW USER <user_id>`
- `SHOW BANDA <band_id>`
- `SHOW ALBUM <album_id>`

## 📄 Documentation

See `Enunciado.pdf` for assignment description and original requirements.

## 👩‍💻 Author

- João Nunes

## 📃 License

This project is for academic and educational use only.
