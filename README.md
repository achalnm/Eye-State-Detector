# Eye State Detector

This was a mini project for the Computer Graphics and Image Processing subject in the sixth semester of the Bachelor of Engineering in Computer Science at Jyothy Institute of Technology, VTU, Bangalore. This was one of the first times I worked with computer vision and facial landmark detection. It is not a complex project but it was a useful starting point for understanding how image processing pipelines work.

## How it works

1. Upload a photo of a face through the web interface.
2. dlib detects the face and predicts 68 facial landmarks on it.
3. The Eye Aspect Ratio (EAR) is calculated from the 6 landmark points around each eye using the Soukupova and Cech formula.
4. If the average EAR falls below 0.3 the eyes are classified as closed, otherwise open.

## Setup

1. Clone the repo.
2. Download `shape_predictor_68_face_landmarks.dat` from [dlib.net](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2) and place it in the project root.
3. Create a virtual environment: `python -m venv venv` and activate it.
4. Install dependencies: `pip install -r requirements.txt`
5. Run the app: `python eyedetect.py`
6. Open `http://127.0.0.1:5000` in your browser.

## Tech stack

| Tool | Purpose |
| ---- | ------- |
| Python | Core language |
| Flask | Web framework |
| dlib | Face detection and landmark prediction |
| OpenCV | Image loading and colour conversion |
| NumPy | Landmark coordinate math |

## Note

The 68 landmark model file is not included in the repo because it is 95MB. Download it separately from [dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2) and extract it to the project root before running.
