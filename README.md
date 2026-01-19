# Fork & Spoon Detector

An Android application that detects and counts forks and spoons in real-time using YOLOv8 and TensorFlow Lite.

![Android](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?logo=kotlin&logoColor=white)


## Features

- **Real-time Object Detection**: Detects forks and spoons using the camera feed
- **Object Counting**: Automatically counts the number of each detected object
- **YOLOv8 Model**: Utilizes YOLOv8 TensorFlow Lite model for accurate detection
- **Native Android**: Built with Kotlin for optimal performance

## 🎥 Demo Video

<div align="center">

[![Watch Demo](https://img.shields.io/badge/▶️_Watch-Demo_Video-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://drive.google.com/file/d/1qePCMwdRH0j1spucQvEdS14BH8ML_p7e/view?usp=sharing)


</div>

## Technologies Used

- **Language**: Kotlin
- **UI Framework**: XML Layouts
- **ML Framework**: TensorFlow Lite
- **Detection Model**: YOLOv8
- **Vision Library**: TensorFlow Lite Task Vision Library

## Requirements

- Android Studio Arctic Fox or later
- Minimum SDK: 24 (Android 7.0)
- Target SDK: 34 (Android 14)
- Camera permission required

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/fork-spoon-detector.git
```

2. Open the project in Android Studio

3. Sync Gradle files

4. Build and run the application on your device or emulator

## Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/com/example/
│   │   │   ├── MainActivity.kt
│   │   │   ├── ObjectDetector.kt
│   │   │   └── ...
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   │   └── activity_main.xml
│   │   │   └── ...
│   │   └── assets/
│   │       └── yolov8_model.tflite
│   └── ...
└── build.gradle
```

## Dependencies

Add the following dependencies to your `build.gradle` file:

```gradle
dependencies {
    // TensorFlow Lite
    implementation 'org.tensorflow:tensorflow-lite:2.14.0'
    implementation 'org.tensorflow:tensorflow-lite-support:0.4.4'
    implementation 'org.tensorflow:tensorflow-lite-task-vision:0.4.4'
    
    // Camera
    implementation 'androidx.camera:camera-camera2:1.3.0'
    implementation 'androidx.camera:camera-lifecycle:1.3.0'
    implementation 'androidx.camera:camera-view:1.3.0'
}
```

## Usage

1. Launch the app
2. Grant camera permission when prompted
3. Point your camera at forks and/or spoons
4. The app will automatically detect and count the objects
5. Detection results and counts are displayed on screen in real-time

## Model Information

- **Model**: YOLOv8 TensorFlow Lite
- **Detected Classes**: Fork, Spoon
- **Input Size**: 640x640 (or your specific input size)
- **Format**: TensorFlow Lite (.tflite)

## Permissions

The app requires the following permission:

```xml
<uses-permission android:name="android.permission.CAMERA" />
```

## How It Works

1. The app captures frames from the device camera using CameraX
2. Each frame is preprocessed and fed to the YOLOv8 TensorFlow Lite model
3. The model outputs bounding boxes, class labels, and confidence scores
4. Detected objects are filtered by confidence threshold
5. Forks and spoons are counted separately and displayed on the UI

## Future Enhancements

- [ ] Add support for more utensil types
- [ ] Implement object tracking across frames
- [ ] Add statistics and history
- [ ] Save detection results
- [ ] Improve model accuracy with custom training

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## Acknowledgments

- YOLOv8 by Ultralytics
- TensorFlow Lite team
- Android CameraX library

## 👨‍💻 Author

**[Himanshu Arya]**

- GitHub: [Himanshu Arya](https://github.com/hkarya625)

Project Link: [https://github.com/hkarya625/fork-spoon-detector](https://github.com/hkarya625/object-detection-app)

---

⭐ Star this repo if you find it helpful!
