# Eye State Detector

Mini project I did for Computer Graphics and Image Processing in 6th sem BE CS at Jyothy Institute of Technology, VTU. It was my first time using dlib and doing anything with facial landmarks so the code is pretty basic but it helped me understand how image processing actually works in practice.

## How it works

1. You upload a photo of a face
2. dlib finds the face and maps 68 landmark points on it
3. The Eye Aspect Ratio (EAR) is calculated from the 6 points around each eye using the Soukupova and Cech formula
4. If the average EAR is below 0.3 the eyes are marked as closed, otherwise open

## Setup

1. Clone the repo
2. Download shape_predictor_68_face_landmarks.dat from dlib.net and drop it in the project root (see note below)
3. Make a virtual environment and activate it
4. Run `pip install -r requirements.txt`
5. Run `python eyedetect.py`
6. Go to [http://127.0.0.1:5000](http://127.0.0.1:5000)

## Tech stack

| Tool | What it does |
| ---- | ------------ |
| Python | main language |
| Flask | web server |
| dlib | face detection and landmark prediction |
| OpenCV | reading and processing images |
| NumPy | maths on the landmark coordinates |

## Note

The landmark model file (shape_predictor_68_face_landmarks.dat) is not in the repo because it is 95MB. Download it from [dlib.net](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2), extract the .bz2 and put the .dat file in the root folder before running.
