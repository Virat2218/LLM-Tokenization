# Vocabulary Explorer: How Words Become Tokens

An interactive educational tool that visualizes how language models turn text into subword tokens and map them into a 3D semantic coordinate space.

---

## How to Open the Page

No build tools, package managers, or local dependencies are required.

### Option 1: Direct Browser Open
Double-click `index.html`, or right-click `index.html` and choose **Open With** → **Google Chrome**, **Safari**, **Firefox**, or **Brave**.

### Option 2: Local Web Server (Recommended)
You can run a lightweight local HTTP server:

```bash
# Using Python 3
python3 -m http.server 8000
```
Then open [`http://localhost:8000`](http://localhost:8000) in your web browser.

---

## Features & Usage

1. **Prominent Analysis Field:**
   - Enter any word (e.g. `algorithm`, `unfaithfulness`) or a full sentence and press **Enter** or select **Analyze**.
   - If empty, an inline helpful validation message guides you to enter text.
   - For single words, the tool displays its definition, subword breakdown, and 3D space position.
   - For sentences, the tool slices the entire phrase into individual tokens, spaces (`␣`), and punctuation with corresponding token IDs.

2. **3D Word Space:**
   - **Rotate:** Click and drag with mouse or finger.
   - **Pan:** Right-click and drag (or two-finger drag).
   - **Zoom:** Use the mouse scroll wheel or pinch on trackpads/touchscreens.
   - **Select Point:** Click any word sphere or label to smoothly focus on it and inspect its details.
   - **Neighbor Lines:** Displays dashed connection lines to its three closest neighbors in Euclidean distance.

3. **Details Panel:**
   - Shows the selected word, its part of speech, semantic category, plain-language definition, and contextual example.
   - Displays subword token chips (e.g., `al` + `gorithm`) with deterministic token IDs.
   - Lists closest nearby words in space with one-click navigation.

4. **Vocabulary List & Add Word:**
   - Browse and search all available words. The currently active word is visually highlighted.
   - Click **+ Add Word** to define a custom word with category and definition. Once saved, it is tokenized, given 3D coordinates, and rendered in the 3D space.

---

## Identification of Sample & Simulated Data

This project is an educational demonstration designed to run offline and in-browser without connecting to a proprietary backend:

- **Subword Tokenization:** Uses a rule-based simulator modeled on Byte-Pair Encoding (BPE) principles (decomposing words into prefixes, stems, suffixes, and punctuation with deterministic token IDs). Real LLMs (such as GPT-4 or Gemini) use trained tokenizer tables with 32,000–100,000+ vocabulary tokens.
- **3D Word Space Coordinates:** The 3D coordinates `[X, Y, Z]` are illustrative projections grouped by semantic domains (*Technology*, *Animals*, *Emotions*, *Daily Life*, *Science*). In production language models, embeddings reside in high-dimensional spaces (typically 768 to 4,096 dimensions) and are projected down to 2D/3D for visualization using dimensionality reduction techniques such as PCA or t-SNE.
- **Vocabulary Data:** Definitions, example sentences, and parts of speech are curated sample entries to allow immediate interactive exploration.
