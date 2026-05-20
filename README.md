# 🐍 Hands-on Python — AI Frontier Day 2

> **Session by Mr. K. Akshay Kumar** · Python & AI App Dev, Kovan Labs  
> CIT Summer Internship "AI Frontier" · 20 May 2026 · 9:30 AM – 12:30 PM

This repo has everything from the **Hands-on Python** session — the slides, the student follow-along site with all 11 code snippets, and the full Google Colab notebook.

---

## 🔗 Quick links

| | |
|--|--|
| 🎞 **Slides** | [ai-frontier-python/slides.html](https://akshaykumar-1729.github.io/ai-frontier-python/slides.html) |
| 📋 **All snippets** | [ai-frontier-python](https://akshaykumar-1729.github.io/ai-frontier-python/) |
| 📓 **Colab notebook** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AkshayKumar-1729/ai-frontier-python/blob/main/notebook/session_notebook.ipynb) |

---

## ⚠️ One-time Colab setup (read this first)

Run **Snippet 0** the moment you open the notebook — it installs all packages and pre-downloads ~800 MB of AI model weights while you follow along.

**After Snippet 0 finishes installing, you must restart once:**

> **Runtime → Restart session** → then **Run All** (Ctrl+F9)

**Why the restart?** Colab boots with NumPy 2.x already loaded in memory. This session pins `numpy<2.0` so MediaPipe 0.10.21 works correctly. The downgrade lands on disk but the running Python process still holds the old version in RAM. Without a restart, any import touching NumPy's C extension crashes:

```
ValueError: numpy.dtype size changed, may indicate binary incompatibility.
```

A runtime restart flushes memory and loads the pinned version fresh. The second run of the install cell is fast — packages are already cached.

---

## 📦 What's in the notebook

| # | Snippet | What it does |
|---|---------|-------------|
| 0 | **Warm-up** | Install all packages, pre-download AI model weights |
| 1 | **Phone filenames** | Variables, lists, list comprehensions — real filenames from your gallery |
| 2 | **EXIF photo rename** | Read EXIF metadata with Pillow, rename every photo to `YYYY-MM-DD_HH-MM-SS.jpg` |
| 3 | **Duplicate finder** | MD5 fingerprint every file, group by hash to find identical copies |
| 4 | **Background remover** | Three lines of Python, a U-2-Net neural network does the rest |
| 5 | **Hacker News scraper** | requests + BeautifulSoup, CSS selectors, live headlines |
| 6 | **Tamil film stats** | `pd.read_html()` pulls every Wikipedia table into a DataFrame in one line |
| 7 | **Browser automation** | Playwright — the same pattern that books Tatkal tickets while you sleep |
| 8 | **Sentiment analysis** | HuggingFace Transformers + DistilBERT: is this tweet happy or angry? |
| 9 | **Face mesh** | MediaPipe maps 468 landmarks on your face live via webcam |
| 10 | **Emotion & age** | DeepFace reads age, gender, and emotion from your selfie |
| 11 | **Gradio web app** | Four lines = FastAPI backend + frontend + public `gradio.live` URL + QR code |

---

## 📚 Sources & further reading

### Libraries
- [Pillow](https://pillow.readthedocs.io/) — image reading & EXIF metadata
- [rembg](https://github.com/danielgatis/rembg) — U-2-Net background removal
- [requests](https://requests.readthedocs.io/) + [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/) — web scraping
- [pandas](https://pandas.pydata.org/) — `read_html()` for Wikipedia tables
- [HuggingFace Transformers](https://huggingface.co/docs/transformers/) — NLP pipeline
- [MediaPipe Face Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker) — 468 facial landmarks
- [DeepFace](https://github.com/serengil/deepface) — emotion / age / gender detection
- [Gradio](https://www.gradio.app/) — instant web app with public URL
- [Playwright (Python)](https://playwright.dev/python/) — browser automation

### Models & datasets
- [DistilBERT SST-2](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english) — the sentiment model used in Snippet 8
- [Stanford Sentiment Treebank](https://nlp.stanford.edu/sentiment/treebank.html) — human-labelled movie reviews that trained it
- [U-2-Net paper (arXiv)](https://arxiv.org/abs/2005.09007) — salient object detection architecture
- [DUTS Saliency Dataset](https://www.kaggle.com/datasets/balraj98/duts-saliency-detection-dataset) — 10k labelled images U-2-Net was trained on
- [FER2013](https://www.kaggle.com/datasets/msambare/fer2013) — 35k facial emotion images DeepFace was trained on
- [mini-Xception architecture](https://github.com/oarriaga/face_classification) — the CNN behind DeepFace emotion detection

### Interesting links from the session
- [CommonCrawl](https://commoncrawl.org/) — the petabyte-scale open web scrape powering many LLMs
- [Lok Sabha constituencies](https://en.wikipedia.org/wiki/List_of_constituencies_of_the_Lok_Sabha) — the Wikipedia table we scraped live
- [Hacker News](https://news.ycombinator.com/) — live headlines scraped in Snippet 5

---

*Built with Google Colab · Slides and snippet site hosted on GitHub Pages.*
