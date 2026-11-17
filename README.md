# LLM Words & Sentences 3D Embedding Explorer

An interactive educational website demonstrating how Large Language Models (LLMs) process both **words** and **full sentences**: from subword tokenization to unified 3D semantic vector coordinates.

---

## How to Open the Website

No build tools, package managers, or local dependencies are required.

### Option 1: Open Directly in Any Browser
- Double-click `index.html`, or
- Right-click `index.html` and choose **Open With** → **Google Chrome**, **Safari**, **Firefox**, or **Brave**.

### Option 2: Run via a Local Server (Recommended)
```bash
# Using Python 3:
python3 -m http.server 8000
```
Then visit [`http://localhost:8000`](http://localhost:8000) in your browser.

---

## Features & 3D Sentence Capabilities

1. **Words & Sentences in the Same 3D Space:**
   - **Words (Round Spheres):** Represent single lexical items clustered by semantic domains (*Technology*, *Animals*, *Emotions*, *Daily Life*, *Science*).
   - **Sentences (Rotating Diamonds):** Full phrases mapped directly into the 3D space near related words (e.g. *"Neural networks learn vector representations through training"* sits beside `neural` and `algorithm`).
   - **Display Filter:** Toggle between **All Items**, **Words Only**, or **Sentences Only** with one click.
   - **Neighbor Connection Lines:** Shows dashed Euclidean distance lines linking sentences to their closest related words and sentences.

2. **Top Analyze Bar (Instant 3D Plotting):**
   - Type any word or complete sentence into the input bar and click **Analyze & Plot in 3D**.
   - The engine automatically tokenizes the input, calculates its semantic cluster and coordinates, renders a new point in the 3D space, and smoothly flies the camera to it.

3. **Details Inspector:**
   - Displays whether the active item is a **Word** or **Sentence**.
   - Shows the full text, definition/context, 3D coordinates `[X, Y, Z]`, and nearest neighbors in space.
   - Breaks down the item into subword and punctuation tokens with their corresponding integer token IDs.

4. **Tokenizer Lab:**
   - Test full sentences to see subwords, punctuation, and spaces (`␣`) represented as distinct colored badges.
   - Statistics on character count, token count, and characters-per-token ratio.
   - Detailed mapping table with token order, types (root, subword, space, punctuation), and lengths.
   - Includes a **"Plot Sentence in 3D Space"** button to immediately visualize the analyzed text in the 3D universe.

5. **Add Word / Sentence Modal:**
   - Select either **Word** or **Sentence / Phrase**.
   - Live token preview updates in real-time as you type.
   - Choose a semantic category to plot your custom entry into its corresponding 3D neighborhood.

6. **Directory:**
   - Searchable, filterable catalog of all words and sentences with category and type filters.

---

## Identification of Sample & Simulated Data

- **Subword Tokenization:** Uses a rule-based simulator modeled on Byte-Pair Encoding (BPE) principles with deterministic token IDs. Real LLMs use trained tokenizer tables with 32,000–100,000+ vocabulary tokens.
- **3D Word Space Coordinates:** The 3D coordinates `[X, Y, Z]` are illustrative projections grouped by semantic domains (*Technology*, *Animals*, *Emotions*, *Daily Life*, *Science*). In production language models, embeddings reside in high-dimensional spaces (typically 768 to 4,096 dimensions) and are projected down to 2D/3D for visualization using dimensionality reduction techniques such as PCA or t-SNE.
- **Sentence Embeddings:** Illustrates how modern sentence embedding architectures (such as Sentence-BERT) map complete thoughts into the same vector space as words.
