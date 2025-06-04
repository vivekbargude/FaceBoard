

# Facial Movement Controlled Virtual Keyboard System

An open-source Human-Computer Interaction (HCI) project that uses facial landmarks and eye-blink detection to simulate keyboard input using only facial movements. This application enables users to select characters on a virtual keyboard through column scanning and blink detection — empowering hands-free communication and accessibility.

---

## Table of Contents

* [Project Overview](#project-overview)
* [Features](#features)
* [Getting Started](#getting-started)
* [Installation & Setup](#installation--setup)
* [Usage](#usage)
* [Technologies Used](#technologies-used)
* [Contributing](#contributing)
* [Credits](#credits)

---

## Project Overview

This project leverages **OpenCV**, **dlib**, and facial landmark detection to implement a virtual keyboard navigable using **eye blinks** and **column-row scanning** logic. It’s ideal for accessibility applications or touchless interfaces where traditional input methods are impractical.

---

## Features

✅ Real-time facial landmark detection
✅ Virtual keyboard grid with character highlighting
✅ Blink-controlled character selection
✅ Column-row scanning mechanism
✅ Works on standard webcam input

---

## Getting Started

Follow these steps to run the project locally on your machine.

### 1. Clone or Download the Repository

```bash
git clone https://github.com/vivekbargude/FaceBoard.git
cd FaceBoard
```

---

## Installation & Setup

### 2. Install Required Python Libraries

Make sure you have **Python 3.6+** installed.

```bash
pip install opencv-python dlib numpy
```

> 💡 **Note:** Installing `dlib` may require CMake and Visual Studio Build Tools on Windows.

### 3. Download Pretrained Shape Predictor

Download the `shape_predictor_68_face_landmarks.dat` file from:
🔗 [http://dlib.net/files/shape\_predictor\_68\_face\_landmarks.dat.bz2](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)

Extract it and place it in the desired location (update the path in the script accordingly):

```python
predictor = dlib.shape_predictor("path_to/shape_predictor_68_face_landmarks.dat")
```

---

## Usage

### 4. Run the Application

```bash
python facial_keyboard.py
```

> Make sure your webcam is connected and accessible.

---

## How It Works

1. **Face Detection**: Uses dlib to detect face and 68 facial landmarks.
2. **Column Scanning**: Columns are highlighted sequentially.
3. **Blink to Select Column**: When the user blinks, the currently highlighted column is selected.
4. **Row Scanning**: Rows in the selected column are scanned.
5. **Blink to Select Character**: Another blink selects the character, which is added to the text buffer.

> Escape key `ESC` exits the program.

---

## Technologies Used

* **Python 3.6+**
* **OpenCV** – Real-time image processing
* **dlib** – Face detection and landmark estimation
* **NumPy** – Array operations

---

## Contributing

We welcome contributions to improve functionality and performance.

1. Fork the repo
2. Clone it:

   ```bash
   git clone https://github.com/vivekbargude/FaceBoard.git
   ```
3. Make your changes and test locally
4. Submit a pull request

---

## Credits

Developed by: **Vivek Bargude**

Inspired by accessibility challenges and advancements in facial gesture interfaces.

---

