# Breath-Bloom Fractal Flower 🌸✨

An interactive, bio-responsive generative art experience built with **p5.js** and **p5.sound.js**. By enabling your microphone and blowing into it, you breathe life into a digital seedling, causing a glowing, hand-drawn **Dragon Curve Fractal Flower** to bloom dynamically on your screen. When you stop, the flower gently retracts back into a pulsing seed.

---

## 🌟 Features

*   **Breath-Responsive Bloom**: Uses microphone amplitude to drive the organic growth and retraction of the fractal flower.
*   **Dragon Curve L-System**: The flower's skeleton is generated programmatically using an L-system:
    *   **Axiom**: `FX`
    *   **Rule X**: `X+YF+`
    *   **Rule Y**: `-FX-Y`
    *   **Angle**: 90°
*   **Hand-Illustrated Aesthetic**: Combines a dark slate-grey paper texture with neon brushstrokes (yellow, lime green, magenta, blue), translucent petals, glowing radial backlighting, and rising pollen particles.
*   **Asymmetric Growth Physics**: The flower blooms rapidly with active breathing and folds back slowly and gracefully when the breathing stops.
*   **One-Tap Calibration**: Tap or click anywhere on the canvas to instantly recalibrate the microphone noise floor to adapt to ambient surroundings.
*   **Mobile-Friendly & Zero Build Tools**: Built completely in vanilla HTML, CSS, and JS using CDNs. No npm install or build steps required.

---

## 🚀 Running Locally

To run the application locally on your computer:

1.  Open your terminal.
2.  Navigate to the `fractal-flower` directory (if not already there).
3.  Start a local HTTP server using Python:
    ```bash
    python3 -m http.server 8000
    ```
4.  Open your web browser and go to:
    ```text
    http://localhost:8000
    ```

---

## 📱 Testing on Your Phone

To test the microphone-driven interaction on a mobile device, the site must be served over a secure connection (`https`) or accessed via your computer's local IP address (which most mobile browsers trust for microphone access on local networks).

1.  Find your computer's local IP address.
    *   **macOS / Linux**: Run `ipconfig getifaddr en0` or `ifconfig | grep "inet "` in terminal.
    *   **Windows**: Run `ipconfig` in Command Prompt.
    *   *Example local IP: `192.168.1.15`*
2.  Start the Python server on your computer:
    ```bash
    python3 -m http.server 8000
    ```
3.  Ensure your phone and computer are connected to the **same Wi-Fi network**.
4.  On your phone's browser, navigate to:
    ```text
    http://<YOUR-COMPUTER-IP>:8000
    ```
    *(e.g., `http://192.168.1.15:8000`)*
5.  Tap the screen to enable the microphone and enjoy!

---

## 🌐 Deploying to GitHub Pages

To publish your prototype to the web for free using GitHub Pages, follow these steps:

1.  **Initialize Git & Commit**:
    ```bash
    git init
    git add .
    git commit -m "Initial breath bloom prototype"
    git branch -M main
    ```
2.  **Add Remote and Push**:
    Create a new empty repository on GitHub named `fractal-flower` and run:
    ```bash
    git remote add origin https://github.com/YOUR-USERNAME/fractal-flower.git
    git push -u origin main
    ```
3.  **Enable GitHub Pages**:
    *   Go to your repository on GitHub.
    *   Click on **Settings** (gear icon) → **Pages** (in the left sidebar under "Code and automation").
    *   Under **Build and deployment**:
        *   **Source**: Select *Deploy from a branch*.
        *   **Branch**: Select *main* and folder */ (root)*.
        *   Click **Save**.
4.  **Visit Your Site**:
    Your application will be live in a couple of minutes at:
    ```text
    https://YOUR-USERNAME.github.io/fractal-flower/
    ```

---

## ✍️ Editing & Pushing Updates

Whenever you make changes to `index.html` and want to push them live to GitHub Pages:

```bash
git add index.html
git commit -m "Update visual styles and behavior"
git push origin main
```
Your live site will update automatically within seconds!
