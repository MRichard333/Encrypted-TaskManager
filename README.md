# Encrypted NoteTask — Secure & Local ToDo + Notes App 🔐

MIT License Node.js ≥ 14.x React ≥ 18.x


# Encrypted ToDo App 🔐

A simple, local, open-source encrypted todo app with passphrase-based encryption.  
Built with React frontend and Node.js + Express backend with SQLite database.

- - -

## Features

*   End-to-end encrypted todos, locked by a passphrase you set
*   Add, delete, and list todos securely
*   Change your encryption passphrase anytime
*   Simple local setup, no external dependencies or cloud required
*   Light/dark mode toggle
*   Open source and privacy-focused

## Requirements

*   Node.js v18+ (tested with v22)
*   npm (comes with Node.js)
*   Git (optional, for cloning the repo)

## Getting Started

### 1\. Clone the repository

```
git clone https://github.com/MRichard333/encrypted-todo-app.git
cd encrypted-todo-app
```

_(Or download and extract the ZIP if you prefer)_

### 2\. Install dependencies

```
npm install
cd server
npm install
cd ..
```

### 3\. Run the backend server

The backend serves the API and the built frontend.

```
node server/app.js
```

By default, it runs on [http://localhost:3001](http://localhost:3001)

### 4\. Run the frontend development server (optional)

If you want to develop or test frontend changes without rebuilding the backend:

```
npm run dev
```

This runs Vite’s dev server on [http://localhost:5173](http://localhost:5173)

The Electron app or browser frontend should use `NODE_ENV=development` to load from here.

### 5\. Build frontend for production

To build the optimized frontend bundle that the backend serves:

```
npm run build
```

This outputs to `client/dist` directory.

### 6\. Run the Electron app

Make sure to build the frontend first (`npm run build`) or have the dev server running (`npm run dev`).

```
npm run electron
```

This starts the Electron app with GPU disabled for compatibility.

## Usage

*   On first run, create your passphrase by entering any string of 6+ characters.
*   Add todos securely encrypted with your passphrase.
*   Lock app anytime to secure data.
*   Change passphrase safely using the UI.
*   Your todos are stored locally in an encrypted SQLite DB (`server/database.sqlite`).

## Project Structure

```
/
├── client/           # React frontend source code
├── server/           # Backend Express server
├── main.js           # Electron main process
├── package.json
├── README.md
```

## Security Notes

*   Your passphrase **is not stored** anywhere; keep it safe.
*   If you forget your passphrase, your todos cannot be decrypted.
*   Data is encrypted at rest in the local SQLite database.
*   No data is sent externally or stored on the internet.

“Electron held at v25.8.3 for native module compatibility (better-sqlite3). Audit warnings acknowledged.”

## Contributing

Feel free to fork, open issues, or submit pull requests.  
Please keep it lightweight, privacy-first, and local-use friendly.

## License

MIT License — see `LICENSE` file.

Made with ❤️ by [MRichard333.com](https://MRichard333.com)  
If you need help or want to discuss features, open an issue or contact me!