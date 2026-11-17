# LLM Word Processing Explorer

An interactive educational website demonstrating how Large Language Models (LLMs) process human words: from raw text to subword tokens, token IDs, and 3D embedding vector spaces.

---

## How to Open and Run

No installations, build steps, or local dependencies are required.

### Option 1: Open Directly in Any Browser
- Double-click `index.html`, or
- Right-click `index.html` and select **Open With** → **Google Chrome**, **Safari**, **Firefox**, or **Brave**.

### Option 2: Run via a Simple Local Server (Recommended)
If you prefer running via a local web server:

```bash
# Using Python 3:
python3 -m http.server 8000
```
Then visit [`http://localhost:8000`](http://localhost:8000) in your browser.

---

## Features & How to Use

1. **3D Word Space (Embeddings)**:
   - **Rotate & Zoom:** Click and drag with your mouse (or touch and drag on mobile) to rotate the 3D universe; use the scroll wheel or pinch to zoom; right-click and drag to pan.
   - **Interactive Points:** Click any floating glowing word sphere to inspect its part of speech, definition, token breakdown, simulated 8-dimensional embedding vector, and 3D coordinates.
   - **Semantic Clustering & Nearest Neighbors:** See dotted lines connecting the selected word to its 3 closest semantic neighbors (e.g. *algorithm* connects to *neural* and *computer*).
   - **Category Filters:** Use the category buttons (**Technology**, **Animals**, **Emotions**, **Food**, **Science**) to filter words and jump between clusters.
   - *Note on illustrative positions:* 3D coordinates demonstrate semantic proximity. Real-world language models typically use 768 to 4096 dimensions.

2. **Tokenizer Playground**:
   - Type any sentence, phrase, or word into the live input box or click one of the quick sample presets.
   - Watch the text split into distinct, color-coded **subword tokens** in real-time.
   - Review token IDs, character counts, and the character-to-token ratio in the detailed token table.

3. **Vocabulary Explorer**:
   - Browse the curated word database with definitions, example sentences, and token counts.
   - Search by word, definition, or category.
   - Click **View in 3D** on any card to immediately focus the 3D camera on that word.

4. **Add a Word**:
   - Click the green **+ Add Word** button in the header.
   - Type a new word, choose its semantic category, and optionally add a definition and example sentence.
   - See an instant preview of its subword tokenization.
   - When submitted, the word is immediately calculated, placed inside its category cluster, rendered in the 3D space, and focused by the camera.

---

## File Structure

- `index.html` — Complete standalone application (HTML structure, Tailwind CSS styling, Three.js 3D visualization, and JavaScript logic).
- `README.md` — Guide on how to open and explore the application.

