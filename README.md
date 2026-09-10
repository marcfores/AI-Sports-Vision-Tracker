# AI Sports Vision: Real-Time Player Tracking & Heatmaps

A computer vision system designed to analyze football match footage, detecting players, tracking their movement trajectories, and visualizing spatial activity. 

Developed as a Final Course Project in Computer Vision, this system leverages deep learning and multi-object tracking algorithms to extract actionable sports analytics from raw video feeds.

## Core Computer Vision Features

*   **Real-Time Object Detection:** Utilizes the YOLOv8 (Ultralytics) model to identify players, referees, and the ball with high precision and speed.
*   **Automated Team Classification:** Implements K-Means clustering ($k=2$) in the HSV color space to dynamically separate teams based on their jersey colors, achieving a high success rate even without manual pre-labeling.
*   **Robust Multi-Object Tracking:** Integrates the ByteTrack algorithm (via Supervision) to maintain unique player identities across frames, successfully handling occlusions and dynamic movements.
*   **Spatial Data Visualization:** Processes accumulated positional data using NumPy and Matplotlib to generate both 2D density maps and 3D surface plots, highlighting areas of high activity on the pitch.

## Performance & Optimization

*   **Hardware Acceleration:** Optimized for CUDA execution, achieving approximately 47 FPS processing speeds on an NVIDIA RTX 3060 GPU (processing faster than real-time for standard 25 FPS video).
*   **ROI Filtering:** Implements Region of Interest (ROI) filtering to exclude spectators in the stands, focusing the neural network strictly on the field of play.

## Repository Structure
*   `/src`: Python source code containing the detection loop, clustering algorithms, and tracking logic.
*   `/docs`: Complete project report (`.pdf`) and presentation slides detailing the methodology, architecture, and technology comparisons.
*   *Note: The raw input video required to execute the tracking script exceeds GitHub's file size limits. **[Download the Input Video Resource Here](https://drive.google.com/file/d/1vMJG0A7JK0R_kUdJ4L3UozCSDxfs2nAp/view?usp=sharing)***

## Tech Stack
*   **Language:** Python (3.10+)
*   **Deep Learning / CV:** YOLOv8, OpenCV, Supervision (Roboflow), ByteTrack
*   **Data Analysis:** NumPy, Matplotlib
