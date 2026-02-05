# Notes API

A simple REST API for managing notes built with Node.js, Express, and MongoDB.

## Features

- Create notes with title and description
- Retrieve all notes
- Update note descriptions
- Delete notes
- Static file serving for frontend

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose
- **Environment**: dotenv for configuration
- **CORS**: Enabled for cross-origin requests

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file with:
   ```
   MONGO_URI=your_mongodb_connection_string
   PORT=3000
   ```

## Usage

### Development
```bash
npm run dev
```

### Production
```bash
npm start
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/notes` | Create a new note |
| GET | `/api/notes` | Get all notes |
| PATCH | `/api/notes/:id` | Update note description |
| DELETE | `/api/notes/:id` | Delete a note |

### Request Examples

**Create Note:**
```json
POST /api/notes
{
  "title": "Sample Note",
  "description": "This is a sample note"
}
```

**Update Note:**
```json
PATCH /api/notes/:id
{
  "description": "Updated description"
}
```

## Project Structure

```
├── src/
│   ├── config/
│   │   └── database.js
│   ├── models/
│   │   └── note.model.js
│   └── app.js
├── public/
├── server.js
└── package.json
```

## License

ISC