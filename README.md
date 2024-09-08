# RTSP Video Streaming with Custom Overlays

Project Overview
This project is a web application that allows users to view RTSP live-streamed video with custom overlays that can be positioned, resized, and managed using a CRUD API. The application consists of a React frontend for the user interface, a Flask backend to handle API requests, and MongoDB for storing overlay information. Users can play a livestream, and place overlays (e.g., text, logos) on top of the video in real-time.

Key Features:
RTSP Video Playback: Streams video from an RTSP URL.
Custom Overlays: Add, edit, delete, and position overlays (e.g., text, images) on top of the video.
CRUD API: Create, Read, Update, Delete overlay configurations using a Flask API.
Responsive UI: Manage overlays directly through a simple user interface.

Tech Stack
Frontend:
React
Axios (for API requests)
HTML5 <video> tag
Backend:
Python (Flask)
MongoDB (Cloud instance)
Dependencies:
Flask
Flask-CORS
pymongo
Axios (React library for HTTP requests)

1. Setting Up the Backend
Clone the repository:
Copy code
git clone https://github.com/your-username/rtsp-overlay-streaming.git
cd rtsp-overlay-streaming/backend

Install Python dependencies:
Copy code
pip install Flask flask-cors pymongo

Configure MongoDB:
Create a MongoDB Atlas account and a cluster.
Get the MongoDB connection string and add it to the app.py:
client = pymongo.MongoClient("<your_mongodb_connection_string>")

Run the Flask Backend:
python app.py
This will start the Flask server at http://localhost:5000.

3. Setting Up the Frontend
Navigate to the frontend folder:
cd ../frontend

Install Node.js dependencies:
npm install

Update RTSP Stream URL:
In the OverlayDisplay.js file, update the streamUrl with your RTSP stream:

javascript
const streamUrl = "rtsp://your_rtsp_stream_url";
Run the Frontend:
bash
Copy code
npm start
This will start the React development server at http://localhost:3000.

Running the Application
Start the Flask backend: This will handle API requests and serve the overlay data.
Start the React frontend: This will display the RTSP video stream along with custom overlays that you can manage through the UI.
Add, Update, and Delete Overlays: Use the UI to manage overlays on the video.
API Endpoints
GET /overlay: Fetch all saved overlays.
POST /overlay: Create a new overlay.
PUT /overlay/
: Update an existing overlay.
DELETE /overlay/
: Delete an overlay.
