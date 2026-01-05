# Cartoon Face Mask Using OpenCV (Real-Time Computer Vision)

## Project Overview
This project implements a **real-time computer vision application** that detects human faces from a live webcam feed and overlays a **cartoon-style face mask** onto detected faces.  
The processed video stream is displayed in real time and **saved to a video file**, demonstrating an end-to-end video processing pipeline.

The project focuses on classical computer vision techniques rather than deep learning, emphasizing **face detection, image masking, coordinate alignment, and video handling** using OpenCV.

---

## Objectives
- Capture live video from a webcam
- Detect faces and eyes in real time
- Accurately align and overlay a cartoon mask on detected faces
- Apply alpha blending for natural visual integration
- Save the processed video stream to a file
- Display results interactively with user-controlled exit

---

## System Workflow
1. Capture frames from the webcam
2. Convert frames to grayscale for detection
3. Detect faces using Haar Cascade classifiers
4. Detect eyes within the face region
5. Estimate facial alignment using eye positions
6. Resize and position the cartoon mask dynamically
7. Apply alpha blending to merge the mask with the face region
8. Display the result and write frames to a video file

---

## Face Detection
Face and eye detection are performed using **Haar Cascade classifiers** provided by OpenCV:
- Frontal face detection
- Eye detection (used for alignment)

These detectors enable fast, real-time performance without requiring GPU acceleration.

---

## Mask Overlay Technique
- The cartoon mask image includes an **alpha channel**
- The mask is resized based on facial geometry
- Pixel-wise alpha blending is applied:
  - Foreground: mask image
  - Background: face region
- Boundary checks prevent out-of-frame overlay errors

This approach ensures smooth and visually consistent masking.

---

## Video Output
- Real-time display using `cv2.imshow()`
- Processed frames saved to a `.avi` video file using `cv2.VideoWriter`
- Automatic cleanup of video capture and resources on exit

---

## Technologies Used
- Python
- OpenCV
- Haar Cascade Classifiers
- Image masking and alpha blending
- Real-time video capture and writing

---

## Skills Demonstrated
- Classical computer vision techniques
- Real-time video processing
- Face detection and region-based analysis
- Image blending and transparency handling
- Coordinate system manipulation
- Practical OpenCV application design

---

## Results
- Successfully detects faces and eyes in real time
- Applies a stable, well-aligned cartoon mask
- Saves the processed video output without frame loss
- Operates smoothly on standard CPU hardware

---

## Limitations
- Haar Cascades may fail under extreme lighting conditions
- Performance depends on webcam quality and resolution
- No facial landmark refinement (e.g., nose or mouth alignment)

---

## Future Enhancements
- Replace Haar Cascades with deep learning-based face detectors
- Add facial landmark detection for improved alignment
- Support multiple masks and dynamic mask selection
- Deploy as a desktop or web application
- Add face tracking for smoother motion handling

---

## Conclusion
This project demonstrates a complete **real-time computer vision pipeline**, combining face detection, image processing, and video recording.  
It showcases strong foundational skills in OpenCV and classical vision techniques applicable to augmented reality and interactive vision systems.
