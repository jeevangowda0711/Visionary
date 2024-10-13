# Visionary - Blind Assistance Application

Visionary is a sophisticated web-based application designed to assist visually impaired users in navigating their surroundings through the use of speech recognition, image processing, and geolocation technologies. The app leverages AI-powered audio responses, real-time video streams, and sensor-based motion detection to provide blind users with a reliable tool for navigating their environment safely and efficiently.

## Features

### 1. **Real-Time Audio and Video Processing**
   - **Audio Recording & Image Capture:** The application allows users to initiate recordings by shaking their device or tapping on the screen. The system captures audio and video streams in real-time using the device’s microphone and camera.
   - **Audio and Image Processing with Gemini AI:** The captured audio and image data are processed using the **Gemini API**, providing detailed descriptions of the user's surroundings, object detection, and safe navigation instructions.

### 2. **Voice Navigation Assistance**
   - **Geolocation & Mapbox Integration:** Visionary uses the device’s GPS capabilities to fetch the user’s current location and provides step-by-step navigation instructions to a desired destination using the **Mapbox Directions API**.
   - **Google Places API:** The system allows users to search for nearby points of interest, such as stores or landmarks, and provides the most direct route using Google Places for geolocation data.

### 3. **Motion and Gesture Detection**
   - **Device Motion Detection:** Visionary detects device movements (such as shaking) using accelerometer data and initiates audio recording or resets the application based on the intensity of the motion.
   - **Double Tap Interaction:** Users can control the app through tactile gestures such as double-tapping to stop audio playback or reset the application. Interaction detection ensures the app is responsive and easy to control even for users with limited mobility.

### 4. **Text-to-Speech (TTS) Support**
   - **Google Cloud Text-to-Speech Integration:** Visionary uses **Google Cloud's Text-to-Speech** API to provide audio feedback in multiple languages, including English, Spanish, Hindi, and many more. The audio is generated in real-time, offering users contextual responses in their preferred language.
   - **Dynamic Language Detection:** The app dynamically detects the language used in queries and provides audio responses in the same language for a more personalized user experience.

### 5. **Error Handling & User Guidance**
   - **Permission Request Handling:** The app ensures that all necessary permissions (camera, microphone, geolocation) are granted before operation. If permissions are denied, clear error messages guide the user on how to resolve the issue.
   - **Geolocation Error Handling:** If the app cannot determine the user’s location or there are issues with the GPS, it provides audio prompts to guide the user on enabling location services or suggests alternative ways to gather location data.

### 6. **Auditory Feedback for User Actions**
   - **Auditory Feedback:** Every user interaction (such as tapping or shaking) triggers auditory feedback, providing confirmation that the action has been recognized and processed. This is key for ensuring that the app is intuitive and accessible for blind users.
   - **Playback Control & Audio Cues:** The app plays synthesized speech responses to users and allows for seamless audio control, ensuring that no instruction or prompt is missed during the interaction.

### 7. **Backend AI Processing**
   - **Gemini AI for Contextual Understanding:** Visionary’s backend uses the **Gemini API** to understand context and generate intelligent responses. Whether the input is a question about surroundings, a directional query, or a general search, the app responds appropriately.
   - **AI-Driven Decision Making:** The app intelligently determines when to trigger navigation, search for information, or offer contextual guidance based on the user’s input and environmental conditions.

### 8. **Security & Performance**
   - **Cross-Origin Resource Sharing (CORS):** Visionary ensures secure interaction with external APIs through proper CORS policies, allowing safe communication between the frontend and backend.
   - **Efficient Media Handling:** The system efficiently handles large files such as audio and image uploads, ensuring minimal latency and smooth user experience.

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jeevangowda0711/Visionary.git
   ```

2. **Navigate to the project directory:**
   ```bash
   cd Visionary
   ```

3. **Create and activate a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # For Linux/Mac
   # OR
   venv\Scripts\activate  # For Windows
   ```

4. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Set up environment variables:**
   - Create a `.env` file in the project root directory and include the following:
     ```
     GEMINI_API_KEY=<Your-Gemini-API-Key>
     GOOGLE_APPLICATION_CREDENTIALS=<Path-to-Google-Credentials-JSON>
     MAPBOX_API_KEY=<Your-Mapbox-API-Key>
     GOOGLE_PLACES_API_KEY=<Your-Google-Places-API-Key>
     ```

6. **Run the application:**
   ```bash
   uvicorn main:app --reload
   ```

7. **Access the application:**
   Open your browser and go to `http://127.0.0.1:8000/` to start using Visionary.

---

## Usage

- **Audio & Image Input:** Tap the microphone button or shake the device to start recording. The app will process the audio and captured image and provide a response.
- **Navigation Queries:** Ask for directions by saying, “How do I get to [location]?” and follow the step-by-step instructions.
- **Object Identification:** Point the camera at objects and ask, “What is this?” The app will analyze the image and respond with details.

---

## Technologies Used

- **FastAPI** for the backend server and API handling.
- **Google Cloud Text-to-Speech API** for generating real-time audio responses.
- **Gemini AI API** for intelligent contextual responses.
- **Mapbox API** for location-based navigation services.
- **Google Places API** for finding nearby locations.
- **HTML, JavaScript (Vanilla), TailwindCSS** for the frontend.
- **Python** for backend scripting and media processing.

---

## Future Enhancements

- **Improve Speech-to-Text Capabilities:** Adding support for continuous speech recognition to allow users to interact without manual input.
- **Advanced Image Recognition:** Incorporating more advanced image recognition for better object detection.
- **Voice Command-Based App Navigation:** Enabling users to control the app entirely through voice commands, eliminating the need for any tactile input.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
