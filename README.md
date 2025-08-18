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
  <img src="static/images/framework2.png" alt="OrthoNet Framework" width="600"/>  
</p>  

*Figure: OrthoNet consists of two main modules — the Detail-oriented Teeth Aligner (dual-branch DRM-Conv + PKConv) and the Memory-guided Teeth Stabilizer (LTM + STM with cross-attention).*  

---



### Visual Comparisons  

<p align="center">  
  <img src="static/images/Qualitative-Results-1.png" alt="Qualitative Results" width="700"/>  
</p>  

*Figure: Comparison between baseline methods (green box) and OrthoNet-enhanced results (red box). Our method significantly improves teeth stability and realism under different occlusion conditions.*  

---

## 🎬 Demo Videos  

Here we showcase demo results of OrthoNet applied to various baselines:  

<p align="center">
  <img src="static/gif/hallo2.gif" width="600"/>
</p>
<div align="center">
  <figcaption style="font-weight: bold;">
    <span style="color: #007bff;">◀ Left: Hallo2</span>
    &nbsp;|&nbsp;
    <span style="color: #28a745;">Right: Hallo2 + Ours ▶</span>
  </figcaption>
</div>

<p align="center">
  <img src="static/gif/joyhallo.gif" width="600"/>
</p>
<div align="center">
  <figcaption style="font-weight: bold;">
    <span style="color: #007bff;">◀ Left: JoyHallo</span>
    &nbsp;|&nbsp;
    <span style="color: #28a745;">Right: JoyHallo + Ours ▶</span>
  </figcaption>
</div>

<p align="center">
  <img src="static/gif/aniportraint.gif" width="600"/>
</p>
<div align="center">
  <figcaption style="font-weight: bold;">
    <span style="color: #007bff;">◀ Left: AniPortrait</span>
    &nbsp;|&nbsp;
    <span style="color: #28a745;">Right: AniPortrait + Ours ▶</span>
  </figcaption>
</div>

<p align="center">
  <img src="static/gif/audio2head.gif" width="600"/>
</p>
<div align="center">
  <figcaption style="font-weight: bold;">
    <span style="color: #007bff;">◀ Left: Audio2Head</span>
    &nbsp;|&nbsp;
    <span style="color: #28a745;">Right: Audio2Head + Ours ▶</span>
  </figcaption>
</div>

<p align="center">
  <img src="static/gif/echomimic.gif" width="600"/>
</p>
<div align="center">
  <figcaption style="font-weight: bold;">
    <span style="color: #007bff;">◀ Left: EchoMimic</span>
    &nbsp;|&nbsp;
    <span style="color: #28a745;">Right: EchoMimic + Ours ▶</span>
  </figcaption>
</div>


## Acknowledgments
Parts of this project page were adopted from the [Nerfies](https://nerfies.github.io/) page.

## Website License
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
