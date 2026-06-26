# Vercel - AI-Powered Mental Health Support

An AI-powered mental wellness platform that provides early emotional health assessment, personalized AI support, and engaging self-care experiences to help users improve their overall well-being. Built with ❤️ for a healthier mind.

![Image](https://github.com/user-attachments/assets/bb946441-117b-4cb3-bffc-37bb401afc85)

---


## 📜 About The Project

In a world where good mental health is more important than ever, finding instant, private and non-judgmental support can be a challenge. **Vercel** was built to address that gap. It’s not a replacement for professional therapy but a **emotional first-aid kit** that offers early detection, personalized support and a safe place for users to understand and manage their feelings.

Our goal is to develop an empathetic, easy-to-use tool that utilizes technology to assist users in beginning their wellness journey. This project was created for [Name of Hackathon] with the aim of making mental health support universally accessible.

### ✨ Key Features

Vercel is packed with a diverse set of features, each designed with a specific therapeutic purpose in mind:

*   🗣️ **Multi-Lingual AI Analysis:** Users can express their feelings in English, Spanish, Hindi, or Urdu. The AI analyzes the text to provide insights on emotion and risk level.
*   🎭 **Personalized AI Personas:** Get advice from a "Father," "Mother," "Best Friend," or even a "Therapist." The AI's response style changes based on your selection for a more comforting experience.
*   🧸 **My Comfort Box:** A personal, digital safe space featuring powerful interactive tools:
    *   **🗑️ The Thought-Shredder:** Based on Cognitive Behavioral Therapy (CBT), this tool allows users to type out a negative thought and visually "shred" it, providing a tangible sense of control and release.
    *   **🎙️ Voice Affirmation Recorder:** Users can record kind and encouraging messages to their future selves. Hearing one's own calm voice is a powerful grounding technique during moments of distress.
    *   **✨ Item Curation:** Save quotes, notes, music links, or image URLs that bring you peace and comfort.
*   💖 **Anonymous Community Stories:** A feed where users can read and share short, positive stories about overcoming struggles. Vote on stories that resonate with you, creating a supportive and hopeful community.
*   📝 **Mental Health & Well-being Quiz:** A GAD-7 and PHQ-9 inspired questionnaire that provides a wellness score and actionable recommendations based on the user's responses.
*   🎵 **Calming Music Player:** A curated selection of ambient and calming music tracks to help users relax, focus, or meditate.
*   🎮 **Comfort Games:** Simple, non-goal-oriented games designed for stress relief and mindfulness:
    *   **🧘 Zen Garden:** Mindfully rake digital sand.
    *   **💧 Bubble Pop:** The simple, satisfying act of popping bubble wrap.
*   🎁 **Kindness Cache:** A surprise pop-up that appears once per session to deliver a random, positive compliment to the user.

---

### 🛠️ Tech Stack

This project was built from the ground up using core web technologies, with a focus on a client-side, no-backend implementation suitable for a hackathon.

*   **Front-End:** `HTML5`, `CSS3` (utilizing Flexbox & Grid for layout), `JavaScript (ES6+)`
*   **APIs:**
    *   **Google Gemini API:** For all generative AI-powered analysis and responses.
    *   **Web Speech API:** For voice-to-text input.
    *   **MediaRecorder API:** For recording and saving voice affirmations.
*   **Storage:** `localStorage` and `sessionStorage` are used to persist user data (tasks, comfort box items, etc.) directly in the browser, ensuring privacy.

---

### 🚀 Getting Started

To get a local copy up and running, follow these simple steps. This project requires an API key from Google to power its AI features.

#### Installation & Setup

1.  **Get a Free Google AI API Key:**
    *   Navigate to [Google AI Studio](https://aistudio.google.com/).
    *   Sign in and click **"Get API key"** > **"Create API key in new project"**.
    *   Copy the generated key. You'll need it in a moment.

2.  **Clone the repository:**
    ```sh
    git clone https://github.com/KingHero11211/Vercel.git
    ```
3.  **Navigate to the project directory:**
    ```sh
    cd Vercel
    ```
4.  **Set Up Your API Key:**
    *   In the project folder, you will find a file named `config.example.js`.
    *   **Rename** this file to `config.js`.
    *   Open the new `config.js` file and **paste your API key** into the placeholder string.

    ```javascript
    // Before (in config.example.js)
    const API_KEY = "PASTE_YOUR_GOOGLE_AI_API_KEY_HERE";

    // After (in your new config.js)
    const API_KEY = "AIzaSy...your...actual...key...";
    ```
    > The `config.js` file is listed in `.gitignore` to ensure your secret key is never committed to GitHub.

5.  **Run the application:**
    *   **The Easy Way (Recommended):** If you use Visual Studio Code, install the **[Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)** extension. Right-click on `HTML.html` and select "Open with Live Server".
    *   **The Simple Way:** You can also just open the `HTML.html` file directly in your web browser.
    
    > **Note:** Using a live server is recommended because some browser features, especially the `MediaRecorder` API, may have security restrictions that prevent them from working when a file is opened directly from the local filesystem (`file:///...`).

---

### ☁️ Deployment on Vercel

You can easily deploy this project to Vercel. To make the AI work on the live site, you need to set the API key as a secure environment variable.

1.  Push your project to GitHub (ensure `config.js` is in your `.gitignore`).
2.  Import the project into Vercel from your GitHub repository.
3.  In the Vercel project dashboard, go to **Settings -> Environment Variables**.
4.  Add a new variable:
    *   **Name:** `GOOGLE_API_KEY`
    *   **Value:** Paste your actual API key here.
5.  Go to **Settings -> Build & Development Settings**.
6.  Find the **Build Command** field, toggle it ON, and enter the following command:
    ```bash
    echo "const API_KEY = '$GOOGLE_API_KEY';" > config.js
    ```
7.  **Redeploy** your project. The build command will create the `config.js` file on Vercel's server before your site goes live, allowing the AI to function correctly.

---

### 📂 Project Structure

The project is organized to be simple and easy to navigate, with API keys handled securely.

```
/
├── 📂 assets/
│   ├── 🔊 audio/         # Contains audio files for the music player
│   └── 🖼️ images/       # Contains images for album art and UI icons
├── 📄 .gitignore         # Tells Git to ignore config.js
├── 📄 config.example.js  # A template for the API key configuration
├── 📄 HTML.html           # The main structure and content
├── 🎨 CSS.css             # All styling, animations, and layout
├── ⚙️ JAVA.js             # All application logic and interactivity
└── 📖 README.md           # You are here!
```

---

### 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

1.  **Fork the Project**
2.  **Create your Feature Branch** (`git checkout -b feature/AmazingFeature`)
3.  **Commit your Changes** (`git commit -m 'Add some AmazingFeature'`)
4.  **Push to the Branch** (`git push origin feature/AmazingFeature`)
5.  **Open a Pull Request**

---

### ⚖️ License

Distributed under the MIT License.

---

### 📬 Contact

Sakshi  - [sakshi.ai.686@gmail.com](mailto:sakshi.ai.686@gmail.com)

Project Link: [https://github.com/Sakshiiii00/Vercel.git](https://github.com/Sakshiiii00/Vercel.git)

### 🙏 Acknowledgments
* Special thanks to the organizers of **Pixel Palette – IEEE RAS MUJ** for hosting the event.
* Appreciation to the open-source community for providing the libraries, icons, and assets used in this project.
* Inspired by the concepts of Cognitive Behavioral Therapy (CBT) and mindfulness techniques.