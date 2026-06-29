ArenaConnect 


A full-stack sports tournament management platform for organizers and players.

What it does

ArenaConnect has two user roles:

Organizers — create a profile, publish tournaments with details and a poster image, manage their events
Players — create a profile, browse and filter tournaments by city and sport, view full tournament details in a modal

Tech stack

LayerTechnologyFrontendHTML5, Bootstrap 5.3, jQuery 3.7, AngularJS 1.8 (tournament finder)BackendNode.js + ExpressDatabaseMongoDBFile uploadsMulterSessionlocalStorage (activeUser key)


Project structure

project-root/
├── server.js                  # Express server, all API routes
├── index.html                 # Login / Register page
│
├── DashOrganizer.html         # Organizer dashboard
├── profileOrganizer.html      # Organizer profile (save/update)
├── publish-tournaments.html   # Post a new tournament
│
├── DashPlayer.html            # Player dashboard
├── profilePlayer.html         # Player profile (save/update)
├── tournament-finder.html     # Browse & filter tournaments (AngularJS)
│
├── Styling/                   # CSS files (one per page)
│   ├── dashOrganizer.css
│   ├── dashPlayer.css
│   ├── profileOrganizer.css
│   ├── profilePlayer.css
│   ├── publish-tournaments.css
│   └── tournament-finder.css
│
├── dashboardpics/             # Static images used in the UI
│   └── *.jpg
│
└── uploads/                   # Profile pics & tournament posters (Multer output)
    └── (auto-generated, gitignored)


API routes (server.js)

MethodRoutePurposePOST/loginPlayer/organizer loginPOST/registerNew user registrationPOST/settingsPlayer password updatePOST/settings-organizerOrganizer password updateGET/search-userFetch organizer profile by emailPOST/saveSave organizer profilePOST/updateUpdate organizer profileGET/fetch-profileFetch player profile by emailPOST/save-profileSave player profilePOST/update-profileUpdate player profilePOST/upload-proofUpload player ID proof filePOST/publish-tournamentSave a new tournamentGET/showCitiesDistinct cities for dropdownGET/showGamesDistinct games for dropdownGET/showRecordsFilter tournaments by city + game


Getting started locally

Prerequisites: Node.js 18+, MongoDB running locally or a MongoDB Atlas URI

bash# 1. Clone the repo
git clone https://github.com/your-username/arenaconnect.git
cd arenaconnect

# 2. Install dependencies
npm install

# 3. Set your MongoDB connection string
# Either edit server.js directly, or add a .env file:
# MONGO_URI=mongodb://localhost:27017/arenaconnect
# PORT=3000

# 4. Start the server
node server.js

# 5. Open in browser
# http://localhost:3000
