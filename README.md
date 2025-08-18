# OrthoNet: Outstanding Orthodontist for Talking Face Synthesis  

> **No More Artifactual Teeth in Talking Face Generation**  
> Official implementation of the paper: *Outstanding Orthodontist: No More Artifactual Teeth in Talking Face* (Su et al., 2025)  

---

## ✨ Overview  

Audio-driven talking face synthesis (TFS) enables generating realistic speaking videos from a single portrait image and a speech audio clip.  
However, existing methods often struggle with **temporal inconsistency and artifacts in the teeth region**, leading to unnatural results.  

We propose **OrthoNet**, a **plug-and-play framework** that works as a *virtual orthodontist* for existing Audio2Video methods.  

**Key Contributions:**  
- 🦷 **Detail-oriented Teeth Aligner** — Preserves teeth details and adapts to shape changes during lip movements.  
- 🧠 **Memory-guided Teeth Stabilizer** — Combines long-term and short-term memory to ensure temporal consistency.  
- 🔌 **Plug-and-Play** — Can be integrated with existing talking face models (e.g., AniPortrait, Audio2Head, Hallo2).  
- 🎥 **Improved Realism** — Eliminates hallucinations, preserves teeth edges, and maintains stability under occlusion.  

---

## 🏗 Framework  

<p align="center">  
  <img src="docs/framework.png" alt="OrthoNet Framework" width="600"/>  
</p>  

*Figure: OrthoNet consists of two main modules — the Detail-oriented Teeth Aligner (dual-branch DRM-Conv + PKConv) and the Memory-guided Teeth Stabilizer (LTM + STM with cross-attention).*  

---

## 📊 Experimental Results  

### Quantitative Metrics  
| Method              | TSM ↑ | ECI ↑ | SSIM ↑ | FVD ↓ |
|---------------------|-------|-------|--------|-------|
| AniPortrait         | 0.753 | 4.068 | 0.847  | 238.5 |
| **+ OrthoNet**      | **0.847** | **4.321** | **0.884**  | **233.8** |
| Audio2Head          | 0.662 | 3.968 | 0.899  | 242.4 |
| **+ OrthoNet**      | **0.785** | **4.213** | **0.907**  | **237.9** |
| Hallo2              | 0.686 | 3.953 | 0.879  | 158.2 |
| **+ OrthoNet**      | **0.813** | **4.249** | **0.906**  | **153.6** |

OrthoNet consistently improves **teeth stability, edge clarity, and temporal coherence** across multiple baselines.  

---

### Visual Comparisons  

<p align="center">  
  <img src="docs/qualitative.png" alt="Qualitative Results" width="700"/>  
</p>  

*Figure: Comparison between baseline methods (green box) and OrthoNet-enhanced results (red box). Our method significantly improves teeth stability and realism under different occlusion conditions.*  

---

## 🎬 Demo Videos  

Here we showcase demo results of OrthoNet applied to various baselines:  

- 🔗 [Demo 1: AniPortrait + OrthoNet](demo/aniportrait.mp4)  
- 🔗 [Demo 2: Hallo2 + OrthoNet](demo/hallo2.mp4)  
- 🔗 [Demo 3: EchoMimic + OrthoNet](demo/echomimic.mp4)  

*(Please upload your own demo videos in `demo/` folder and update the links above.)*  

## Acknowledgments
Parts of this project page were adopted from the [Nerfies](https://nerfies.github.io/) page.

## Website License
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
