# Real-time Hand Detection and Recognition using MediaPipe and OpenCV
![175758358-1931e49b-07dd-4092-b42c-f27e285533e6](https://github.com/Rutuja-Salunke/Real-time-Hand-Detection-and-Recognition-using-MediaPipe-and-OpenCV/assets/102023809/235c71ef-3723-4d2c-8ffd-51e5d56ff3b8)
- **Objective**:
  - The project's primary goal is to use computer vision to detect and recognize hands in real-time video using the MediaPipe library.

- **Libraries Used**:
  - **OpenCV (`cv2`):**
    - Utilized for capturing video frames from the webcam, image processing, and displaying the final results.
  - **MediaPipe (`mediapipe`):**
    - Provides pre-trained models for hand tracking, offering hand landmarks and additional information.

- **Hand Detection Model Initialization**:
  - The script initializes the `Hands` class from the MediaPipe library.
  - Parameters for model initialization include:
    - `static_image_mode`: Set to `False` for real-time video processing.
    - `model_complexity`: Controls the complexity of the detection model.
    - `min_detection_confidence`: Minimum confidence required to consider a hand as detected.
    - `min_tracking_confidence`: Minimum confidence required to maintain tracking of a hand.
    - `max_num_hands`: Specifies the maximum number of hands to detect (in this case, set to 2).

- **Video Capture**:
  - The `cv2.VideoCapture` is used to access the default webcam and capture video frames.

- **Image Processing**:
  - Each video frame is flipped horizontally using `cv2.flip` to mirror the feed.
  - Color space conversion from BGR to RGB is performed using `cv2.cvtColor`.

- **Hand Detection Processing**:
  - The RGB image is passed through the hand detection model using `hands.process`.
  - The results contain information about detected hands, including landmarks and confidence scores.

- **Display Information on Video Feed**:
  - If both hands are present in the frame, the script displays "Both Hands" using `cv2.putText`.
  - If only one hand is detected, the script determines if it's the right or left hand based on the MediaPipe results and displays "Right Hand" or "Left Hand" accordingly.

- **User Interaction**:
  - The program enters a while loop to continuously display the processed video feed.
  - Pressing the 'q' key breaks the loop, leading to the release of the camera and closing of the OpenCV window.

- **Text Display**:
  - Information about the detected hands (both or left/right) is overlaid on the video frame using `cv2.putText`.

- **Window Handling**:
  - The `cv2.imshow` method is used to display the video feed in a window.
  - The program exits when the user presses 'q', releasing the camera and closing the OpenCV window.

  

