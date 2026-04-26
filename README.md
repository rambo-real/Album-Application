# Album Application

A full-stack media management application that allows users to create albums and upload photos with drag-and-drop functionality. Built with a React frontend and a Spring Boot REST API backend.

---

## Features

- **User Authentication** — Register, login, and logout with JWT-based authentication
- **Album Management** — Create, edit, and delete albums
- **Photo Upload** — Drag-and-drop or click-to-select file upload with multi-file support
- **Photo Grid** — View uploaded photos in a responsive grid layout
- **Photo Management** — Edit and delete individual photos within an album
- **Protected Routes** — All album and photo operations require authentication
- **Responsive UI** — Built with Material UI for a clean, responsive experience

---

## Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| React 18 | UI framework |
| Material UI (MUI v5) | Component library |
| Redux Toolkit | State management |
| React Router v6 | Client-side routing |
| Axios | HTTP client with JWT auth headers |
| react-dropzone | Drag-and-drop file upload |
| Formik + Yup | Form handling and validation |
| Framer Motion | Animations and transitions |

### Backend
> The frontend proxies API requests to a Spring Boot REST API running on `http://localhost:8080`. See the backend repository for setup.

---

## Project Structure

```
src/
├── client/
│   └── client.js           # Axios API client with JWT auth helpers
├── components/             # Reusable UI components
├── layout/
│   └── MainLayout/         # App shell (header, drawer, navigation)
├── pages/
│   ├── albums/
│   │   ├── albums.js       # Albums list view
│   │   ├── albumAdd.js     # Create new album
│   │   ├── albumEdit.js    # Edit album details
│   │   ├── albumShow.js    # View album and its photos
│   │   ├── albumUpload.js  # Drag-and-drop photo upload
│   │   └── PhotoEdit.js    # Edit individual photo
│   └── authentication/
│       ├── Login.js        # Login page
│       └── Register.js     # Registration page
├── routes/                 # Route definitions
├── store/                  # Redux store and reducers
└── themes/                 # MUI theme configuration
```

---

## Getting Started

### Prerequisites

- Node.js >= 16
- npm or yarn
- Spring Boot backend running on port 8080

### Installation

```bash
# Clone the repository
git clone https://github.com/rambo-real/album-application.git
cd album-application

# Install dependencies
npm install

# Start the development server
npm start
```

The app runs on [http://localhost:3000](http://localhost:3000) and proxies API requests to `http://localhost:8080`.

### Build for Production

```bash
npm run build
```

---

## API Integration

All API calls are versioned under `/api/v1` and handled through the `client.js` utility, which automatically attaches the JWT Bearer token from `localStorage` to authenticated requests.

Key endpoints consumed:
- `POST /api/v1/auth/login` — Authenticate and receive JWT
- `GET /api/v1/albums` — Fetch all albums
- `POST /api/v1/albums` — Create a new album
- `POST /api/v1/albums/:id/upload-photos` — Upload photos (multipart/form-data)
- `DELETE /api/v1/albums/:id` — Delete an album

---

## Screenshots

> _Coming soon_

---

## Author

**Abdur-Rahman Aregbeshola**
- Portfolio: [abdurrahman-batman.vercel.app](https://abdurrahman-batman.vercel.app)
- GitHub: [@rambo-real](https://github.com/rambo-real)
- LinkedIn: [linkedin.com/in/abdur-rahman-aregbeshola](https://linkedin.com/in/abdur-rahman-aregbeshola)
