---
title: "AdaSpot: Spend Resolution Where It Matters for Precise Event Spotting"
collection: publications
permalink: /publication/2026-06-AdaSpot
excerpt: >-
  <strong>Abstract:</strong> Precise Event Spotting aims to localize fast-paced actions or events in videos with high temporal precision, a key task for applications in sports analytics, robotics, and autonomous systems. Existing methods typically process all frames uniformly, overlooking the inherent spatio-temporal redundancy in video data. This leads to redundant computation on non-informative regions while limiting overall efficiency. To remain tractable, they often spatially downsample inputs, losing fine-grained details crucial for precise localization. To address these limitations, we propose AdaSpot, a simple yet effective framework that processes low-resolution videos to extract global task-relevant features while adaptively selecting the most informative region-of-interest in each frame for high-resolution processing. The selection is performed via an unsupervised, task-aware strategy that maintains spatio-temporal consistency across frames and avoids the training instability of learnable alternatives. This design preserves essential fine-grained visual cues with a marginal computational overhead compared to low-resolution-only baselines, while remaining far more efficient than uniform high-resolution processing. Experiments on standard PES benchmarks demonstrate that AdaSpot achieves state-of-the-art performance under strict evaluation metrics (e.g., +3.96 and +2.26 mAP@0 frames on Tennis and FineDiving), while also maintaining strong results under looser metrics. Code is available at: https://github.com/arturxe2/AdaSpot.
date: 2026-06-01
venue: 'CVPR'
paperurl: 'https://arxiv.org/abs/2602.22073'
codeurl: 'https://github.com/arturxe2/AdaSpot'
pageurl: 'https://arturxe2.github.io/projects/AdaSpot/'
citation: '<u>Xarles, A.</u>, Escalera, S., Moeslund, T. B., & Clapés, A. (2026). AdaSpot: Spend Resolution Where It Matters for Precise Event Spotting. Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 24010-24020.'
---
