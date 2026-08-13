# ArenaConnect

A full-stack sports tournament management platform for organizers and players.

ArenaConnect simplifies tournament publishing, discovery, and profile management through a responsive web interface and a Node.js + MongoDB backend.

---

## Features

### Organizer
- Create and manage organizer profile
- Publish tournaments with:
  - title
  - city
  - sport
  - date and venue
  - description
  - poster image upload
- Update tournament information

### Player
- Create and manage player profile
- Browse available tournaments
- Filter tournaments by **city** and **sport**
- View complete tournament details in a modal window

---

## Tech Stack

| Layer | Technology |
|------|------------|
| Frontend | HTML5, Bootstrap 5.3, jQuery 3.7, AngularJS 1.8 |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| File Uploads | Multer |
| Session Handling | localStorage (activeUser) |

---

## Project Structure

```text
project-root/
│
├── server.js
├── index.html
├── DashOrganizer.html
├── profileOrganizer.html
├── publish-tournaments.html
├── DashPlayer.html
├── profilePlayer.html
├── tournament-finder.html
│
├── Styling/
│   ├── dashOrganizer.css
│   ├── dashPlayer.css
│   ├── profileOrganizer.css
│   ├── profilePlayer.css
│   ├── publish-tournaments.css
│   └── tournament-finder.css
│
├── dashboardpics/
│
└── uploads/
```

---

## API Endpoints

### Authentication
- POST `/login`
- POST `/register`

### Organizer Profile
- GET `/search-user`
- POST `/save`
- POST `/update`

### Player Profile
- GET `/fetch-profile`
- POST `/save-profile`
- POST `/update-profile`
- POST `/upload-proof`

### Tournaments
- POST `/publish-tournament`
- GET `/showCities`
- GET `/showGames`
- GET `/showRecords`

---

## Getting Started

### Prerequisites
- Node.js 18+
- MongoDB running locally or a MongoDB Atlas URI

### Clone the repository

```bash
git clone https://github.com/your-username/arenaconnect.git
cd arenaconnect
```

### Install dependencies

```bash
npm install
```

### Configure environment variables

Create a `.env` file:

```env
MONGO_URI=mongodb://localhost:27017/arenaconnect
PORT=3000
```

### Start the server

```bash
node server.js
```

### Open in browser

```text
http://localhost:3000
```

---

## Future Improvements

- JWT authentication
- Password hashing with bcrypt
- Role-based access control
- Tournament registration and payment integration
- Admin dashboard
- Cloud storage for uploads

---

## Author

**Anshpreet Kaur**

- Full Stack Developer
- MERN Stack | Web Development | MongoDB | Node.js

GitHub: https://github.com/ansh625

---

## License

This project is licensed under the **MIT License**.
