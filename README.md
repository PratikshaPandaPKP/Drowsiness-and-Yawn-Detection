1. **Libraries and Modules**: 
   - Imports necessary libraries for video processing (`imutils`, `cv2`, `dlib`), threading, and mathematical calculations (`numpy`, `scipy`).

2. **Functions**:
   - `alarm(msg)`: Activates an audible alarm using the `espeak` command when drowsiness or yawning is detected.
   - `eye_aspect_ratio(eye)`: Calculates the eye aspect ratio (EAR) to detect eye closure.
   - `final_ear(shape)`: Computes the average EAR for both eyes.
   - `lip_distance(shape)`: Measures the distance between the upper and lower lips to detect yawning.

3. **Main Parameters**:
   - `EYE_AR_THRESH`: Threshold for detecting drowsiness based on EAR.
   - `EYE_AR_CONSEC_FRAMES`: Number of consecutive frames the EAR must be below the threshold to trigger an alarm.
   - `YAWN_THRESH`: Threshold for detecting yawning based on lip distance.

4. **Initialization**:
   - Loads face detector (`haarcascade_frontalface_default.xml`) and landmark predictor (`shape_predictor_68_face_landmarks.dat`).
   - Starts the video stream from the specified webcam.

5. **Main Loop**:
   - Captures video frames, converts them to grayscale, and detects faces.
   - For each detected face:
     - Predicts facial landmarks.
     - Calculates EAR and lip distance.
     - Draws contours around the eyes and mouth.
     - Checks if EAR is below the threshold for a specified number of frames to detect drowsiness.
     - Checks if the lip distance exceeds the threshold to detect yawning.
     - Triggers the alarm if drowsiness or yawning is detected.
     - Displays EAR and yawning metrics on the video frame.
   - Adjusts frame size to fit the screen and displays it.

6. **Exit Condition**:
   - The loop continues until the 'q' key is pressed, after which the video stream and window are closed.

This script is used for real-time monitoring of drowsiness and yawning, potentially useful in situations requiring continuous alertness, such as driving.


**Video Link of The Project in Action:**

https://www.loom.com/share/235eb4d0279348ae84fb892d967c968e?sid=bf98bd27-0ade-48a2-85eb-031255d59de9


**Link of The Zip Project File:** 

https://1drv.ms/u/c/f5113501d80b7674/ESvRhBneOdtCmbNIGrTTu_YBEsP4jcKz7w0v2uewYBltIA?e=tPra09
