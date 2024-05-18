---
permalink: /projects/T-DEED
author_profile: true
---

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<div class="post">
                <header class="project-title" style="text-align: center; margin-top: 2em">
                    <h1 class="project-title" style="font-weight: bold; color: #404040">T-DEED: Temporal-Discriminability Enhancer Encoder-Decoder for Precise Event Spotting in Sports Videos</h1>
                    <p class="project-venue" style="font-size: 1.0em;">CVsports Workshop at CVPR, 2024 </p>
                    <h3>
                        <a href="https://scholar.google.es/citations?user=MNdw5eYAAAAJ&hl=ca&amp;hl=en" rel="external nofollow noopener" target="_blank">Artur Xarles</a>
                        , <a href="https://scholar.google.com/citations?user=oI6AIkMAAAAJ&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Sergio Escalera</a>
                        , <a href="https://scholar.google.es/citations?user=XmkDts4AAAAJ&hl=ca&oi=ao&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Thomas B. Moeslund</a>
                        , and <a href="https://scholar.google.es/citations?user=n4BtpPsAAAAJ&hl=ca&oi=ao&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Albert Clapés</a>
                    </h3>
                    <h5>University of Barcelona, Computer Vision Center, and Aalborg University</h5>
                    <div class="publications project-links">
                        <a href="https://arxiv.org/abs/2404.05392" class="btn" role="button" rel="external nofollow noopener" target="_blank">arXiv</a>
                        <a href="https://github.com/arturxe2/T-DEED" class="btn" role="button" rel="external nofollow noopener" target="_blank">Code</a>
                    </div>
                </header>
                <div style="margin-top:20px">
                    <figure>
                        <picture>
                            <img src="/images/PESTask.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="PEStask" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                        </picture>
                    </figure>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="abstract" style="text-align: justify;">
                        <h3 style="text-align: center;">Abstract</h3>
                        <i>In this paper, we introduce T-DEED, a Temporal-Discriminability Enhancer Encoder-Decoder for Precise Event Spotting in sports videos. T-DEED addresses multiple challenges in the task, including the need for discriminability among frame representations, high output temporal resolution to maintain prediction precision, and the necessity to capture information at different temporal scales to handle events with varying dynamics. It tackles these challenges through its specifically designed architecture, featuring an encoder-decoder for leveraging multiple temporal scales and achieving high output temporal resolution, along with temporal modules designed to increase token discriminability. Leveraging these characteristics, T-DEED achieves SOTA performance on the FigureSkating and FineDiving datasets.</i>
                    </div>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="abstract" style="text-align: justify;">
                        <h3 style="text-align: center;">Motivation</h3>
                        <i>A depth examination of the Action Spotting task within soccer matches revealed four main challenges: (1) the necessity for precise predictions, given the tight tolerances while evaluating the task; (2) a long-tail data distribution, where some of the actions occur infrequently; (3) the presence of noisy labels resulting from the subjective judgment of annotators in determining temporal locations; and (4) the non-visibility of certain actions due to replays or camera angles. ASTRA was designed with dedicated modules tailored to address each of the challenges.</i>
                    </div>
                </div>
                <div style="margin-top:20px">
                    <figure>
                        <picture>
                            <img src="/images/discriminabilityFD.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="ASTRA" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                        </picture>
                    </figure>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="abstract" style="text-align: justify;">
                        <h3 style="text-align: center;">Architecture</h3>
                        <p>
                            Our model, Temporal-Discriminability Enhancer Encoder-Decoder (T-DEED), is designed to increase token discriminability for Precise Event Spotting (PES) while leveraging multiple temporal scales. As illustrated in the Figure, T-DEED comprises three main blocks: a feature extractor, a temporally discriminant encoder-decoder, and a prediction head.
                        </p>
                        <p>
                            We process videos through fixed-length clips, each containing \( L \) densely sampled frames. The feature extractor, composed of a 2D backbone with Gate-Shift-Fuse (GSF) modules, handles the input frames, generating per-frame representations of dimension \( d \), hereby referred to as <i>tokens</i>. These tokens undergo further refinement within the temporally discriminant encoder-decoder. This module employs SGP layers which -- as shown by Shi et al. -- diminish token similarity, thereby boosting discriminability across tokens of the same sequence.
                        </p>
                        <p>
                            The encoder-decoder architecture allows the processing of features across diverse temporal scales, helpful for detecting events requiring different amounts of temporal context. We also integrate skip connections to preserve the fine-grained information from the initial layers. To effectively merge information proceeding from varying temporal scales in the skip connections, we introduce the SGP-Mixer layer, detailed in Section 2. This layer employs the same principles as the SGP layer to enhance token discriminability while gathering information from varying range temporal windows.
                        </p>
                        <p>
                            Finally, the output tokens are directed to the prediction head, resembling those commonly used in Action Spotting (AS) literature. It encompasses a classification component to identify whether an event occurs at the given temporal position or in close proximity (within a radius of \( r_{E} \) frames). Additionally, for the positive classifications, a displacement component pinpoints the exact temporal position of ground truth events.
                        </p>
                    </div>
                </div>
                <div style="margin-top:20px">
                    <figure>
                        <picture>
                            <img src="/images/modelArchitecture.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="Nonvisible" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                        </picture>
                    </figure>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="bibtex" style="text-align: left;">
                        <h3 style="text-align: center;">BibTeX</h3>
                        <div class="bibtex">
                            <i>@inproceedings{xarles2023astra,<br>
                                &emsp;title={ASTRA: An Action Spotting TRAnsformer for Soccer Videos},<br>
                                &emsp;author={Xarles, Artur and Escalera, Sergio and Moeslund, Thomas B and Clap{\'e}s, Albert},<br>
                                &emsp;booktitle={Proceedings of the 6th International Workshop on Multimedia Content Analysis in &emsp;Sports},<br>
                                &emsp;pages={93--102},<br>
                                &emsp;year={2023}<br>
                                }</i>
                        </div>
                    </div>
                </div>
                <p>
                    <img data-src="/assets/img/belfusion/apde.png" class="lazy">
                </p>
            </div>