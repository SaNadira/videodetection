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
