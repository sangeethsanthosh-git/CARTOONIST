# CARTOONIST
Cartoonizer: Transform Your Photos and Videos into Cartoons

Cartoonizer is a Flask-based web application that transforms both photos and videos into cartoon-style artwork using TensorFlow and OpenCV. With an intuitive interface and advanced features, users can create stunning cartoon effects with ease. The project now supports video conversion in addition to photo conversion, along with 10 new features to enhance creativity and user engagement.

Table of Contents

Features
New Features
Demo
Installation
Usage
Project Structure
Technologies Used
Contributing
License
Authors


Features

Photo and Video Cartoonization: Transform images (PNG, JPG, JPEG, GIF) and videos (MP4, AVI) into cartoon-style artwork.
Real-Time Progress Updates: See processing status with Server-Sent Events (SSE).
Responsive UI: Built with Tailwind CSS for a modern, user-friendly experience.
File Support: Handles files up to 100 MB.


New Features
Cartoonizer has been enhanced with the following 10 features:

Multiple Cartoon Styles: Choose from Classic Comic, Anime, Sketch, or Watercolor styles for both photos and videos.
Customization Options: Adjust edge thickness (1-10) and color intensity (1-100).
Background Replacement: Add cartoon-themed backgrounds (e.g., Cityscape, Magical Forest) to photos and videos.
Real-Time Preview: Preview cartoon effects for photos using a low-res canvas (CamanJS).
Batch Processing: Cartoonize multiple photos or a video in one session.
Text and Stickers: Add text and stickers to photos with an interactive editor (Fabric.js).
Social Media Sharing: Share cartoonized photos and videos to Facebook, Twitter, or Instagram.
Cartoon Avatars: Create avatars from selfies using Mediapipe facial detection (photos only).
Undo/Redo: Experiment with edits safely (photos only).
Educational Mode: Learn about cartoonization with tooltips.


Demo
Photo Cartoonization
Watch a quick demo of cartoonizing a photo with the "Anime" style, adjusting settings, and adding a background:

Video Cartoonization
See how a short video is transformed into a cartoon with the "Classic Comic" style:

Note: Replace the placeholder images above with actual demo videos or GIFs after recording them (see Usage for recording instructions).

Installation
Prerequisites

Python 3.8+
FFmpeg (for video processing)
GPU (optional, for faster TensorFlow inference)

Steps

Clone the Repository:
git clone https://github.com/your-username/cartoonizer.git
cd cartoonizer


Set Up a Virtual Environment (optional but recommended):
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install Dependencies:
pip install -r requirements.txt

If requirements.txt is not available, install the following:
pip install flask tensorflow opencv-python mediapipe pyyaml numpy


Install FFmpeg:

Windows: Download from ffmpeg.org, extract, and add to your system PATH.
Mac: brew install ffmpeg
Linux: sudo apt-get install ffmpeg


Download Pre-trained Models:

The project uses pre-trained models for cartoonization. Ensure the white_box_cartoonizer/saved_models directory contains the necessary weights. If not, download them from this link and place them in the saved_models directory.


Set Up Static Folders:

Create static/backgrounds and add cartoon-themed background images (e.g., cityscape.jpg, forest.jpg, space.jpg).
Create static/stickers and add sticker images (e.g., star.png).




Usage
Running the App

Start the Flask server:
python app.py

The app will run on http://127.0.0.1:8080.

Open your browser and navigate to http://127.0.0.1:8080.

Upload a photo or video, customize settings (style, edge thickness, color intensity, background), and process. For photos, you can also add text/stickers, create avatars, and use educational mode.


Recording Demo Videos
To create demo videos for the README:

Use a screen recording tool (e.g., OBS Studio, QuickTime Player, or Xbox Game Bar).
Record the following:
Photo Demo: Upload a photo, select "Anime" style, adjust sliders, add a background, and show the result.
Video Demo: Upload a short video (10-15 seconds), select "Classic Comic" style, and show the processed video.


Save videos as MP4 or convert to GIF using tools like EZGIF.
Upload videos/GIFs to GitHub or a hosting service (e.g., Imgur) and update the demo section with the links.


Project Structure
cartoonizer/
├── app.py                    # Main Flask application
├── cartoonize.py             # Cartoonization logic (TensorFlow model)
├── config.yaml               # Configuration file
├── templates/
│   └── index_cartoonized.html # HTML template for the app
├── static/
│   ├── uploaded_images/      # Temporary storage for uploaded files
│   ├── cartoonized_outputs/  # Storage for processed outputs
│   ├── backgrounds/          # Cartoon-themed background images
│   └── stickers/             # Sticker images for photo editing
├── white_box_cartoonizer/
│   └── saved_models/         # Pre-trained TensorFlow models
└── README.md                 # Project documentation


Technologies Used

Frontend: HTML, CSS (Tailwind CSS), JavaScript (jQuery, Fabric.js, CamanJS)
Backend: Flask, TensorFlow, OpenCV, Mediapipe, FFmpeg
Other: Server-Sent Events (SSE), Google Cloud Storage (optional)


Contributing
We welcome contributions to improve Cartoonizer! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make your changes and commit (git commit -m "Add your feature").
Push to your branch (git push origin feature/your-feature).
Open a Pull Request with a detailed description of your changes.


License
This project is licensed under the MIT License. See the LICENSE file for details.



For questions or feedback, please contact us at [sangeethsanthosh80@gmail.com].
