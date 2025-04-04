# emotion-detection-by-using-Cnn<img width="1181" alt="Screenshot 2025-04-04 at 4 31 46 PM" src="https://github.com/user-attachments/assets/86ed7ab0-06b5-4dec-8439-eaac4ddf7636" />
# Emotion Detection Streamlit App

This application uses a Convolutional Neural Network to detect and classify emotions in faces. The model is trained on the FER2013 dataset and can recognize 7 different emotions: Angry, Disgust, Fear, Happy, Neutral, Sad, and Surprise.

## Features

- **Upload Image**: Analyze emotions in uploaded images
- **Webcam Integration**: Real-time emotion detection using your webcam
- **Adjustable Parameters**: Control face detection sensitivity and confidence thresholds
- **Statistics Display**: View detailed information about detected faces and emotions


 

2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Create a `model` directory and place your trained model files in it:
   ```bash
   mkdir -p model
   ```
   
   You need to have the following files in the model directory:
   - `network_emotions.json`: The model architecture
   - `weights_emotions.hdf5`: The trained model weights

## Usage

Run the Streamlit app:
```bash
streamlit run app.py
```

The application will open in your default web browser.

### Interface Options

1. **Upload Image Tab**:
   - Upload an image containing faces
   - View the detected emotions with confidence scores
   - See statistics about the detected faces

2. **Webcam Tab**:
   - Use your webcam for real-time emotion detection
   - Start/stop the webcam with a button click
   - See live statistics about detected emotions

3. **Sidebar Controls**:
   - Adjust the confidence threshold for predictions
   - Modify face detection parameters like scale factor, minimum neighbors, and minimum face size

## Model Information

The emotion detection model is based on a Convolutional Neural Network architecture with:
- Multiple convolutional layers with batch normalization
- Max pooling layers for downsampling
- Dropout layers to prevent overfitting
- Dense layers for final classification

The model was trained on the FER2013 dataset, which contains facial expressions categorized into 7 emotions.

## Requirements

- Python 3.7+
- TensorFlow 2.x
- OpenCV
- Streamlit
- NumPy

See `requirements.txt` for the complete list of dependencies.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
