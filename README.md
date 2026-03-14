# Safari Golf Club - Bay Area NorCal

This project is the official website for the Safari Golf Club, Bay Area NorCal chapter.

## Deployment Instructions

To ensure your website works correctly on GitHub Pages, you must upload all necessary files to your repository.

### Essential Files

1. **`golf_club.html`** (The main website file)
2. **`golf_background.png`** (The background image)

### Uploading via GitHub Web Interface (Recommended)

Since Git commands might not be available on your system, follow these steps:

1. Open your repository on [GitHub](https://github.com/).
2. Click the **"Add file"** button and select **"Upload files"**.
3. Drag and drop **both** `golf_club.html` and `golf_background.png` into the upload area.
4. Scroll down, add a commit message (e.g., "Update club website"), and click **"Commit changes"**.

### Troubleshooting

- **"git is not recognized" Error**: This means Git is not installed on your computer. Use the web upload method described above instead of the terminal.
- **Missing Background**: Ensure `golf_background.png` is in the same folder as `golf_club.html` on GitHub.
- **Rankings Not Showing**: The app uses your browser's local storage to save data. If you move to a different computer or clear your browser data, you will need to re-import your data if you have an export file.

## Firebase Integration setup

This application now uses Firebase for real-time cloud data storage! This replaces `localStorage` and ensures everyone sees the same updates instantly across multiple devices.

To activate this feature, you will need to create a Firebase Project:

1. Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. In the project overview, click the **Web** icon (`</>`) to register a web app.
3. Copy the **`firebaseConfig`** object provided.
4. Open the `golf_club.html` file in a code editor.
5. In `golf_club.html`, locate the `firebaseConfig` object (around line 3600) and replace the placeholder `"YOUR_API_KEY"`, `"YOUR_PROJECT_ID"`, etc., with the exact values from your Firebase Console.
6. Still in your Firebase console, go to **Firestore Database** and click **Create database** (start it in Test Mode for development or set rules to allow read/write access).
7. The application will handle the rest, seeding the empty database with initial `clubData` automatically upon the first successful connection.

## Features

- Member Management
- Handicap Tracking
- Score Recording
- Treasurer Reports
- Secretary Meeting Management

## Safari Golf Club Bay Area NorCal
