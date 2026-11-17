# LLM Vocabulary & Tokenization Explorer

An interactive educational website demonstrating how Large Language Models (LLMs) process human words: from raw text to subword tokens, token IDs, and 3D embedding vector spaces.

---

## How to Open the Website

No build tools, package managers, or local dependencies are required.

### Option 1: Open Directly in Any Browser
- Double-click `index.html`, or
- Right-click `index.html` and select **Open With** → **Google Chrome**, **Safari**, **Firefox**, or **Brave**.

### Option 2: Run via a Local Server (Recommended)
```bash
# Using Python 3:
python3 -m http.server 8000
```
Then visit [`http://localhost:8000`](http://localhost:8000) in your browser.

---

## Features & Navigation

1. **Top Quick Analyze Bar:**
   - Type any word, rare term, or full sentence into the search field and click **Analyze** (or press <kbd>Enter</kbd>).
   - Single words are immediately focused in the 3D space and details panel.
   - Sentences automatically open in the Tokenizer Lab.

2. **3D Word Space (Primary Tab):**
   - **Rotate & Zoom:** Click and drag with your mouse (or touch and drag on mobile) to rotate; use scroll wheel or pinch to zoom; right-click and drag to pan.
   - **Interactive Points & Readable Sprites:** Each word is rendered with high-contrast text labels that always face the camera.
   - **Details Inspector:** Clicking any word displays its definition, context example, subword tokens with IDs, and nearest semantic neighbors.
   - **Neighbor Lines:** Toggle dashed Euclidean distance lines connecting the selected word to its closest neighbors.
   - **Semantic Clusters:** Quick filter buttons for **Technology**, **Animals**, **Emotions**, **Daily Life**, and **Science**.
   - **Quick Word Selector:** Click any word in the side pill cloud to instantly fly the camera to it.

3. **Tokenizer Lab (Dedicated Tab):**
   - Test any sentence or custom text to see how language models slice text into tokens.
   - Color-coded visual token badges with character spans and token IDs.
   - Statistics bar showing character count, token count, and characters-per-token ratio.
   - Full Token ID mapping table detailing token order, type (root, prefix, suffix, space `␣`, punctuation), and length.
   - Educational guide explaining why models use subword tokenization (handling rare words, fixed vocabulary size, space preservation).

4. **Vocabulary Grid (Full Directory Tab):**
   - Searchable, filterable card directory of all vocabulary words.
   - Filter by category or search by word/definition.
   - Each card displays parts of speech, definitions, example sentences, and token badges, with a **"View in 3D"** button.

5. **Add Word Modal:**
   - Click the green **+ Add Word** button in the header.
   - Type any word to see real-time subword tokenization before saving.
   - Plots the new word into its semantic cluster in 3D space, adds it to the vocabulary directory, and focuses the camera on it.

---

## Identification of Sample & Simulated Data

- **Subword Tokenization:** Uses a rule-based simulator modeled on Byte-Pair Encoding (BPE) principles with deterministic token IDs. Real LLMs use trained tokenizer tables with 32,000–100,000+ vocabulary tokens.
- **3D Word Space Coordinates:** The 3D coordinates `[X, Y, Z]` are illustrative projections grouped by semantic domains (*Technology*, *Animals*, *Emotions*, *Daily Life*, *Science*). In production language models, embeddings reside in high-dimensional spaces (typically 768 to 4,096 dimensions) and are projected down to 2D/3D for visualization using dimensionality reduction techniques such as PCA or t-SNE.
- **Vocabulary Data:** Definitions, example sentences, and parts of speech are curated sample entries to allow immediate interactive exploration.
