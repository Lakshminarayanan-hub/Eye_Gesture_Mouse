# Eye-Controlled Mouse

Eye-Controlled Mouse is a Python program that uses computer vision and facial landmarks to control the mouse cursor. It utilizes the `mediapipe` library for facial landmark detection and `pyautogui` for mouse cursor control.

## Prerequisites

Before running the program, make sure you have the following installed:

- Python 3.x
- OpenCV (`cv2`)
- MediaPipe (`mediapipe`)
- PyAutoGUI (`pyautogui`)

You can install these dependencies using `pip`:

```bash
pip install opencv-python mediapipe pyautogui
```

## How It Works

1. The program captures video from your computer's default camera (usually the webcam).

2. It uses `mediapipe` to detect facial landmarks, specifically focusing on the right eye and a specific set of points around it.

3. It calculates the position of the mouse cursor based on the detected landmarks.

4. When the user blinks their right eye (specifically, when the vertical distance between two specific points is less than a threshold), the program simulates a mouse click.

5. The program continuously updates the mouse cursor position based on the detected eye landmarks, allowing you to move the cursor by moving your eye.

6. The camera feed with overlayed landmarks and mouse cursor movement is displayed in a window.

## How to Use

1. Ensure that your webcam is properly connected and accessible.

2. Run the Python script. The program will open a window displaying your camera feed with overlaid landmarks.

3. To control the mouse cursor, look at the desired point on the screen and blink your right eye.

4. The program will simulate a mouse click at the cursor position when it detects a blink.

5. To exit the program, press `ESC`.

## Configuration

You can adjust the program's behavior by modifying the following parameters in the script:

- `cam = cv2.VideoCapture(0)`: Change the camera source (0 for the default camera).

- `output = face_mesh.process(rgb_frame)`: You can configure other options for face mesh processing if needed.

- `if (left[0].y - left[1].y) < 0.004:`: Adjust the blink detection threshold to match your eye movement.

## Issues and Limitations

- The program relies on the accuracy of the facial landmark detection, which may not work perfectly for all users.

- Lighting conditions and the position of the camera can affect the program's performance.

- The program's configuration may need to be fine-tuned for individual use cases.

## License

This software is released under the MIT License. See the `LICENSE` file for more details.

## Acknowledgments

- This program uses the `mediapipe` library for facial landmark detection.

- Mouse cursor control is made possible by the `pyautogui` library.

## Author

- Lakshmi Narayanan M
- rajimurugu123456@gmail.com

Please feel free to reach out if you have any questions, feedback, or suggestions.

Enjoy controlling your mouse with your eyes!
