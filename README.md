# Real-time Hand Detection and Recognition using MediaPipe and OpenCV

- **Objective**: The project aims to detect and recognize hands in real-time using the MediaPipe library in Python.

- **Libraries Used**:
  - OpenCV (`cv2`): Used for capturing video frames, image processing, and displaying the results.
  - MediaPipe (`mediapipe`): Utilized for hand tracking, providing hand landmarks and information.

- **Hand Detection Model**:
  - The `Hands` class from the MediaPipe library is used to initialize the hand detection model.
  - Configuration parameters include static image mode, model complexity, confidence thresholds, and the maximum number of hands to detect.

- **Video Capture**:
  - The script captures video frames from the default webcam using OpenCV (`cv2.VideoCapture`).

- **Image Processing**:
  - Each frame is flipped horizontally to mirror the video feed.
  - The color space of the image is converted from BGR to RGB.

- **Hand Detection**:
  - The processed RGB image is passed through the MediaPipe hand detection model (`hands.process`).
  - Results include hand landmarks and additional information about the detected hands.

- **Display Information on Video Feed**:
  - If both hands are present, it displays "Both Hands" on the image.
  - If only one hand is present, it determines if it's the right or left hand using the MediaPipe results and displays "Right Hand" or "Left Hand" accordingly.

- **User Interaction**:
  - The program continuously displays the processed video feed.
  - Pressing 'q' exits the program.

- **Text Display**:
  - Information about the detected hands is displayed on the video frame using OpenCV's `cv2.putText` method.

- **Window Handling**:
  - The `cv2.imshow` method is used to display the video feed.
  - The program exits when the user presses 'q', releasing the camera and closing the OpenCV window.
**Conclusion:**

This project successfully demonstrates real-time hand detection and recognition using the MediaPipe library and OpenCV. The combination of these powerful tools allows for the efficient processing of video frames from a webcam, providing information about the presence and classification of hands in the feed. The key takeaways from this project include:

- **Model Initialization:** The initialization of the MediaPipe hand detection model with specific parameters enables real-time processing, allowing the system to adapt to various complexities and confidence thresholds.

- **Accurate Hand Recognition:** The project accurately identifies and distinguishes between both hands, displaying appropriate labels on the video feed. The integration of MediaPipe's hand landmarks facilitates precise hand tracking and recognition.

- **User Interaction:** The application offers a user-friendly experience with continuous video feed display. The 'q' key provides a convenient way to exit the program, releasing the camera and closing the window seamlessly.

- **Versatility:** The project is versatile, capable of handling scenarios where both hands or only a single hand is present, offering flexibility in different applications.

- **Educational Value:** This project serves as a practical example for those learning computer vision, showcasing the integration of popular libraries for real-world applications. The use of MediaPipe and OpenCV in tandem provides a robust foundation for building more complex computer vision projects.


