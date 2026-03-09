# Algorithms Supported By Essentia 

## CHATGPT OVERVIEW 
<hr>
# DJ Set-List Organizer: Feature Prioritization for Song Similarity / Mixability

For a **DJ set-list organizer by “song similarity / mixability”**, the most useful features are those that capture:

- Tempo + groove  
- Key / chords  
- Energy / loudness dynamics  
- Timbre (sound palette)  

---

## 🔥 Highest Value for DJ Similarity (Use These First)

### 🎵 Rhythm & Timing (Mixability)

- Beat detection / BPM  
- Onset detection  
- Rhythm transform  
- Beat loudness  

**Why:** Lets you match tracks by BPM, detect half-time/double-time feel, and compare groove density.

---

### 🎹 Tonal / Harmonic (Harmonic Mixing)

- HPCP (chroma) / chroma-related features  
- Key and scale  
- Chords  
- Tuning frequency  

**Why:** Key compatibility + chord vibe is huge for “these tracks blend well.”

---

### ⚡ Energy / Dynamics (Set Flow)

- Loudness, Leq, Vickers’ loudness  
- Envelope descriptors (attack time, envelope shape)  
- Dynamic complexity  

**Why:** Helps you avoid energy cliffs, plan build-ups, and match “punchiness.”

---

### 🎛 Timbre / Texture (Sounds-Like Similarity)

- MFCC (and optionally GFCC)  
- Spectral contrast  
- Spectral peaks / roll-off / HFC  

**Why:** Groups tracks that feel similar sonically (bright/dark, crisp/washed, percussive/airy).

---

## 🟡 Medium Value (Nice Add-Ons Once Basics Work)

### 🎚 Spectral Bands

- Mel / Bark / ERB bands  

**Why:** Useful for “brightness / bassiness” summaries and coarse similarity.

---

### 🧩 Segmentation / Structure

- Audio segmentation  

**Why:** Can help align intros/outros, find drops, breakdowns, and build a “transition map.”

---

### 💃 Danceability (Genre-Dependent)

- Danceability  

**Why:** Sometimes correlates with “club-ready feel,” but can be noisy depending on style.

---

## 🔵 Lower Value / Mostly Internal Tools (Not Primary Features)

### Signal Processing Blocks

- FFT / DCT  
- Frame cutter  
- Windowing  
- Smoothing  

These are **building blocks**, not similarity features by themselves.

---

### Filters

- FIR / IIR  
- DC removal  
- Equal loudness  

These are **preprocessing tools**, not descriptors.

---

### Statistical Moments

- Kurtosis  
- Skewness  
- Other raw statistical moments  

Can help as auxiliary features, but rarely drive DJ-relevant similarity alone.

---

## 🤖 ML Models (How They Fit)

### If You Have Labeled Examples  
(“These two tracks go well together”)

- Use **SVM / TensorFlow inference**  
- Learn a **mixability score**

### If You Don’t Have Labels (Common Case)

- Build feature vectors  
- Use **nearest neighbors / clustering**  
  - kNN  
  - Cosine distance  
  - UMAP + HDBSCAN  

---

## 🎯 A Practical “DJ Similarity Vector” (Simple + Strong Baseline)

Start with:

- BPM + beat histogram / rhythm transform  
- Key + HPCP  
- Loudness + dynamic complexity + attack time  
- MFCC statistics + spectral contrast  

This combination usually captures:

- Same tempo family  
- Harmonic compatibility  
- Similar energy level  
- Similar sonic vibe  

---

If you tell me your target genres (house / tech-house / EDM / hip-hop / DnB, etc.), I can suggest a **feature set + weighting strategy** tailored to that style (for example, house prioritizes groove + timbre, while melodic techno leans more heavily on key and chords).