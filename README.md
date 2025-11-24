# Smart Physiotherapy Assistant 🏋️‍♂️🩺

A computer vision-based rehabilitation assistant designed to monitor physiotherapy exercises in real-time. This system uses **OpenCV** and **MediaPipe** to track body landmarks, calculates joint angles to assess form, and provides instant audio feedback using **gTTS** (Google Text-to-Speech).

## 🌟 Key Features
* **Real-time Pose Detection:** accurately tracks key body joints without wearable sensors.
* **Angle Calculation:** Computes precise angles for various joints to determine if an exercise is performed correctly.
* **Audio Feedback:** Provides vocal cues (e.g., "Good," "Perfect," "Try Again," "You Stopped") and counts repetitions aloud.
* **Session Modes:**
    * **Solo Mode:** Includes start delays and automatic timeouts for independent use.
    * **Assisted Mode:** Allows a therapist or operator to manually control the session (Start/Pause).
* **Performance Logging:** Automatically saves session metrics (Reps, Avg Score, Latency) to a CSV file (`session_metrics/performance_log.csv`).
* **Visual Overlay:** Displays rep counts, form status (Correct/Incorrect/Perfect), and live joint angles on the screen.

## 📋 Supported Exercises
1.  **Squats** (Knee angle monitoring)
2.  **Shoulder Abduction** (Shoulder range of motion)
3.  **Elbow Flexion** (Bicep curls/rehabilitation)
4.  **Hip Flexion** (Hip joint mobility)
5.  **Wrist Extension** (Wrist rehabilitation)

## 🛠️ Tech Stack
* **Python 3.x**
* **OpenCV** (Image processing)
* **MediaPipe** (Pose estimation)
* **gTTS & Playsound** (Audio feedback)
* **NumPy** (Geometric calculations)

## 🚀 Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Yashaswini-Umesh-0304/Smart-Physiotherapy-Assistant.git
    cd Smart-Physiotherapy-Assistant

    ```

2.  **Install dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

## 💻 Usage

1.  Run the main application:
    ```bash
    python main.py
    ```

2.  **Select Mode:**
    * Type `solo` for self-training (automatic countdowns).
    * Type `assisted` for manual control.

3.  **Select Exercise:**
    * Enter one of: `squat`, `abduction`, `elbow`, `hipflex`, `wristext`.

4.  **Controls during session:**
    * `q`: Quit application.
    * `s` / `a` / `e` / `h` / `w`: Switch exercise mid-session.
    * **(Assisted Mode Only)**: Press `1` to Start/Resume, `0` to Pause.

## 📊 Analytics
After every session, the system generates a performance log in the `session_metrics` folder containing:
* Total Repetitions
* Average Accuracy Score
* Frame Processing Efficiency
* System Latency
