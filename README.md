# 📸 Guess the Photo

Guess the Photo is a lightweight, interactive web application that allows users to create custom, shareable photo-guessing quizzes. Users can upload an image, write hints, and set multiple-choice options. The app encodes the quiz data directly into a shareable URL, meaning friends can play instantly without needing to log in or rely on a backend database.

## ✨ Features

### 🛠️ Creator Mode
*   **Image Upload:** Drag-and-drop or click to upload a custom photo.
*   **Custom Answers:** Define the correct name for the photo and three tricky distractors.
*   **Dynamic Hints:** Add 1 to 3 custom questions or hints to help players guess the image before it is fully revealed.
*   **Instant Sharing:** Generates a unique, base64-encoded URL containing all quiz data. Just copy the link and share it anywhere!

### 🎮 Player Mode
*   **Progressive Reveal:** The image is initially hidden or heavily blurred. 
*   **Hint System:** Hints are presented to the player one by one.
*   **Multiple Choice:** The correct answer and distractors are randomized and presented as clickable buttons.
*   **Instant Feedback:** Players immediately find out if they guessed right, followed by a full reveal of the unblurred image.
*   **Create Your Own:** A call-to-action encourages players to build their own quiz after finishing.

## 🚀 How It Works (The URL Magic)

This application is 100% client-side. To avoid the need for a database, the app takes the uploaded image (converted to a data URI), the answers, and the hints, and compresses them into a Base64 encoded string. This string is appended to the URL as a query parameter (e.g., `?quiz=base64data`). 

When a user visits the site, the app checks the URL:
- **No query parameter?** The app loads Creator Mode.
- **Query parameter exists?** The app decodes the data and loads Player Mode.

## 💻 Tech Stack

*   **Frontend:** React / Tailwind CSS (or HTML/CSS/Vanilla JS depending on the Claude output)
*   **State Management:** React Hooks (`useState`, `useEffect`)
*   **Data Handling:** Base64 Encoding/Decoding (`btoa`, `atob`)

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/guess-the-photo.git](https://github.com/yourusername/guess-the-photo.git)
2. **Website Link:**
   https://divyesh-manickam.github.io/Photo-Guesser/
