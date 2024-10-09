
# PosturePal: Real-Time Posture Correction Using Computer Vision

Welcome to **PosturePal**, an innovative tool that monitors your posture in real time using your device's webcam. PosturePal helps you maintain a healthy sitting posture by detecting slouching and forward shoulder posture, both when you are facing the camera or in a side view. It provides subtle reminders and alerts to prevent long-term back issues.

## Key Features:

- **Real-time posture detection** using MediaPipe Pose and OpenCV.
- Detects both **front-facing and side-view slouching**.
- Provides gentle **audio reminders** and **pop-up notifications** to correct posture.
- **Warning system** that resets after every 100th warning, with an optional beep after every threshold.
- Lightweight and easy-to-use tool that runs locally without the need for cloud processing.

## Demo

![PosturePal in action](demo.gif)  
_Example of how PosturePal detects slouching posture and gives feedback._

## How It Works

PosturePal uses the following features to detect bad posture:

1. **Shoulder alignment** – Ensures your shoulders remain level, which helps detect lateral tilting.
2. **Spine curvature (slouch detection)** – Detects slouching or forward-leaning posture based on the relative positioning of shoulders and hips.
3. **Side view slouch detection** – Monitors for excessive forward shoulder posture, even when viewed from the side.

## Getting Started

### Prerequisites

Ensure you have the following dependencies installed:

- Python 3.x
- OpenCV (`pip install opencv-python`)
- MediaPipe (`pip install mediapipe`)
- Numpy (`pip install numpy`)
- Tkinter (included with most Python installations)
- SoundDevice (`pip install sounddevice`)

### Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/MohanVamsi183/PosturePal.git
   ```

2. Navigate to the repository directory:

   ```bash
   cd PosturePal
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the program:

   ```bash
   python postureCorrect.py
   ```

## Usage

Once you run the program, PosturePal will access your webcam to analyze your posture in real time. The system will alert you with warnings whenever it detects poor posture, ensuring you maintain healthy sitting habits.

- **Warnings**: Each bad posture event will trigger a pop-up warning. After every 100th warning, the system plays a beep sound.
- **Reset**: Once the warning count reaches the threshold (100), it will reset, and the system will continue monitoring.

## Customization

You can modify the posture correction sensitivity or the alert frequency in the `postureCorrect.py` file. Adjust the following parameters based on your needs:

- **Warning threshold**: Change the `max_warnings` value to set how many warnings trigger the beep sound.
- **Spine slouch threshold**: Adjust the `spine_slouch_threshold` to increase or decrease sensitivity to forward leaning.

## Future Enhancements

- Add machine learning-based posture correction improvement suggestions.
- Integrate with wearable devices for improved tracking.


