---
permalink: /projects/ActionValuationBenchmark/
author_profile: true
---

<div class="post">
  <header class="project-title" style="text-align: center; margin-top: 2em">
    <h1 class="project-title" style="font-weight: bold; color: #404040">Benchmarking Action Valuation in Football: From Standardized Evaluation to Systematic Spatio-Temporal Model Design</h1>
    <p class="project-venue" style="font-size: 1.0em;">Submitted</p>
    <h3>
      <a href="https://scholar.google.es/citations?user=MNdw5eYAAAAJ&amp;hl=en" rel="external nofollow noopener" target="_blank">Artur Xarles</a>,
      Arnau Barrera-Roy,
      <a href="https://scholar.google.com/citations?user=oI6AIkMAAAAJ&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Sergio Escalera</a>,
      <a href="https://scholar.google.es/citations?user=XmkDts4AAAAJ&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Thomas B. Moeslund</a>, and
      <a href="https://scholar.google.es/citations?user=n4BtpPsAAAAJ&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Albert Clapés</a>
    </h3>
  </header>

  <div style="margin-top: 20px">
    <figure>
      <img src="/images/AV_task.jpg" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" alt="BenchBomb action valuation task">
    </figure>
  </div>

  <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
    <div class="project-narrow" id="abstract" style="text-align: justify;">
      <h3 style="text-align: center;">Abstract</h3>
      <i>Action Valuation (AV) in football aims to assign values to individual player actions reflecting their quality and contribution to team performance, supporting applications in sports analytics. Despite the growing number of AV methods, systematic comparison remains challenging due to limited public datasets and the lack of standardized evaluation protocols. Existing methods are therefore often assessed using different datasets, valuation formulations, and evaluation settings, limiting direct and reproducible comparison. To address this gap, we introduce BenchBomb, an AV benchmark built on StatsBomb Open Data that provides standardized data partitions and a common evaluation protocol for heterogeneous AV methods. Inspired by player-valuation approaches, BenchBomb evaluates action values through their downstream predictive power when aggregated into player- and team-level performance indicators. Using BenchBomb, we systematically analyze AV design choices across four dimensions: valuation framework, supervision design, game-state representation, and model architecture. Our findings show that goal-based supervision outperforms denser proxy outcomes, intermediate credit-assignment horizons provide the best balance for value propagation, and player positional information improves state-value estimation. Based on these findings, we introduce VAST, Valuation of Actions through Systematic Spatio-Temporal design, which combines the empirically supported design choices into a unified AV approach. VAST achieves the strongest downstream performance on BenchBomb, outperforming established methods including xThreat, VAEP, and Atomic-VAEP. Compared with the strongest existing baseline, VAST improves performance on the downstream metrics, reducing Team 1X2 NLL from 1.0081 to 0.9992 and Player 1X2 NLL from 1.0021 to 0.9969. We will publicly release the benchmark code, evaluation pipeline, and VAST implementation upon acceptance.</i>
    </div>
  </div>
</div>
