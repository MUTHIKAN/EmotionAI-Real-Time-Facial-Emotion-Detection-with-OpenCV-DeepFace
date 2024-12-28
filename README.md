# Facial-Emotion-Recognition-using-OpenCV-and-Deepface
This project implements real-time facial emotion detection using the `deepface` library and OpenCV. It captures video from the webcam, detects faces, and predicts the emotions associated with each face. The emotion labels are displayed on the frames in real-time.
This is probably the shortest code to implement realtime emotion monitoring.

## Dependencies

- [deepface](https://github.com/serengil/deepface): A deep learning facial analysis library that provides pre-trained models for facial emotion detection. It relies on TensorFlow for the underlying deep learning operations.
- [OpenCV](https://opencv.org/): An open-source computer vision library used for image and video processing.

## Usage
### Initial steps:
- Git clone this repository Run: `git clone https://github.com/manish-9245/Facial-Emotion-Recognition-using-OpenCV-and-Deepface.git`
- Run: `cd Facial-Emotion-Recognition-using-OpenCV-and-Deepface`
1. Install the required dependencies:
   - You can use `pip install -r requirements.txt`
   - Or you can install dependencies individually:
      - `pip install deepface`
      - `pip install tf_keras`
      - `pip install opencv-python`

2. Download the Haar cascade XML file for face detection:
   - Visit the [OpenCV GitHub repository](https://github.com/opencv/opencv/tree/master/data/haarcascades) and download the `haarcascade_frontalface_default.xml` file.

3. Run the code:
   - Execute the Python script.
   - The webcam will open, and real-time facial emotion detection will start.
   - Emotion labels will be displayed on the frames around detected faces.

## Approach

1. Import the necessary libraries: `cv2` for video capture and image processing, and `deepface` for the emotion detection model.

2. Load the Haar cascade classifier XML file for face detection using `cv2.CascadeClassifier()`.

3. Start capturing video from the default webcam using `cv2.VideoCapture()`.

4. Enter a continuous loop to process each frame of the captured video.

5. Convert each frame to grayscale using `cv2.cvtColor()`.

6. Detect faces in the grayscale frame using `face_cascade.detectMultiScale()`.

7. For each detected face, extract the face ROI (Region of Interest).

8. Preprocess the face image for emotion detection using the `deepface` library's built-in preprocessing function.

9. Make predictions for the emotions using the pre-trained emotion detection model provided by the `deepface` library.

10. Retrieve the index of the predicted emotion and map it to the corresponding emotion label.

11. Draw a rectangle around the detected face and label it with the predicted emotion using `cv2.rectangle()` and `cv2.putText()`.

12. Display the resulting frame with the labeled emotion using `cv2.imshow()`.

13. If the 'q' key is pressed, exit the loop.

14. Release the video capture and close all windows using `cap.release()` and `cv2.destroyAllWindows()`.

![image](https://github.com/manish-9245/Facial-Emotion-Recognition-using-OpenCV-and-Deepface/assets/69393822/57c41270-7575-4bc7-ae7a-99d67239a5ab)

## Contribution
Contributions are welcome! If you have suggestions or improvements, please:
1. Fork the repository.
2. Create a new branch.
3. Commit your changes.
4. Submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For any queries, feel free to reach out:
- **Author**: Muthikanraj
- **GitHub**: [MUTHIKAN](https://github.com/MUTHIKAN)

