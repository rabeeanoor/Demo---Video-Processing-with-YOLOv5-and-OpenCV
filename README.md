
# Video Processing with YOLOv5 and OpenCV

## Overview
This Python script is designed to process multiple videos by performing object detection using YOLOv5 model and annotating frames with relevant information. The script reads video files from a specified directory, detects objects within predefined regions of interest (ROIs), and annotates frames with data such as productive time, idle time, and associated personnel. The annotated frames are then saved as processed videos to an output directory.

## Features
- **Object Detection:** Utilizes the YOLOv5 model for real-time object detection within video frames.
- **ROI Annotation:** Defines specific regions of interest (ROIs) within each frame and annotates them with relevant information.
- **Data Visualization:** Visualizes data such as productive time, idle time, and associated personnel for each ROI within the video frames.
- **Data Aggregation:** Aggregates total productive time and idle time for each tank and PLC across all processed videos.

## Dependencies
- Python 3.x
- OpenCV
- PyTorch
- NumPy
- Pandas
- Matplotlib
- MoviePy
- Pillow

## Usage
1. **Installation**: Ensure all dependencies are installed. You can install them using `pip`. Run:
   ```
   pip install opencv-python torch numpy pandas matplotlib moviepy pillow
   ```
2. **Input Data Preparation**: Place your input videos in the specified video folder (`video_path`). Ensure your data is in the specified Excel format (`client_dashboard.xlsx`) with the required columns: `Start_File`, `Station`, `Start_Time`, `End_Time`, `Person`.
3. **Configuration**: Update the paths for the video folder (`video_path`) and output directory (`output_path`) in the script as per your setup.
4. **Running the Script**: Execute the script. Processed videos will be saved to the output directory.
   ```
   python video_processing.py
   ```
5. **Reviewing Results**: Review the processed videos in the output directory to observe object detection results and annotations.

## Notes
- The script assumes the input videos are in MP4 format. Adjust the codec (`fourcc`) and video file format if needed.
- ROIs are predefined for each tank based on their coordinates within the video frames.
- Ensure the YOLOv5 model is properly installed and loaded before running the script. You can install it using PyTorch's `torch.hub.load()` function.
- This script is intended for use with specific data formats and video processing requirements. Modify it as needed for your specific use case.

## Author
[Your Name]

## License
This project is licensed under the [MIT License](LICENSE).

