<h1 align="center">Hi, I'm Anirudh 👋</h1>

<p align="center">
  <b>Senior Research Engineer · Vision-Language Models Team Lead at <a href="https://bharatgen.com/">BharatGen</a></b>
</p>

<p align="center">
  <a href="https://srini-anirudh.github.io/"><img alt="Website" src="https://img.shields.io/badge/Website-srini--anirudh.github.io-1f6feb?style=for-the-badge"/></a>
  <a href="https://srini-anirudh.github.io/blogs/"><img alt="The Backward Pass" src="https://img.shields.io/badge/Blog-The%20Backward%20Pass-d1242f?style=for-the-badge"/></a>
  <a href="https://scholar.google.com/citations?hl=en&user=bhm5TBQAAAAJ"><img alt="Google Scholar" src="https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=googlescholar&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/anirudh-srini/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://x.com/Anirud_Srini"><img alt="X" src="https://img.shields.io/badge/@Anirud__Srini-000000?style=for-the-badge&logo=x&logoColor=white"/></a>
</p>

I'm a senior research engineer at BharatGen, where I lead the vision-language models team. My work covers answers that point to evidence on the page, the infrastructure for training and serving VLMs, and sovereign foundation models for India.

I write long-form explainers on how modern AI works, and each one comes with code you can run.

---

## 📖 The Backward Pass

**The Backward Pass is my blog series.** It explains how modern AI models are built, trained and scaled, from first principles. 70+ articles, interactive figures, cited sources, and a runnable lab for each theory post.

