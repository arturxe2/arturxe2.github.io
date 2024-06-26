---
permalink: /projects/ASTRA/
author_profile: true
---

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<div class="post">
                <header class="project-title" style="text-align: center; margin-top: 2em">
                    <h1 class="project-title" style="font-weight: bold; color: #404040">ASTRA: An Action Spotting TRAnsformer for Soccer Videos</h1>
                    <p class="project-venue" style="font-size: 1.0em;">ACM Workshop on Multimedia Content Analysis in Sports, 2023 </p>
                    <h3>
                        <a href="https://scholar.google.es/citations?user=MNdw5eYAAAAJ&hl=ca&amp;hl=en" rel="external nofollow noopener" target="_blank">Artur Xarles</a>
                        , <a href="https://scholar.google.com/citations?user=oI6AIkMAAAAJ&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Sergio Escalera</a>
                        , <a href="https://scholar.google.es/citations?user=XmkDts4AAAAJ&hl=ca&oi=ao&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Thomas B. Moeslund</a>
                        , and <a href="https://scholar.google.es/citations?user=n4BtpPsAAAAJ&hl=ca&oi=ao&amp;hl=en&amp;oi=ao" rel="external nofollow noopener" target="_blank">Albert Clapés</a>
                    </h3>
                    <h5>University of Barcelona, Computer Vision Center, and Aalborg University</h5>
                    <div class="publications project-links">
                        <a href="https://arxiv.org/abs/2404.01891" class="btn" role="button" rel="external nofollow noopener" target="_blank">arXiv</a>
                        <a href="https://github.com/arturxe2/ASTRA" class="btn" role="button" rel="external nofollow noopener" target="_blank">Code</a>
                    </div>
                </header>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="abstract" style="text-align: justify;">
                        <h3 style="text-align: center;">Abstract</h3>
                        <i>In this paper, we introduce ASTRA, a Transformer-based model designed for the task of Action Spotting in soccer matches. ASTRA addresses several challenges inherent in the task and dataset, including the requirement for precise action localization, the presence of a long-tail data distribution, non-visibility in certain actions, and inherent label noise. To do so, ASTRA incorporates (a) a Transformer encoder-decoder architecture to achieve the desired output temporal resolution and to produce precise predictions, (b) a balanced mixup strategy to handle the long-tail distribution of the data, (c) an uncertainty-aware displacement head to capture the label variability, and (d) input audio signal to enhance detection of non-visible actions. Results demonstrate the effectiveness of ASTRA, achieving a tight Average-mAP of 66.82 on the test set. Moreover, in the SoccerNet 2023 Action Spotting challenge, we secure the 3rd position with an Average-mAP of 70.21 on the challenge set. </i>
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
                            <img src="/images/nonvisible.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="ASTRA" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                        </picture>
                    </figure>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="abstract" style="text-align: justify;">
                        <h3 style="text-align: center;">Architecture</h3>
                        Our solution, ASTRA, leverages embeddings \( \mathcal{E} \) from multiple modalities to achieve its goals. Specifically, ASTRA is built upon \( | \mathcal{E} | - 1 \) pre-computed visual embeddings, complemented by an additional audio embedding derived from the log-mel spectrogram of the audio using a VGG-inspired backbone. The network responsible for generating this audio embedding is jointly trained with the ASTRA model. The embeddings are input to the model in clips spanning a duration of \( T \) seconds.

                        These features from each backbone are processed in parallel streams, where Point-wise Feed-Forward Networks (PFFN) project them to a common dimension \( d \). The projected embeddings are then combined in the subsequent Transformer encoder-decoder module, with learnable queries in the decoder. Inspired by the architecture proposed in DETR, this module enables ASTRA to handle different input and output temporal dimensions \( L_{\text{in}} \) and \( L_{\text{out}} \), respectively, and facilitates a straightforward fusion of multiple embeddings.

                        To enhance ASTRA's ability to capture fine-grained details, we introduce a temporally hierarchical architecture for the Transformer encoder. This architecture enables the encoder to attend to more local information in the initial layers and reduces the computational cost. Finally, ASTRA employs two prediction heads to generate classification and displacement predictions for the anchors introduced by Soares et al. These anchors correspond to specific temporal positions and class actions, as described in their work. Additionally, we adopt their suggestion of employing a radius for both classification and displacement \( r_{c} \) and \( r_{d} \), respectively, to define the temporal range around a ground-truth action within which it can be detected.

                        Furthermore, to account for label uncertainty, ASTRA adapts the prediction head responsible for displacement by modeling them as Gaussian distributions instead of deterministic temporal positions. This allows ASTRA to capture temporal location uncertainty and provide a more comprehensive representation of the actions. Additionally, ASTRA incorporates a balanced mixup technique to improve model generalization and accommodate the long-tail distribution of the data.
                    </div>
                </div>
                <div style="margin-top:20px">
                    <figure>
                        <picture>
                            <img src="/images/ASTRA_diagram.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="Nonvisible" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
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
            </div>