# Number Plate Detection Model

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Scripts](#scripts)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

Welcome to the Number Plate Detection Model project! This project leverages YOLO (You Only Look Once) models to detect vehicles and their number plates in images or videos. The system utilizes two trained YOLO models: 
1. **YOLO Model** trained on the COCO dataset for general object detection (like cars).
2. **Number Plate Detection Model** trained specifically to recognize number plates.

The `main.py` script orchestrates the processing of input media to detect vehicles and their number plates, and outputs the processed video. Additionally, the `missing_data.py` script helps fill in any missing frames in the video by averaging adjacent frames.

## Features

- **Vehicle Detection**: Identify vehicles in frames using the YOLO model trained on the COCO dataset.
- **Number Plate Detection**: Detect and localize number plates on the identified vehicles.
- **Frame-by-Frame Processing**: Analyze videos frame by frame and combine the processed frames into a video output.
- **Frame Interpolation**: Fill missing frames by averaging neighboring frames using the `missing_data.py` script.
- **Easy Integration**: Simple steps to integrate and use the model on your own images or videos.

## Installation

To get started with the Number Plate Detection Model, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/gaurav23v/number-plate-detection.git
   cd number-plate-detection
   ```

2. **Install Dependencies**:
   Make sure you have Python installed. You can install the required packages using pip:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Running the Detection

1. **Prepare Your Input**:
   - Place your image or video file in the project directory or any accessible location.
   - Note down the file path.

2. **Run the `main.py` Script**:
   - Edit the `main.py` file to specify the path of your input file in the code:
     ```python
     input_path = 'path/to/your/input/file.jpg'  # Replace with your actual file path
     ```
   - Execute the script:
     ```bash
     python main.py
     ```
   - The script will process the file and output a video with detected vehicles and number plates.

### Handling Missing Frames

If you have missing frames in your video, use the `missing_data.py` script to fill them in.

1. **Specify Missing Frames**:
   - Update `missing_data.py` to include the path to your video and any specific details about the missing frames.

2. **Run the `missing_data.py` Script**:
   ```bash
   python missing_data.py
   ```

## Scripts

### `main.py`

- **Purpose**: Detects vehicles and number plates in the provided media.
- **Usage**: Configure the `input_path` variable and run the script to process the media.
- **Dependencies**: Uses OpenCV and YOLO models for detection.

### `missing_data.py`

- **Purpose**: Fills in missing frames in a video by averaging the frames before and after the missing one.
- **Usage**: Specify the video path and details about missing frames in the script and run it.
- **Dependencies**: Uses OpenCV for video manipulation.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, feel free to reach out:

- **GitHub Issues**: [Issues Page](https://github.com/gaurav23v/number-plate-detection/issues)
- **Email**: gaurav2301v@gmail.com

Enjoy using the Number Plate Detection Model!

---

*Note: Replace placeholder URLs and email with actual information related to your project.*