| | | |
|:--:|:--:|:--:|
| [<img src="https://srini-anirudh.github.io/blogs/what-autograd-actually-does/preview.png" width="290"/>](https://srini-anirudh.github.io/blogs/what-autograd-actually-does/) | [<img src="https://srini-anirudh.github.io/blogs/inside-a-training-step/preview.png" width="290"/>](https://srini-anirudh.github.io/blogs/inside-a-training-step/) | [<img src="https://srini-anirudh.github.io/blogs/build-attention-from-scratch/preview.png" width="290"/>](https://srini-anirudh.github.io/blogs/build-attention-from-scratch/) |
| **[What Autograd Actually Does](https://srini-anirudh.github.io/blogs/what-autograd-actually-does/)**<br/>Backpropagation from scalar chain rules to saved tensors and checkpointing | **[Inside a Training Step](https://srini-anirudh.github.io/blogs/inside-a-training-step/)**<br/>Shapes, FLOPs, activation lifetimes, optimizer state and memory | **[Build Attention From Scratch](https://srini-anirudh.github.io/blogs/build-attention-from-scratch/)**<br/>MHA, GQA, MLA and tiled online softmax, tested against SDPA |

**Read:** [all articles](https://srini-anirudh.github.io/blogs/) · **Run:** [12 coding tutorials and a lab for every post](https://github.com/srini-anirudh/blog-coding-tutorials) · **Subscribe:** [RSS](https://srini-anirudh.github.io/feed.xml)

---

## 🔬 Research interests

I work on three connected problems. Each links to its page, its papers and its write-ups.

### 1. [Grounded document intelligence](https://srini-anirudh.github.io/research.html#grounded-document-intelligence)

*Turn pages into text without losing information, and ground every answer in the page with masks.*

Converting a document to text loses information, so we built a representation that keeps everything on the page: text, hierarchy, position and style. And a model that types out coordinates is a brittle way to ground an answer. People mark the page instead, so the VLM decides *what* to ground and *at what granularity*, and SAM highlights *where* as a mask.

**Thesis:** [Building Grounded Document Intelligence](https://srini-anirudh.github.io/blogs/building-grounded-document-intelligence/) · [talk and slides](https://srini-anirudh.github.io/research/docai-talk/)

```mermaid
flowchart LR
  R["<b>REPLICA</b><br/>page → lossless HTML<br/>ICDAR 2026 · Oral"] -- "generates training data for" --> M["<b>M3Grounder</b><br/>mask-based grounded VQA<br/>CVPR 2026"]
  M --> D["<b>DoCoG</b><br/>grounded chain-of-thought<br/>ECCV 2026 · Spotlight"]
  L["<b>DocLayout-VL</b><br/>promptable layout masks<br/>ECCV 2026"] -. "closes the loop" .-> R
```

<table>
  <tr>
    <td align="center" width="25%"><a href="https://srini-anirudh.github.io/blogs/replica-visually-faithful-document-reconstruction/"><img src="https://srini-anirudh.github.io/blogs/replica-visually-faithful-document-reconstruction/preview.png" width="230"/></a><br/><b>REPLICA</b><br/>Visually faithful document reconstruction<br/><sub>ICDAR 2026 · Oral</sub><br/><a href="https://replica-agents.github.io/">project</a> · <a href="https://srini-anirudh.github.io/blogs/replica-visually-faithful-document-reconstruction/">blog</a></td>
    <td align="center" width="25%"><a href="https://srini-anirudh.github.io/blogs/m3grounder-mask-based-document-grounding/"><img src="https://srini-anirudh.github.io/blogs/m3grounder-mask-based-document-grounding/preview.png" width="230"/></a><br/><b>M3Grounder</b><br/>Multi-span, multi-granular grounding<br/><sub>CVPR 2026</sub><br/><a href="https://m3grounder.github.io/">project</a> · <a href="https://srini-anirudh.github.io/blogs/m3grounder-mask-based-document-grounding/">blog</a></td>
    <td align="center" width="25%"><a href="https://srini-anirudh.github.io/blogs/docog-grounded-chain-of-thought/"><img src="https://srini-anirudh.github.io/blogs/docog-grounded-chain-of-thought/preview.png" width="230"/></a><br/><b>DoCoG</b><br/>Mask-based grounded chain-of-thought<br/><sub>ECCV 2026 · Spotlight</sub><br/><a href="https://docog-eccv.github.io/">project</a> · <a href="https://srini-anirudh.github.io/blogs/docog-grounded-chain-of-thought/">blog</a></td>
    <td align="center" width="25%"><a href="https://srini-anirudh.github.io/blogs/doclayout-vl-promptable-layout-segmentation/"><img src="https://srini-anirudh.github.io/blogs/doclayout-vl-promptable-layout-segmentation/preview.png" width="230"/></a><br/><b>DocLayout-VL</b><br/>Hierarchical, open-set, promptable layout<br/><sub>ECCV 2026</sub><br/><a href="https://doclayoutvl.github.io/">project</a> · <a href="https://srini-anirudh.github.io/blogs/doclayout-vl-promptable-layout-segmentation/">blog</a></td>
  </tr>
</table>

### 2. [VLM infrastructure](https://srini-anirudh.github.io/research.html#vlm-infrastructure)

*The whole stack that builds a sovereign vision foundation model, from storage to evaluation.*

<p align="center">
  <a href="https://srini-anirudh.github.io/research.html#vlm-infrastructure"><img src="assets/patram-stack.png" alt="The Patram stack, read from the bottom up: Storage (Patram-FS, Patram-DB); Raw data collection (Patram-Scraper, synthetic docs) and Annotation and visualisation (DarshinAI); Training data generation (Patram-Ingest); Training infrastructure (Patram-Core); Models (Patram suite); Evaluation (PatramBench, Patram-Eval)" width="760"/></a><br/>
  <sub>The Patram stack, read from the bottom up.</sub>
</p>

**Patram-Ingest** wraps vLLM in durable execution, so data-generation runs that last weeks keep GPUs busy and survive node failures. Talks: [guest lecture at IIIT Hyderabad](https://srini-anirudh.github.io/talks/programming-ai-accelerators/) · [vLLM Meetup Mumbai 2026](https://srini-anirudh.github.io/talks/patram-ingest-slides/)

### 3. [Sovereign foundation models](https://srini-anirudh.github.io/research.html#sovereign-foundation-models)

*The Patram series: India's document VLM, and the benchmark that measures it.*

- **[Patram](https://bharatgen.com/products/patram/)**: a vision-language model for Indian document understanding, built over BharatDocs, a corpus of 20M+ documents and 250M+ pages in English and 22 Indian languages. [Weights](https://huggingface.co/bharatgenai/patram-7b-instruct)
- **[Patram-Bench](https://patrambench.github.io/)** (ICDAR 2026): 52,607 documents, 23 languages, 52 tasks, 2.4M+ QA annotations, 29 VLMs evaluated.
- **e-vikrAI**: [Indic VLMs for e-commerce](https://bharatgen.com/products/e-vikrai/).

---

## 💻 Code

| Repo | What it is |
|---|---|
| [**blog-coding-tutorials**](https://github.com/srini-anirudh/blog-coding-tutorials) | 12 code-first tutorials, from PyTorch basics to VLM training and agent RL, plus one runnable lab with measured results for each post on the blog |
| [**srini-anirudh.github.io**](https://github.com/srini-anirudh/srini-anirudh.github.io) | Source of the website and blog |

<p align="center"><sub>Everything above is written up at <a href="https://srini-anirudh.github.io/">srini-anirudh.github.io</a>.</sub></p>
