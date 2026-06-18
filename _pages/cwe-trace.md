---
layout: default
title: CWE-Trace
permalink: /projects/cwe-trace/
description: Calibration without comprehension — diagnosing the limits of fine-tuning LLMs for vulnerability detection in systems software
nav: false
---

<div class="ct-page">

<style>
.ct-page{
  --ct-ink:#1b1f27;
  --ct-sub:#5b6472;
  --ct-line:#e6e8ec;
  --ct-accent:#b5402a;
  --ct-accent-soft:#fbeae6;
  --ct-paranoid:#b5402a;
  --ct-skeptical:#2a5fb5;
  --ct-bg-card:#fafafa;
  color:var(--ct-ink);
  margin: 0 -1rem 3rem -1rem;
}
.ct-page *{box-sizing:border-box;}
.ct-hero{
  text-align:center;
  padding:3.2rem 1.5rem 2.4rem;
  border-bottom:1px solid var(--ct-line);
  margin-bottom:2.4rem;
}
.ct-hero h1{
  font-size:2.1rem;
  line-height:1.25;
  font-weight:700;
  max-width:880px;
  margin:0 auto 1.1rem;
  letter-spacing:-0.01em;
}
.ct-hero .ct-tag{
  display:inline-block;
  font-size:0.78rem;
  font-weight:700;
  letter-spacing:0.08em;
  text-transform:uppercase;
  color:var(--ct-accent);
  background:var(--ct-accent-soft);
  border-radius:999px;
  padding:0.3rem 0.9rem;
  margin-bottom:1.1rem;
}
.ct-hero .ct-authors{
  font-size:1.05rem;
  margin-bottom:0.3rem;
}
.ct-hero .ct-affil, .ct-hero .ct-venue{
  color:var(--ct-sub);
  font-size:0.92rem;
  margin-bottom:0.2rem;
}
.ct-links{
  display:flex;
  justify-content:center;
  gap:0.6rem;
  flex-wrap:wrap;
  margin-top:1.4rem;
}
.ct-pill{
  display:inline-flex;
  align-items:center;
  gap:0.4rem;
  padding:0.5rem 1.1rem;
  border-radius:999px;
  font-size:0.88rem;
  font-weight:600;
  border:1px solid var(--ct-line);
  color:var(--ct-sub);
  background:#fff;
}
.ct-pill.ct-soon{ opacity:0.55; cursor:default; }
.ct-stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:1px;
  background:var(--ct-line);
  border:1px solid var(--ct-line);
  border-radius:10px;
  overflow:hidden;
  margin:0 auto 2.8rem;
  max-width:980px;
}
.ct-stat{
  background:#fff;
  padding:1.2rem 0.8rem;
  text-align:center;
}
.ct-stat .ct-num{ font-size:1.5rem; font-weight:700; color:var(--ct-accent); display:block; }
.ct-stat .ct-label{ font-size:0.78rem; color:var(--ct-sub); margin-top:0.2rem; }
.ct-section{
  max-width:980px;
  margin:0 auto 3.4rem;
  padding:0 1rem;
}
.ct-section h2{
  font-size:1.5rem;
  font-weight:700;
  margin-bottom:0.3rem;
  padding-bottom:0.6rem;
  border-bottom:2px solid var(--ct-ink);
}
.ct-section h2 .ct-rq-num{ color:var(--ct-accent); }
.ct-section .ct-lede{
  color:var(--ct-sub);
  font-size:0.95rem;
  margin:0.6rem 0 1.6rem;
}
.ct-section p{ line-height:1.65; }
.ct-abstract{
  background:var(--ct-bg-card);
  border-left:4px solid var(--ct-accent);
  border-radius:6px;
  padding:1.4rem 1.6rem;
  font-size:0.98rem;
  line-height:1.7;
}
.ct-fig{ margin:1.6rem 0; text-align:center; }
.ct-fig img{
  max-width:100%;
  border:1px solid var(--ct-line);
  border-radius:8px;
}
.ct-fig figcaption{
  font-size:0.86rem;
  color:var(--ct-sub);
  margin-top:0.7rem;
  text-align:left;
  line-height:1.5;
}
.ct-fig-row{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:1.4rem;
}
@media (max-width:760px){ .ct-fig-row{ grid-template-columns:1fr; } .ct-stats{ grid-template-columns:repeat(2,1fr); } }
.ct-findings{
  display:grid;
  gap:0.9rem;
  margin-top:1.4rem;
}
.ct-finding{
  background:var(--ct-bg-card);
  border:1px solid var(--ct-line);
  border-radius:8px;
  padding:1rem 1.2rem;
}
.ct-finding .ct-finding-title{
  font-weight:700;
  font-size:0.95rem;
  margin-bottom:0.35rem;
  display:flex;
  gap:0.5rem;
  align-items:baseline;
}
.ct-finding .ct-finding-title .ct-finding-no{
  color:#fff;
  background:var(--ct-ink);
  border-radius:50%;
  width:1.5rem;
  height:1.5rem;
  min-width:1.5rem;
  display:inline-flex;
  align-items:center;
  justify-content:center;
  font-size:0.78rem;
}
.ct-finding p{ margin:0; font-size:0.92rem; color:#333; }
.ct-badge-row{ display:flex; gap:0.5rem; flex-wrap:wrap; margin-top:0.6rem; }
.ct-badge{
  font-size:0.74rem;
  font-weight:700;
  padding:0.18rem 0.6rem;
  border-radius:999px;
}
.ct-badge.paranoid{ background:#fbeae6; color:var(--ct-paranoid); }
.ct-badge.skeptical{ background:#e8eefb; color:var(--ct-skeptical); }
.ct-discuss-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:1.2rem;
  margin-top:1.2rem;
}
.ct-discuss-card{
  border:1px solid var(--ct-line);
  border-radius:8px;
  padding:1.1rem 1.3rem;
}
.ct-discuss-card h3{ font-size:1rem; margin:0 0 0.5rem; }
.ct-discuss-card p{ font-size:0.92rem; color:#333; margin:0; }
@media (max-width:760px){ .ct-discuss-grid{ grid-template-columns:1fr; } }
.ct-supp{
  background:#f6f3ee;
  border:1px dashed #cbbfa9;
  border-radius:10px;
  padding:1.6rem 1.8rem;
}
.ct-supp h2{ border-bottom:2px solid #cbbfa9; }
.ct-supp .ct-lede{ color:#7a6c52; }
.ct-supp-list{ font-size:0.92rem; line-height:1.7; columns:2; column-gap:2rem; }
@media (max-width:760px){ .ct-supp-list{ columns:1; } }
.ct-table{ width:100%; border-collapse:collapse; font-size:0.88rem; margin-top:1rem; }
.ct-table th, .ct-table td{ border:1px solid var(--ct-line); padding:0.45rem 0.7rem; text-align:right; }
.ct-table th:first-child, .ct-table td:first-child{ text-align:left; }
.ct-table thead th{ background:var(--ct-ink); color:#fff; }
.ct-table tbody tr:nth-child(even){ background:var(--ct-bg-card); }
.ct-bib{
  background:#1b1f27;
  color:#e6e8ec;
  border-radius:8px;
  padding:1.2rem 1.4rem;
  font-family:ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;
  font-size:0.82rem;
  overflow-x:auto;
  white-space:pre;
  line-height:1.55;
}
.ct-footer{
  text-align:center;
  color:var(--ct-sub);
  font-size:0.85rem;
  padding-top:1.5rem;
  border-top:1px solid var(--ct-line);
}
</style>

<div class="ct-hero">
  <span class="ct-tag">CWE-Trace · Research Project</span>
  <h1>Calibration Without Comprehension: Diagnosing the Limits of Fine-Tuning LLMs for Vulnerability Detection in Systems Software</h1>
  <div class="ct-authors">Arastoo Zibaeirad &nbsp;·&nbsp; Marco Vieira</div>
  <div class="ct-affil">University of North Carolina at Charlotte</div>
  <div class="ct-venue">azibaeir@charlotte.edu · marco.vieira@charlotte.edu</div>
  <div class="ct-links">
    <span class="ct-pill ct-soon">📄 Paper (coming soon)</span>
    <span class="ct-pill ct-soon">💻 Code (coming soon)</span>
    <span class="ct-pill ct-soon">🤗 Model weights (coming soon)</span>
  </div>
</div>

<div class="ct-stats">
  <div class="ct-stat"><span class="ct-num">834</span><span class="ct-label">curated Linux kernel samples</span></div>
  <div class="ct-stat"><span class="ct-num">74</span><span class="ct-label">distinct CWE types</span></div>
  <div class="ct-stat"><span class="ct-num">8 + 15</span><span class="ct-label">vanilla / LoRA fine-tuned models</span></div>
  <div class="ct-stat"><span class="ct-num">52.1%</span><span class="ct-label">best detection score (vs. 50% chance)</span></div>
</div>

<div class="ct-section">
<h2>Abstract</h2>
<div class="ct-abstract">
Whether LLMs scoring well on vulnerability benchmarks genuinely reason about security or merely pattern-match on contaminated data remains unresolved. We present <strong>CWE-Trace</strong>, a framework for LLM vulnerability detection built from 834 manually curated Linux kernel samples spanning 74 CWEs. The framework enforces a strict temporal split (pre-2025 historical set / post-cutoff leakage-free set), preserves context-aware vulnerable–patched pairs, and introduces two diagnostic metrics: the Directional Failure Index (DFI) and Hierarchical Distance and Direction (HDD). We evaluate eight vanilla LLMs and 15 LoRA fine-tuned variants across non-targeted detection, targeted detection, and CWE classification.
<br><br>
Our analysis yields two key results. First, <strong>data contamination provides no measurable advantage</strong> — function-level analysis shows that 84% of nominally contaminated samples carry no usable memorization signal: vulnerable functions are absent or cross-mapped across datasets, and ~31% of contaminated samples carry CWE misclassification. Second, <strong>backbone directional priors dominate fine-tuning</strong> — models exhibit stable, systematic failure modes (DFI ranging from −85.5 to +94.8 pp) that persist from historical to post-cutoff data and resist correction. Fine-tuning shifts the output threshold without changing the decision policy. This is calibration without comprehension: output distributions adapt to training data while the underlying security reasoning remains absent. The weakest backbone at binary detection (DeepSeek-R1) gains the most in coarse CWE classification, revealing that detection and understanding are decoupled capabilities. The best detection score reaches only 52.1% (+2.1 pp above chance); exact CWE ranking remains below 1.3% Top-1 accuracy, confirming that current LLMs lack reliable security reasoning for systems software, regardless of fine-tuning strategy.
</div>
</div>

<div class="ct-section">
<h2>Framework</h2>
<p class="ct-lede">A pipeline for evaluating whether fine-tuned LLMs genuinely reason about vulnerabilities, or merely calibrate their outputs to training labels.</p>
<figure class="ct-fig">
  <img src="{{ '/assets/img/cwe-trace/workflow.png' | relative_url }}" alt="CWE-Trace framework overview">
  <figcaption>Overview of the CWE-Trace framework. The pipeline begins with the extraction and manual pairing of 834 Linux kernel samples (417 pairs), strictly split into historical (PBD, ≤2024) and leakage-free (LFD, 2025) datasets. The framework evaluates diverse LLMs (both vanilla and fine-tuned) across three tasks — Non-targeted Detection, Targeted Detection, and CWE Classification — with performance assessed via a suite of metrics covering detection accuracy, pair-wise consistency, and classification ranking.</figcaption>
</figure>
<p>CWE-Trace pairs vulnerable and patched code extracted from Linux kernel commits into context-aware blocks that preserve cross-file dependencies (macros, type definitions, interacting functions) often discarded by function-isolated baselines. A strict <strong>temporal split</strong> — a Pre-cutoff Benchmark Dataset (PBD, ≤2024) and a Leakage-Free Dataset (LFD, 2025-only) — lets us separate genuine generalization from memorization. Two diagnostic metrics go beyond aggregate accuracy: the <strong>Directional Failure Index (DFI)</strong> quantifies whether a model's errors skew "paranoid" (over-flagging) or "skeptical" (under-flagging), and <strong>Hierarchical Distance and Direction (HDD)</strong> measures how far off a wrong CWE prediction lands in the CWE-1000 taxonomy graph, and in which direction.</p>
</div>

<div class="ct-section">
<h2>Why context matters: a motivating example</h2>
<figure class="ct-fig">
  <img src="{{ '/assets/img/cwe-trace/motivation_example.png' | relative_url }}" alt="CVE-2024-41010 motivating example" style="max-width:520px;">
  <figcaption>A unified diff of CVE-2024-41010. The vulnerability (Use-After-Free, CWE-416) is invisible in <code>sch_ingress.c</code> unless the model also verifies the type definition in <code>tcx.h</code> — highlighting the necessity of multi-file context for realistic vulnerability detection.</figcaption>
</figure>
</div>

<div class="ct-section">
<h2><span class="ct-rq-num">RQ1</span> — Vulnerability Detection Performance and Directional Failure</h2>
<p class="ct-lede">Do vanilla and fine-tuned LLMs actually detect vulnerabilities, or do near-50% accuracy scores hide systematic directional bias?</p>
<div class="ct-fig-row">
  <figure class="ct-fig">
    <img src="{{ '/assets/img/cwe-trace/rq1_detection_mechanisms.png' | relative_url }}" alt="RQ1 mechanism analysis">
    <figcaption>Mechanism analysis: fine-tuning deltas inside vs. outside the FT label space (a), and on contaminated vs. clean samples (b).</figcaption>
  </figure>
  <figure class="ct-fig">
    <img src="{{ '/assets/img/cwe-trace/rq1_ft_vs_vanilla_shift_map.png' | relative_url }}" alt="Fine-tuned vs vanilla shift map">
    <figcaption>Fine-tuned vs. vanilla shift map across backbones and datasets.</figcaption>
  </figure>
</div>
<div class="ct-findings">
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">1</span> Base models perform near-random with severe directional bias
      <span class="ct-badge-row"></span>
    </div>
    <p>Overall accuracy clusters at 49–53% (chance = 50%). The best vanilla model, CodeLlama, reaches only 52.1% (+2.1pp above chance). DeepSeek-R1 is strongly <span class="ct-badge paranoid">paranoid</span> (DFI +94.8pp on PBD), GPT-4.1-mini is strongly <span class="ct-badge skeptical">skeptical</span> (DFI −85.5pp), and Qwen3-4B shows near-total abstention. These patterns persist from PBD to LFD.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">2</span> Fine-tuning effect is determined by the base model's initial competence</div>
    <p>Qwen3-4B gains +27.5 to +41.5pp mainly by overcoming abstention, not by learning transferable semantics. Llama3.1 fine-tuning is mostly neutral or harmful (down to −50.7pp). DeepSeek-R1 fine-tuning consistently degrades detection while amplifying its paranoid prior.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">3</span> Label-space transfer is flat — fine-tuning shifts policy, not CWE knowledge</div>
    <p>Gains on CWEs covered by the fine-tuning label space are nearly identical to gains on uncovered CWEs, indicating a global response-policy shift rather than CWE-specific learning.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">4</span> Contamination has no detectable effect</div>
    <p>No consistent advantage of contaminated "seen-CVE" samples over clean ones across any backbone family — contamination provides no memorization shortcut.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">5</span> Context depth is necessary but not sufficient</div>
    <p>Single-function (L1) vs. multi-file/multi-function (L2) samples show almost no split-level difference — near-chance performance persists across both context depths.</p>
  </div>
</div>
</div>

<div class="ct-section">
<h2><span class="ct-rq-num">RQ2</span> — CWE-1000 Classification Before and After Fine-Tuning</h2>
<p class="ct-lede">Can models at least place a vulnerability into the correct coarse CWE-1000 root family?</p>
<figure class="ct-fig">
  <img src="{{ '/assets/img/cwe-trace/rq2_taxonomy_ft_delta_heatmap.png' | relative_url }}" alt="RQ2 taxonomy fine-tuning delta heatmap">
  <figcaption>Fine-tuning Δ Root-Micro@1 for coarse CWE-1000 classification relative to the vanilla backbone. Red = fine-tuning hurts; green = fine-tuning helps.</figcaption>
</figure>
<div class="ct-fig-row">
  <figure class="ct-fig">
    <img src="{{ '/assets/img/cwe-trace/rq2_bias_persistence.png' | relative_url }}" alt="RQ2 bias persistence">
    <figcaption>Directional bias persists from PBD to LFD.</figcaption>
  </figure>
  <figure class="ct-fig">
    <img src="{{ '/assets/img/cwe-trace/rq2_archetype_radar_charts.png' | relative_url }}" alt="RQ2 archetype radar charts">
    <figcaption>Representative per-model behavioral archetypes (radar charts).</figcaption>
  </figure>
</div>
<div class="ct-findings">
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">1</span> Base models reach moderate coarse-level accuracy but with macro disparity</div>
    <p>StarCoder2 leads on LFD at 61.0% Micro@1, but Macro@1 stays as low as 9.7–19.3% on PBD — models concentrate predictions on a narrow set of frequent root families rather than reasoning across the full taxonomy.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">2</span> Fine-tuning response is systematically backbone-dependent — and inverse to RQ1</div>
    <p>DeepSeek-R1-32B improves on every fine-tuning dataset (+9.2 to +25.9pp); Llama3.1-8B degrades on every one (down to −49.0pp). The backbone hardest to improve in detection (RQ1) can gain the most on coarse taxonomy placement.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">3</span> Binary-label fine-tuning causes catastrophic forgetting of CWE knowledge</div>
    <p>Llama3.1-8B Devign-FT drops −49.0pp on LFD Root-Micro@1 — the worst single result in the study. Devign has no CWE labels, so binary-only fine-tuning erases coarse taxonomy knowledge rather than improving it.</p>
  </div>
</div>
</div>

<div class="ct-section">
<h2><span class="ct-rq-num">RQ3</span> — Semantic Depth and Hierarchical Error</h2>
<p class="ct-lede">Can a model that recovers the broad weakness family also recover the exact CWE and place it correctly in the taxonomy?</p>
<figure class="ct-fig">
  <img src="{{ '/assets/img/cwe-trace/rq3_semantic_depth.png' | relative_url }}" alt="RQ3 semantic depth analysis">
  <figcaption>Per-model MRR ranking (a); MRR vs. HDD mean distance for fine-tuned models (b); HDD error profile — Exact / Shallow / Deep / Lateral / Invalid (c); VDISC-FT specialization on its five labeled CWEs vs. all remaining classes (d).</figcaption>
</figure>
<div class="ct-fig-row">
  <figure class="ct-fig">
    <img src="{{ '/assets/img/cwe-trace/cwe_ranking_comprehensive_analysis.png' | relative_url }}" alt="CWE ranking comprehensive analysis">
    <figcaption>Comprehensive CWE ranking analysis across all models and splits.</figcaption>
  </figure>
  <figure class="ct-fig">
    <img src="{{ '/assets/img/cwe-trace/cwe_knowledge_depth_analysis.png' | relative_url }}" alt="CWE knowledge depth analysis">
    <figcaption>CWE knowledge-depth analysis.</figcaption>
  </figure>
</div>
<figure class="ct-fig">
  <img src="{{ '/assets/img/cwe-trace/top_5_lfd_cwes_analysis.png' | relative_url }}" alt="Top 5 LFD CWEs analysis" style="max-width:680px;">
  <figcaption>Per-class error breakdown for the five most frequent LFD CWEs.</figcaption>
</figure>
<div class="ct-findings">
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">1</span> CWE exact identification is unsolved</div>
    <p>Best vanilla Top-1 on LFD is 14.71% (GPT-4.1-mini); best MRR is 27.55%. DeepSeek-R1 and StarCoder2 score 0% Top-1. Exact semantic recovery remains rare across the board.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">2</span> Lateral errors are the universal dominant failure mode (86.5% mean)</div>
    <p>Across all eight vanilla models, 86.5% of wrong predictions land at the correct hierarchy depth but in the wrong sibling branch — only 4.2% are exact matches. Models reach the right specificity level but not the correct sibling category.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">3</span> MRR and HDD are only weakly coupled — validating HDD as a distinct diagnostic</div>
    <p>Qwen3-Coder reaches MRR = 14.61% on LFD but HDD mean distance = 6.22, while Llama3.1 has lower MRR (5.52%) yet tighter hierarchical proximity (HDD = 4.95). Ranking correctness and hierarchical proximity are not the same signal.</p>
  </div>
  <div class="ct-finding">
    <div class="ct-finding-title"><span class="ct-finding-no">4</span> VDISC specialization is sharp (+33.3pp) but trades hierarchical plausibility for exact match</div>
    <p>On samples within VDISC's five labeled classes, VDISC-FT improves Top-1 by up to +33.3pp — but the same models are flat-to-worse outside those classes. Fine-tuning trades "plausibly related wrong" predictions for "exactly right or unrelated" ones: narrow supervision produces brittle specialization.</p>
  </div>
</div>
</div>

<div class="ct-section">
<h2>Discussion</h2>
<p class="ct-lede">Two results explain why LLM-based vulnerability detection remains unreliable — and point toward where the field should focus next.</p>
<div class="ct-discuss-grid">
  <div class="ct-discuss-card">
    <h3>The backbone's directional prior dominates fine-tuning</h3>
    <p>Near-random accuracy (~50%) masks extreme, stable, backbone-determined directional bias. <span class="ct-badge skeptical">Skeptical</span> models (e.g. GPT-4.1-mini) default to "Safe"; <span class="ct-badge paranoid">paranoid</span> models (e.g. DeepSeek-R1, CodeLlama) flag nearly all complex C code as vulnerable. Selecting a backbone is selecting a failure mode — fine-tuning mostly shifts the output threshold, not the underlying decision policy.</p>
  </div>
  <div class="ct-discuss-card">
    <h3>Fine-tuning decouples detection from understanding</h3>
    <p>VDISC fine-tuning produces large exact-Top-1 gains on its five labeled classes but not on uncovered ones — a narrow supervised label set without transferable root-cause semantics. Detection and exact semantic diagnosis move on largely independent axes.</p>
  </div>
  <div class="ct-discuss-card">
    <h3>CVE-level contamination does not yield a detectable advantage</h3>
    <p>CVE-level overlap does not imply function-level memorization: the vulnerable function evaluated in PBD was frequently absent from training. Combined with label noise (~31% CWE misclassification) and a 51:1 safe-context-to-root-cause supervision ratio, an estimated 84% of nominally contaminated samples carry no usable memorization signal.</p>
  </div>
  <div class="ct-discuss-card">
    <h3>Implications for reliability</h3>
    <p>The bottleneck is not dataset size but the structure and fidelity of the supervision signal. A more promising path: training data that pairs each CVE with its root-cause function, plus fine-tuning methods (e.g. contrastive or DPO-style objectives on paired vulnerable/patched examples) that explicitly counter directional collapse rather than assuming balanced supervision alone will fix it.</p>
  </div>
</div>
</div>

<div class="ct-section ct-supp">
<h2>Supplementary material</h2>
<p class="ct-lede">Material from the project's appendix and broader experiment suite that didn't fit in the main paper.</p>

<figure class="ct-fig">
  <img src="{{ '/assets/img/cwe-trace/rq2_appendix_complete_radar_charts.png' | relative_url }}" alt="Complete per-model radar charts (appendix)">
  <figcaption>Appendix — complete per-model behavioral radar charts for all 8 vanilla and 15 fine-tuned models (the main paper shows only representative archetypes from this set in Figure RQ2).</figcaption>
</figure>

<p>Beyond the contamination analysis reported in the paper (Table: CWE label accuracy on contaminated samples — 281 samples audited across PrimeVul, MegaVul, and LineVul, 68.7% combined CWE-label accuracy), the full audit pipeline ran nine function-level contamination experiments:</p>
<table class="ct-table">
  <thead><tr><th>Dataset</th><th>Total contaminated</th><th>Correct CWE</th><th>Incorrect CWE</th><th>Accuracy</th></tr></thead>
  <tbody>
    <tr><td>PrimeVul</td><td>88</td><td>61</td><td>27</td><td>69.3%</td></tr>
    <tr><td>MegaVul</td><td>144</td><td>94</td><td>46</td><td>67.1%</td></tr>
    <tr><td>LineVul</td><td>49</td><td>38</td><td>11</td><td>77.6%</td></tr>
    <tr><td><strong>Combined</strong></td><td><strong>281</strong></td><td><strong>193</strong></td><td><strong>88</strong></td><td><strong>68.7%</strong></td></tr>
  </tbody>
</table>

<div class="ct-supp-list">
<ul>
  <li><strong>Exp 1 — SVD/HPS by source.</strong> Per-model semantic-vulnerability-detection (SVD) and hierarchical-prediction-score (HPS) breakdown on PrimeVul- and MegaVul-contaminated samples.</li>
  <li><strong>Exp 2 — Code similarity.</strong> Best-match code similarity between PBD CVEs and PrimeVul/MegaVul candidates, to verify whether "contaminated" samples are actually near-duplicates.</li>
  <li><strong>Exp 3 — HPS / HDD breakdown.</strong> Exact / parent / child / sibling / same-root / unrelated decomposition per model.</li>
  <li><strong>Exp 4 — CWE consistency.</strong> Cross-checks PBD ground-truth CWE labels against PrimeVul and MegaVul's labels for the same CVEs.</li>
  <li><strong>Exp 5 — Label bias.</strong> Vulnerable vs. safe label ratios per contaminated CVE in the training corpora.</li>
  <li><strong>Exp 6 — Class imbalance.</strong> Training vulnerable-class percentage vs. predicted vulnerable-class percentage, per model.</li>
  <li><strong>Exp 7 — VDISC CWE coverage.</strong> Performance on VDISC's five labeled CWEs vs. all other CWEs, PBD and LFD.</li>
  <li><strong>Exp 8 — Exact-match case study.</strong> Qualitative case studies of exact-match predictions.</li>
  <li><strong>Exp 9 — Cross-architecture.</strong> Training-set vulnerable-class percentage and balancing strategy vs. accuracy, across backbone architectures.</li>
</ul>
</div>
</div>

<div class="ct-section">
<h2>Citation</h2>
<div class="ct-bib">@misc{zibaeirad2026calibration,
  title  = {Calibration Without Comprehension: Diagnosing the Limits of
            Fine-Tuning LLMs for Vulnerability Detection in Systems Software},
  author = {Zibaeirad, Arastoo and Vieira, Marco},
  year   = {2026},
  note   = {University of North Carolina at Charlotte},
}</div>
</div>

<div class="ct-footer">
  University of North Carolina at Charlotte &nbsp;·&nbsp; azibaeir@charlotte.edu / marco.vieira@charlotte.edu
</div>

</div>
