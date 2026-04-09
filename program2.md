---
layout: page
title: Program
---

<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>RECOMB 2026 – Program</title>
<link href="https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@400;600;700&family=Source+Serif+4:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet" />
<style>
  :root {
    --blue:       #1a5fa8;
    --blue-light: #e8f0fb;
    --blue-mid:   #2d7dd2;
    --blue-row:   #d0e4f7;
    --accent:     #0d47a1;
    --gray-line:  #d0d7de;
    --gray-text:  #555;
    --gray-bg:    #f6f8fa;
    --white:      #ffffff;
    --radius:     4px;
    --font-body:  'Source Sans 3', sans-serif;
    --font-serif: 'Source Serif 4', serif;
  }

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body {
font-family: var(–font-body);
font-size: 15px;
color: #222;
background: var(–white);
line-height: 1.6;
}

/* ── Page header ── */
.page-header {
background: var(–blue);
color: #fff;
padding: 28px 40px 22px;
border-bottom: 3px solid var(–accent);
}
.page-header h1 {
font-family: var(–font-serif);
font-size: 1.9rem;
font-weight: 600;
letter-spacing: .02em;
}
.page-header p { font-size: .93rem; opacity: .85; margin-top: 4px; }

/* ── Container ── */
.container { max-width: 980px; margin: 0 auto; padding: 36px 24px 60px; }

/* ── Top links ── */
.top-links { margin-bottom: 28px; display: flex; gap: 16px; flex-wrap: wrap; }
.top-links a {
display: inline-block;
background: var(–blue);
color: #fff;
padding: 7px 18px;
border-radius: var(–radius);
text-decoration: none;
font-weight: 600;
font-size: .88rem;
letter-spacing: .01em;
transition: background .15s;
}
.top-links a:hover { background: var(–accent); }

