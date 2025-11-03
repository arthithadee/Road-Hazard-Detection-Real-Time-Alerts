Real-Time Pothole Detection Using YOLOv8 & OpenCV

Potholes are depressions or breaks in the pavement surface of roads. They cause vehicle damage (tyre, suspension), increase accident risk, slow traffic, and require costly maintenance.

On Indian roads especially, poor drainage, heavy rains and mixed usage cause potholes to appear frequently and with varying shapes and sizes.

Manual inspection is labour-intensive, slow and often reactive (after complaints).

The aim: develop a real-time AI system that can detect potholes from dash-cam or smartphone video/image feed, so that alerts can be issued (to driver or maintenance crew) and preventative action taken earlier.

Use an object-detection deep-learning model (e.g., YOLOv8) to directly detect potholes in images/video frames.

Pipeline steps:

Capture video or images from a dash-cam or smartphone mounted in vehicle.

Pre-process frames (resize, crop to region of interest e.g., road ahead, possibly stabilise).

Run the detection model on each frame to identify bounding boxes around potholes.

For each detected pothole above a confidence threshold, trigger an alert (visual overlay, beep, log entry, send notification).

Optionally, log detection data with timestamp + GPS (if available) for road maintenance mapping.

Training: gather an annotated dataset of potholes (bounding boxes), train (or fine-tune) YOLOv8 model for “pothole” as a class.

Deployment: use a lightweight version (e.g., YOLOv8n or YOLOv8s) for real-time inference on edge device or smartphone.

Additional enhancements: filter false positives (e.g., manhole covers, shadows), estimate pothole size or severity, integrate with map for maintenance scheduling.
