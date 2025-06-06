# videodetection
Robust Face Recognition in Videos Using FaceNet and MTCNN
Overview
This repository contains an implementation of a robust face recognition system for video processing using FaceNet, MTCNN, and multiple pre-processing techniques. The model can detect and recognize faces across different backgrounds and lighting conditions while applying temporal aggregation to improve recognition stability across frames.

Features
Face Detection & Recognition: Uses MTCNN for face detection and alignment, followed by FaceNet for embedding extraction.

Robust Pre-processing: Enhances image quality using:

Bilateral Filtering (preserves edges while smoothing background noise).

CLAHE-based Color Normalization (minimizes color distortions and enhances facial contrast).

Multi-Image Representation: Generates robust embeddings by averaging multiple images per person, including augmented variations.

Temporal Aggregation (Tracking): Maintains and updates embeddings across frames to improve stability and recognition accuracy.

Customizable Cosine Similarity Threshold: Optimized for balancing false positives and negatives.

Frame Storage & Video Output: Saves processed frames and reconstructs a final video using FFMPEG.

Installation
Clone the repository:

bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
Install required dependencies:

bash
pip install facenet-pytorch opencv-python torchvision
Ensure your Google Drive is mounted in Colab if running within a notebook.

Usage
Step 1: Prepare Known Faces
Place reference images in ColabImages/ inside Google Drive.

Store at least 6 images per person for better recognition accuracy.

Modify known_people in the script to reflect their file paths.

Step 2: Run Face Recognition on a Video
Ensure your input video file (test_video.mp4) is stored in ColabVideos/ in Google Drive.

Execute the script in Google Colab or a local Python environment to process the video.

Step 3: Retrieve Output
Processed frames are stored temporarily and then compiled into an output video (output_video.mp4) using FFMPEG.

The final video is saved in Google Drive under ColabVideos/.

Configuration Options
Modify margin in MTCNN to fine-tune face bounding box expansion.

Adjust cosine_threshold (default: 0.75) in the script to refine recognition sensitivity.

Customize bilateral filter parameters (d, sigmaColor, sigmaSpace) to optimize background smoothing.

Future Improvements
Integrate RetinaFace for more advanced face detection.

Experiment with adaptive embedding fusion over frames for improved temporal consistency.

Enhance tracker algorithms beyond Euclidean distance-based matching.