/* ── Day tabs ── */
.day-tabs { display: flex; gap: 6px; flex-wrap: wrap; margin-bottom: 28px; }
.day-tab {
padding: 8px 22px;
border: 2px solid var(–blue);
border-radius: var(–radius);
background: var(–white);
color: var(–blue);
font-weight: 700;
font-size: .88rem;
cursor: pointer;
transition: background .15s, color .15s;
}
.day-tab.active, .day-tab:hover { background: var(–blue); color: #fff; }

/* ── Day panel ── */
.day-panel { display: none; }
.day-panel.active { display: block; }

/* ── Schedule table ── */
.schedule { width: 100%; border-collapse: collapse; }

/* Time slot (blue highlight rows) */
.schedule .time-row td {
background: var(–blue-row);
font-weight: 700;
color: var(–accent);
padding: 9px 14px;
font-size: .88rem;
letter-spacing: .03em;
border-top: 2px solid var(–blue);
}

/* Break / Lunch rows */
.schedule .break-row td {
background: var(–gray-bg);
color: var(–gray-text);
font-style: italic;
padding: 7px 14px;
font-size: .87rem;
border-top: 1px solid var(–gray-line);
}

/* Keynote row */
.schedule .keynote-row td {
padding: 12px 14px;
border-top: 1px solid var(–gray-line);
vertical-align: top;
}
.keynote-name {
font-weight: 700;
color: var(–blue);
font-size: 1rem;
}
.keynote-title {
font-family: var(–font-serif);
font-style: italic;
color: #333;
margin-top: 2px;
}

/* Session header row */
.schedule .session-header-row td {
background: var(–blue-light);
font-weight: 700;
color: var(–accent);
padding: 8px 14px;
font-size: .92rem;
border-top: 2px solid #b8cfe8;
letter-spacing: .015em;
}

/* Paper rows */
.schedule .paper-row td {
padding: 10px 14px 10px 28px;
border-top: 1px solid var(–gray-line);
vertical-align: top;
}
.paper-row:nth-child(even) td { background: #fafcff; }

.paper-title {
font-weight: 600;
color: #1a1a2e;
font-size: .94rem;
}
.paper-authors {
color: var(–gray-text);
font-size: .86rem;
margin-top: 2px;
}

/* Poster / Special row */
.schedule .poster-row td {
background: #fff8e1;
border-top: 2px solid #f0c040;
padding: 9px 14px;
font-weight: 700;
color: #7a5800;
font-size: .88rem;
}

/* Awards / Gala */
.schedule .event-row td {
background: #f0f4ff;
border-top: 2px solid #8faad8;
padding: 9px 14px;
font-weight: 700;
color: #2a3a6e;
font-size: .88rem;
}

/* Time cell (left column) */
.time-cell {
white-space: nowrap;
width: 130px;
color: #444;
font-size: .85rem;
vertical-align: top;
padding-top: 12px;
}

/* ── Section divider ── */
.section-label {
margin: 32px 0 10px;
font-size: 1.25rem;
font-family: var(–font-serif);
font-weight: 600;
color: var(–blue);
border-bottom: 2px solid var(–blue-row);
padding-bottom: 6px;
}

/* ── Abstract toggle button ── */
.abstract-btn {
display: inline-block;
margin-top: 6px;
padding: 3px 12px;
font-size: .78rem;
font-weight: 700;
border: 1.5px solid var(–blue-mid);
border-radius: 20px;
color: var(–blue-mid);
background: transparent;
cursor: pointer;
transition: background .13s, color .13s;
letter-spacing: .02em;
}
.abstract-btn:hover, .abstract-btn.open { background: var(–blue-mid); color: #fff; }

.abstract-box {
display: none;
margin-top: 8px;
padding: 10px 14px;
background: var(–blue-light);
border-left: 3px solid var(–blue-mid);
font-size: .88rem;
color: #333;
line-height: 1.65;
border-radius: 0 var(–radius) var(–radius) 0;
}
.abstract-box.open { display: block; }

/* ── Footer note ── */
.footer-note {
margin-top: 40px;
font-size: .84rem;
color: var(–gray-text);
text-align: center;
border-top: 1px solid var(–gray-line);
padding-top: 18px;
}
</style>

</head>
<body>

<div class="page-header">
  <h1>RECOMB 2026 &mdash; Program</h1>
  <p>International Conference on Research in Computational Molecular Biology</p>
</div>

<div class="container">

  <div class="program-links">
    <h5><a class="program-link" href="{{ '/accepted_papers.md' | relative_url }}" target="_blank">RECOMB 2026 List of Accepted Papers</a></h5>
    <h5><a class="program-link" href="https://recomb.org/proceedings/proceedings/2030-2026/2026/" target="_blank">RECOMB 2026 Proceedings</a></h5>
  </div>

  <!-- Day Tabs -->

  <div class="day-tabs">
    <button class="day-tab active" onclick="showDay(0, this)">Day 1</button>
    <button class="day-tab" onclick="showDay(1, this)">Day 2</button>
    <button class="day-tab" onclick="showDay(2, this)">Day 3</button>
    <button class="day-tab" onclick="showDay(3, this)">Day 4</button>
  </div>

  <!-- ════════════════════════════════════════ DAY 1 ════ -->

  <div class="day-panel active" id="day-0">
    <p class="section-label">Day 1</p>
    <table class="schedule">

```
  <tr class="time-row"><td colspan="2">09:00 &ndash; 09:05</td></tr>
  <tr class="keynote-row">
    <td class="time-cell"></td>
    <td><span class="keynote-name">Opening Ceremony</span></td>
  </tr>

  <tr class="time-row"><td colspan="2">09:05 &ndash; 10:05</td></tr>
  <tr class="keynote-row">
    <td class="time-cell"></td>
    <td>
      <div class="keynote-name">Keynote 1 &mdash; Paul Medvedev</div>
    </td>
  </tr>

  <tr class="break-row"><td colspan="2">10:05 &ndash; 10:30 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">10:30 &ndash; 12:20</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 1: Sequence I</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Minimizer Density revisited: Models and Multiminimizers</div>
    <div class="paper-authors">Ingels et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">MaxGeomHash: An Algorithm for Variable-Size Random Sampling of Distinct Elements</div>
    <div class="paper-authors">Hera et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Faster and Scalable Parallel External-Memory Construction of Colored Compacted de Bruijn Graphs with Cuttlefish 3</div>
    <div class="paper-authors">Khan et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Sequence-to-graph alignment based copy number calling using a network flow formulation</div>
    <div class="paper-authors">Magalhães et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Privacy-Preserving Pangenome Graphs</div>
    <div class="paper-authors">Blindenbach et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">bronko: ultrarapid, alignment-free detection of viral genome variation</div>
    <div class="paper-authors">Doughty et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">12:20 &ndash; 13:30 &nbsp;&nbsp; Lunch Break</td></tr>

  <tr class="time-row"><td colspan="2">13:30 &ndash; 15:20</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 2: Protein/ML I</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Predicting interaction-specific protein–protein interaction perturbations by missense variants with MutPred-PPI</div>
    <div class="paper-authors">Stewart et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Bacterial protein function prediction via multimodal deep learning</div>
    <div class="paper-authors">Muzio et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Evolutionary profile enhancement improves protein function annotation</div>
    <div class="paper-authors">Dai et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Integrative Multi-Scale Sequence–Structure Modeling for Antimicrobial Peptide Prediction and Design</div>
    <div class="paper-authors">Li et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">ProtFlow: Flow Matching-based Protein Sequence Design with Comprehensive Protein Semantic Distribution Learning and High-quality Generation</div>
    <div class="paper-authors">Kong et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Transforming Biological Foundation Model Representations for Out-of-Distribution Data</div>
    <div class="paper-authors">Pratapa et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">15:20 &ndash; 15:50 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">15:50 &ndash; 17:05</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 3: Single-Cell I</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Random Matrix Theory-guided sparse PCA for single-cell RNA-seq data</div>
    <div class="paper-authors">Chardès</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Gene-First Identity Construction for Robust Cell Identification in Single-Cell Transcriptomics</div>
    <div class="paper-authors">Yang et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Error Correction Algorithms for Efficient Gene Quantification in Single Cell Transcriptomics</div>
    <div class="paper-authors">Zentgraf et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Nullstrap-DE: A General Framework for Calibrating FDR and Preserving Power in Differential Expression Methods</div>
    <div class="paper-authors">Jiang et al.</div>
  </td></tr>

  <tr class="poster-row"><td colspan="2">17:05 &ndash; 19:00 &nbsp;&nbsp; Poster Session I</td></tr>
</table>
```

  </div>

  <!-- ════════════════════════════════════════ DAY 2 ════ -->

  <div class="day-panel" id="day-1">
    <p class="section-label">Day 2</p>
    <table class="schedule">

```
  <tr class="time-row"><td colspan="2">09:00 &ndash; 10:00</td></tr>
  <tr class="keynote-row">
    <td class="time-cell"></td>
    <td><div class="keynote-name">Keynote 2 &mdash; Gene Myers</div></td>
  </tr>

  <tr class="break-row"><td colspan="2">10:00 &ndash; 10:25 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">10:25 &ndash; 12:20</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 4: Sequence II</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">KuPID: Kmer-based Upstream Preprocessing of Long Reads for Isoform Discovery</div>
    <div class="paper-authors">Borowiak &amp; Yu</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">SLAB: A Sweep Line Algorithm in PBWT for Finding Haplotype Block Cores</div>
    <div class="paper-authors">Naseri et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">pHapCompass: Probabilistic Assembly and Uncertainty Quantification of Polyploid Haplotype Phase</div>
    <div class="paper-authors">Hosseini et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">On Deriving Synteny Blocks by Compacting Elements</div>
    <div class="paper-authors">Bohnenkämper et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Compressed inverted indexes for scalable sequence similarity</div>
    <div class="paper-authors">Ingels et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Fast and Flexible Flow Decompositions in General Graphs via Dominators</div>
    <div class="paper-authors">Sena &amp; Tomescu</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">12:20 &ndash; 13:30 &nbsp;&nbsp; Lunch Break</td></tr>

  <tr class="time-row"><td colspan="2">13:30 &ndash; 14:45</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 5: Multi-Omics</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Multimodal spatial alignment and morphology mapping with MOSAICField</div>
    <div class="paper-authors">Liu et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Multi-modal tissue-aware graph neural network for in silico genetic discovery</div>
    <div class="paper-authors">Aggarwal et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Modeling Multi-Modal Brain Connectomes for Brain Disorder Diagnosis via Graph Diffusion Optimal Transport Network</div>
    <div class="paper-authors">Sheng et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Achieving spatial multi-omics integration from unaligned serial sections with DIME</div>
    <div class="paper-authors">Sun et al.</div>
  </td></tr>

  <tr class="time-row"><td colspan="2">14:45 &ndash; 15:20</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 6: Small Molecules</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">SpecLig: Energy-Guided Hierarchical Model for Target-Specific 3D Ligand Design</div>
    <div class="paper-authors">Zhang et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Joint Learning of Drug-Drug Combination and Drug-Drug Interaction via Coupled Tensor-Tensor Factorization with Side Information</div>
    <div class="paper-authors">Zhang et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">15:20 &ndash; 15:50 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">15:50 &ndash; 17:05</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 7: Transcriptomics</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Summarizing RNA Structural Ensembles via Maximum Agreement Secondary Structures</div>
    <div class="paper-authors">Gu et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">CLADES - Contrastive Learning Augmented DifferEntial Splicing with Orthologous Positive Pairs</div>
    <div class="paper-authors">Talukder et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Alternet: Alternative splicing-aware gene regulatory network inference</div>
    <div class="paper-authors"></div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Deep genomic models of allele-specific measurements</div>
    <div class="paper-authors">Tu et al.</div>
  </td></tr>

  <tr class="poster-row"><td colspan="2">17:05 &ndash; 19:00 &nbsp;&nbsp; Poster Session II</td></tr>
</table>
```

  </div>

  <!-- ════════════════════════════════════════ DAY 3 ════ -->

  <div class="day-panel" id="day-2">
    <p class="section-label">Day 3</p>
    <table class="schedule">

```
  <tr class="time-row"><td colspan="2">09:00 &ndash; 10:00</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 8: Phylogeny I</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Constrained diffusion as a paradigm for evolution</div>
    <div class="paper-authors">Lazarev et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Deconvolving Phylogenetic Distance Mixtures</div>
    <div class="paper-authors">Arasti et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">A Cophylogenetic Approach for Virus-Host Interaction Prediction</div>
    <div class="paper-authors">Chowdhury et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">10:00 &ndash; 10:25 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">10:25 &ndash; 12:20</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 9: Single-Cell II</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">scDesignPop generates population-scale single-cell RNA-seq data for power analysis, method benchmarking, and privacy protection</div>
    <div class="paper-authors">Dong et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">scProfiterole: Clustering of Single-Cell Proteomic Data Using Graph Contrastive Learning via Spectral Filters</div>
    <div class="paper-authors">Coşkun et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Integrating morphology and gene expression in unpaired single-cell data using GeoAdvAE</div>
    <div class="paper-authors">Du &amp; Lin</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">MOSAIC: A Spectral Framework for Integrative Phenotypic Characterization Using Population-Level Single-Cell Multi-Omics</div>
    <div class="paper-authors">Lu et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Integrative Inference of Spatially Informed Cell Lineage Trees using LineageMap</div>
    <div class="paper-authors">Pan et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Causal gene regulatory network inference from Perturb-seq via adaptive instrumental variable modeling</div>
    <div class="paper-authors">Sun et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">12:20 &ndash; 13:30 &nbsp;&nbsp; Lunch Break</td></tr>

  <tr class="time-row"><td colspan="2">13:30 &ndash; 14:30</td></tr>
  <tr class="keynote-row">
    <td class="time-cell"></td>
    <td><div class="keynote-name">Keynote 3 &mdash; Alexandros Stamatakis</div></td>
  </tr>

  <tr class="time-row"><td colspan="2">14:30 &ndash; 15:25</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 10: Phylogeny II</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Quartet-based species tree methods enable fast and consistent tree of blobs reconstruction under the network multispecies coalescent</div>
    <div class="paper-authors">Dai et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">STELAR-X: Scaling Coalescent-Based Species Tree Inference to 100,000 Species and Beyond</div>
    <div class="paper-authors">Saha &amp; Bayzid</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">PaNDA: Efficient Optimization of Phylogenetic Diversity in Networks</div>
    <div class="paper-authors">Holtgrefe et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">15:25 &ndash; 15:55 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">15:55 &ndash; 17:10</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 11: Cancer &amp; Evolution</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Arborist: Prioritizing Bulk DNA Inferred Tumor Phylogenies via Low-pass Single-cell DNA Sequencing Data</div>
    <div class="paper-authors">Weber et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Identifying Robust Subclonal Structures Through Tumor Progression Tree Alignment</div>
    <div class="paper-authors">Wu et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Fast and accurate resolution of ecDNA sequence using Cycle-Extractor</div>
    <div class="paper-authors">Faizrahnemoon et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">POTTR: Identifying Recurrent Trajectories in Evolutionary and Developmental Processes using Posets</div>
    <div class="paper-authors">Käufler et al.</div>
  </td></tr>

  <tr class="event-row"><td colspan="2">17:30 &nbsp;&nbsp; Gala Dinner</td></tr>
</table>
```

  </div>

  <!-- ════════════════════════════════════════ DAY 4 ════ -->

  <div class="day-panel" id="day-3">
    <p class="section-label">Day 4</p>
    <table class="schedule">

```
  <tr class="time-row"><td colspan="2">09:00 &ndash; 10:00</td></tr>
  <tr class="keynote-row">
    <td class="time-cell"></td>
    <td><div class="keynote-name">Keynote 4 &mdash; Sara Mostafavi</div></td>
  </tr>

  <tr class="break-row"><td colspan="2">10:00 &ndash; 10:25 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">10:25 &ndash; 12:20</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 12: Protein/ML II</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Fast, accurate construction of multiple sequence alignments from protein language embeddings</div>
    <div class="paper-authors">Hoang et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Generating Hybrid Proteins with the MSA-Transformer</div>
    <div class="paper-authors">Tule et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Deconvolving mutation effects on protein stability and function with disentangled protein language models</div>
    <div class="paper-authors">Ding et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Quantum and Temporal Graph Neural Networks Reveal New Accuracy Limits in Predicting Protein–Ligand Dissociation Kinetics</div>
    <div class="paper-authors">Salamatov et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Protein Compositional Ratio Representation (PCRR) Systematically Improves Human Disease Prediction</div>
    <div class="paper-authors">Madduri et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Uncertainty-aware synthetic lethality prediction with pretrained foundation models</div>
    <div class="paper-authors">Hua et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">12:20 &ndash; 13:30 &nbsp;&nbsp; Lunch Break</td></tr>

  <tr class="time-row"><td colspan="2">13:30 &ndash; 15:25</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 13: Statistical Genetics</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Prediction of lifetime disease liability from EHR features</div>
    <div class="paper-authors">Di &amp; Cai</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Private Information Leakage from Polygenic Risk Scores</div>
    <div class="paper-authors">Nikitin &amp; Gürsoy</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">A biobank-scale method for learning environmental modulators of gene–environment interaction underlying complex traits</div>
    <div class="paper-authors">Liu et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Bias in genome-wide association test statistics due to omitted interactions</div>
    <div class="paper-authors">Yelmen et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">GOPHER: Optimization-based Phenotype Randomization for Genome-Wide Association Studies with Differential Privacy</div>
    <div class="paper-authors">Nandi et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Evolutionary dynamics under phenotypic uncertainty</div>
    <div class="paper-authors">Mohanty et al.</div>
  </td></tr>

  <tr class="break-row"><td colspan="2">15:25 &ndash; 15:55 &nbsp;&nbsp; Coffee Break</td></tr>

  <tr class="time-row"><td colspan="2">15:55 &ndash; 17:30</td></tr>
  <tr class="session-header-row"><td colspan="2">Session 14: Single-Cell III</td></tr>

  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">CAMP: Coreset Accelerated Metacell Partitioning enables scalable analysis of single-cell data</div>
    <div class="paper-authors">Li et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">DeltaNMF: A Two-Stage Neural NMF for Differential Gene Program Discovery</div>
    <div class="paper-authors">Karpurapu et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">Information Geometry Reconciles Discrete and Continuous Variation in Single-Cell and Spatial Transcriptomic Analysis</div>
    <div class="paper-authors">Cai et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">DiCoLo: Integration-free and cluster-free detection of localized differential gene co-expression in single-cell data</div>
    <div class="paper-authors">Li et al.</div>
  </td></tr>
  <tr class="paper-row"><td class="time-cell"></td><td>
    <div class="paper-title">CycleGRN: Inferring Gene Regulatory Networks from Cyclic Flow Dynamics in Single-Cell RNA-seq</div>
    <div class="paper-authors">Zhao et al.</div>
  </td></tr>

  <tr class="event-row"><td colspan="2">17:30 &ndash; 18:30 &nbsp;&nbsp; Closing Session &amp; Awards</td></tr>
</table>
```

  </div>

  <p class="footer-note">Questions? Email the organizers at <strong>recomb2026@gmail.com</strong></p>
</div>

<script>
  function showDay(index, btn) {
    document.querySelectorAll('.day-panel').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.day-tab').forEach(b => b.classList.remove('active'));
    document.getElementById('day-' + index).classList.add('active');
    btn.classList.add('active');
  }

  function toggleAbstract(btn) {
    const box = btn.nextElementSibling;
    const open = box.classList.toggle('open');
    btn.classList.toggle('open', open);
    btn.textContent = open ? 'Hide Abstract ▲' : 'Abstract ▼';
  }
</script>

</body>
</html>

