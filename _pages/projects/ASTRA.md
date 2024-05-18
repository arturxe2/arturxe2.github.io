---
permalink: /projects/ASTRA
title: "ASTRA: An Action Spotting TRAnsformer for Soccer Videos"
author_profile: true
---

<div class="post">
                <header class="project-title" style="text-align: center; margin-top: 2em">
                    <h1 class="project-title" style="font-weight: bold; color: #404040">ASTRA: An Action Spotting TRAnsformer for Soccer Videos</h1>
                    <p class="project-venue" style="font-size: 2.5em;">ACM Workshop on Multimedia Content Analysis in Sports, 2023 </p>
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
                <div style="margin-top:20px">
                    <figure>
                        <picture>
                            <img src="/images/ASTRA_diagram.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="ASTRA" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                        </picture>
                    </figure>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="abstract" style="text-align: justify;">
                        <h3 style="text-align: center;">Abstract</h3>
                        <i>In this paper, we introduce ASTRA, a Transformer-based model designed for the task of Action Spotting in soccer matches. ASTRA addresses several challenges inherent in the task and dataset, including the requirement for precise action localization, the presence of a long-tail data distribution, non-visibility in certain actions, and inherent label noise. To do so, ASTRA incorporates (a) a Transformer encoder-decoder architecture to achieve the desired output temporal resolution and to produce precise predictions, (b) a balanced mixup strategy to handle the long-tail distribution of the data, (c) an uncertainty-aware displacement head to capture the label variability, and (d) input audio signal to enhance detection of non-visible actions. Results demonstrate the effectiveness of ASTRA, achieving a tight Average-mAP of 66.82 on the test set. Moreover, in the SoccerNet 2023 Action Spotting challenge, we secure the 3rd position with an Average-mAP of 70.21 on the challenge set. </i>
                    </div>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="motivations" style="text-align: justify;">
                        <h3 style="text-align: center;">Motivation</h3>
                    </div>
                </div>
                <div id="accordion" style="margin-top:20px">
                    <div class="card">
                        <div class="card-header" id="headingOne" style="text-align: center; padding:0px;">
                            <button class="btn btn-link dropdown-toggle" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne" style="font-size: 16px">Motion consistency as a plausibility requirement </button>
                        </div>
                        <div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
                            <div class="card-body">
                                <div class="row">
                                    <div class="col-5">
                                        <figure>
                                            <picture>
                                                <img src="/assets/img/belfusion/motion_metric.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="Motion" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                                            </picture>
                                        </figure>
                                    </div>
                                    <div class="col-7" style="text-align: justify;">
                                        Most prior stochastic works focus on predicting a highly diverse distribution of motions. Such diversity has been traditionally defined and evaluated in the coordinate space. This definition biases research toward models that generate <b>fast and motion-divergent motions</b>
                                        (see Fig. in the left). Although there are scenarios where predicting low-speed diverse motion is important, this is discouraged by prior techniques. For example, in assistive robotics, anticipating behaviors (i.e., actions) like whether the interlocutor is about to shake your hand or scratch their head might be crucial for preparing the robot’s actuators on time. In a surveillance scenario, a foreseen noxious behavior might not differ much from a well-meaning one when considering only the poses along the motion sequence. We argue that this behavioral perspective is paramount to build next-generation stochastic HMP models. <br>
                                        <br>
                                        BeLFusion, by building a latent space where behavior is disentangled from poses and motion, detaches <b>diversity</b>
                                        from the traditional coordinate-based perspective and <b>promotes it from a behavioral viewpoint</b>
                                        . 
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-header" id="headingTwo" style="text-align: center; padding:0px">
                            <button class="btn btn-link collapsed dropdown-toggle" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo" style="font-size: 16px">Contextual coherence as a realism driver </button>
                        </div>
                        <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordion">
                            <div class="card-body">
                                <figure>
                                    <picture>
                                        <img src="/assets/img/belfusion/samples_superimposed.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="APDE" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                                    </picture>
                                </figure>
                                <div style="margin-bottom: 20px">
                                    Results from prior diversity-centric works often suffer from a tradeoff that has been persistently overlooked: <b>predicted motion looks unnatural when observed following the motion of the immediate past</b>
                                    . The strong diversity regularization techniques employed often produce abrupt speed changes or direction discontinuities. We argue that consistency with the immediate past is a requirement for prediction plausibility. <br>
                                    <br>
                                    Figure below shows the evolution of 10 superimposed predictions along time in two actions from H36M (sitting down, and giving directions), and two datasets from AMASS (DanceDB, and GRAB). First, the acceleration of GSPS and DivSamp at the beginning of the prediction leads to extreme poses very fast, abruptly transitioning from the observed motion. Second, <b>it shows the capacity of BeLFusion to adapt the diversity predicted to the context.</b>
                                    For example, the diversity of motion predicted while giving directions focuses on the upper body, and does not include holistic extreme poses. Interestingly, when just sitting, the predictions include a wider range of full-body movements like laying down, or bending over. A similar context fitting is observed in the AMASS cross-dataset scenario. For instance, BeLFusion correctly identifies that the diversity must target the upper body in the GRAB dataset, or the arms while doing a dance step. 
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="architecture" style="text-align: justify;">
                        <h3 style="text-align: center;">Architecture</h3>
                    </div>
                </div>
                <div style="margin-top:20px">
                    <figure>
                        <picture>
                            <img src="/assets/img/belfusion/arch.png" class="figure-padding img-fluid rounded z-depth-1" width="100%" height="auto" title="BeLFusion" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">
                        </picture>
                    </figure>
                </div>
                <p>A latent diffusion model conditioned on an encoding \(x=c\) of the observation, \(\mathbf{X}\), progressively denoises a sample from a zero-mean unit variance multivariate normal distribution into a behavior code. Then, the behavior coupler \(\mathcal{B}_{\phi}\) decodes the prediction by transferring the sampled behavior to the target motion, \(\mathbf{x}_{m}\). In our implementation, \(f_{\Phi}\) is a conditional U-Net with cross-attention, and \(h_{\lambda}\), \(g_{\alpha}\), and \(\mathcal{B}_{\phi}\) are one-layer recurrent neural networks.</p>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="architecture" style="text-align: justify;">
                        <h3 style="text-align: center;">Implicit diversity loss</h3>
                    </div>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top:5px">$$\underset{k}{\min}\; \mathcal{L}_{lat}(\mathbf{X}, \mathbf{Y}_{e}^k) + \lambda \; \underset{k}{\min}\; \mathcal{L}_{rec}(\mathbf{X}, \mathbf{Y}_{e}^k)$$ </div>
                <div class="d-flex align-items-center justify-content-center">
                    Regularization relaxation value: 
                    <b>
                        <span style="margin-left:10px; font-size: 1.2em;" id="k_range_val">k=1</span>
                    </b>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top:20px">
                    <input type="range" class="form-range" min="0" max="7" step="1" value="0" id="k_range" style="width: 50%">
                </div>
                <div class="card" style="margin-top:20px">
                    <div style="flex-direction: column; justify-content: center; display: inline-flex; align-items: center; margin:10px">
                        <h5 style="max-width:100%; margin-bottom:10px">Human3.6M</h5>
                        <img id="k-h36m" src="/assets/img/belfusion/k_analysis/k_h36m_0.png" width="100%">
                    </div>
                    <div style="margin-top:30px; flex-direction: column; justify-content: center; display: inline-flex; align-items: center; margin:10px">
                        <h5 style="max-width:100%; margin-bottom:10px">AMASS</h5>
                        <img id="k-amass" src="/assets/img/belfusion/k_analysis/k_amass_0.png" width="86%">
                    </div>
                    <p style="margin:10px">
                        Regularization relaxation usually leads to out-of-distribution predictions. This is often solved by employing additional complex techniques like pose priors, or bone-length losses that regularize the other predictions. BeLFusion can dispense with it due to mainly two reasons: 1) Denoising diffusion models are capable of faithfully capturing a greater breadth of the training distribution than GANs or VAEs; 2) The variational training of the behavior coupler makes it more robust to errors in the predicted behavior code. <br>
                        <br>
                        In general, increasing k enhances the samples' diversity, accuracy, and realism. For k &lt;5, going through the whole chain of denoising steps boosts accuracy. However, for <b>k &gt;5</b>
                        , further denoising only boosts diversity- and realism-wise metrics (APD, CMD, FID), and <b>makes the fast single-step inference extremely accurate</b>
                        .
                    </p>
                </div>
                <div style="max-width: site.max_project_width; margin-top:50px; padding: 0px !important">
                    <h3 style="text-align: center; margin-bottom:20px">
                        Examples <i>in motion</i>
                    </h3>
                    <div class="d-flex justify-content-center" id="list-tab" role="tablist">
                        <div class="list-group list-group-horizontal" style="display: flex; max-width: 600px;">
                            <a class="list-group-item list-group-item-action active" id="h36m-list" data-toggle="list" href="#h36m" role="tab" aria-controls="h36m" style="flex: 1; text-align: center;">Human3.6M</a>
                            <a class="list-group-item list-group-item-action" id="amass-list" data-toggle="list" href="#amass" role="tab" aria-controls="amass" style="flex: 1; text-align: center;">AMASS</a>
                        </div>
                    </div>
                    <div class="tab-content figure" id="nav-tabContent" style="padding: 0px !important">
                        <div class="tab-pane fade show active" id="h36m" role="tabpanel" aria-labelledby="h36m-list" style="padding: 0px !important">
                            <div class="d-flex align-items-center justify-content-center">
                                <div class="dropdown list-group">
                                    <button class="btn dropdown-toggle" style="max-width:600px" type="button" id="h36m-btn" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                        <span class="selection">H_4_Sitting</span>
                                    </button>
                                    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton" id="list-tab" role="tablist">
                                        <a class="dropdown-item dropdown-item-action" href="#H_4_Sitting" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_4_Sitting">H_4_Sitting</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_148_WalkDog" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_148_WalkDog">H_148_WalkDog</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_402_Smoking" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_402_Smoking">H_402_Smoking</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_446_Smoking" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_446_Smoking">H_446_Smoking</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_541_Phoning" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_541_Phoning">H_541_Phoning</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_608_Walking" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_608_Walking">H_608_Walking</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_861_SittingDown" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_861_SittingDown">H_861_SittingDown</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_910_SittingDown" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_910_SittingDown">H_910_SittingDown</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_962_WalkTogether" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_962_WalkTogether">H_962_WalkTogether</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_1928_Eating" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_1928_Eating">H_1928_Eating</a>
                                        <a class="dropdown-item dropdown-item-action" href="#H_2103_Photo" id="h36m-dropdown" data-toggle="list" role="tab" aria-controls="H_2103_Photo">H_2103_Photo</a>
                                    </div>
                                </div>
                            </div>
                            <div class="card" style="padding: 10px !important; margin-top:10px">
                                <div class="tab-content figure" id="nav-tabContent">
                                    <div class="tab-pane fade show active gif" id="H_4_Sitting" role="tabpanel">
                                        <img class="gif" src="/assets/img/belfusion/hmp_videos/H_4_Sitting.gif">Whereas for ‘H_4_Sitting’ BeLFusion’s predicted motions showcase a high variety of arms-related actions, its predictions for sequences where the arms are used in an ongoing action (‘H_402_Smoking’, ‘H_446_Smoking’, and ‘H_541_Phoning’) have a more limited variety of arms motion.
                                    </div>
                                    <div class="tab-pane fade" id="H_148_WalkDog" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_148_WalkDog.gif">None of the models is able to model the high-speed walking movement from the ground truth.
                                    </div>
                                    <div class="tab-pane fade" id="H_402_Smoking" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_402_Smoking.gif">BeLFusion's predictions for sequences where the arms are used in an ongoing action (‘H_402_Smoking’, ‘H_446_Smoking’, and ‘H_541_Phoning’) have a more limited variety of arms motion.
                                    </div>
                                    <div class="tab-pane fade" id="H_446_Smoking" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_446_Smoking.gif">BeLFusion's predictions for sequences where the arms are used in an ongoing action (‘H_402_Smoking’, ‘H_446_Smoking’, and ‘H_541_Phoning’) have a more limited variety of arms motion.
                                    </div>
                                    <div class="tab-pane fade" id="H_541_Phoning" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_541_Phoning.gif">BeLFusion's predictions for sequences where the arms are used in an ongoing action (‘H_402_Smoking’, ‘H_446_Smoking’, and ‘H_541_Phoning’) have a more limited variety of arms motion.
                                    </div>
                                    <div class="tab-pane fade" id="H_608_Walking" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_608_Walking.gif">When the observation shows an ongoing fast motion, BeLFusion is the only model that consistently generates a coherent transition between the observation and the predicted behavior. Other methods mostly predict a sudden stop of the previous action.
                                    </div>
                                    <div class="tab-pane fade" id="H_861_SittingDown" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_861_SittingDown.gif">In general, BeLFusion provides good coverage of all plausible futures given the contextual setting. In this example, our model’s predictions contain as many different actions as all other methods, with no realism trade-off as for GSPS or DivSamp.
                                    </div>
                                    <div class="tab-pane fade" id="H_910_SittingDown" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_910_SittingDown.gif">In general, BeLFusion provides good coverage of all plausible futures given the contextual setting. In this example, our model’s predictions contain as many different actions as all other methods, with no realism trade-off as for GSPS or DivSamp.
                                    </div>
                                    <div class="tab-pane fade" id="H_962_WalkTogether" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_962_WalkTogether.gif">Our method predicts motions that are compatible with the ongoing action of walking next to someone, whereas other methods ignore such possibility.
                                    </div>
                                    <div class="tab-pane fade" id="H_1928_Eating" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_1928_Eating.gif">When the observation shows an ongoing fast motion, BeLFusion is the only model that consistently generates a coherent transition between the observation and the predicted behavior. Other methods mostly predict a sudden stop of the previous action.
                                    </div>
                                    <div class="tab-pane fade" id="H_2103_Photo" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/H_2103_Photo.gif">When the observation shows an ongoing fast motion, BeLFusion is the only model that consistently generates a coherent transition between the observation and the predicted behavior. Other methods mostly predict a sudden stop of the previous action.
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="tab-pane fade" id="amass" role="tabpanel" aria-labelledby="amass-list" style="padding: 0px !important">
                            <div class="d-flex align-items-center justify-content-center">
                                <div class="dropdown list-group">
                                    <button class="btn dropdown-toggle" style="max-width:600px" type="button" id="amass-btn" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                        <span class="selection">A_103_Transitions</span>
                                    </button>
                                    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton" id="list-tab" role="tablist">
                                        <a class="dropdown-item dropdown-item-action" href="#A_103_Transitions" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_103_Transitions">A_103_Transitions</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_1087_DanceDB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_1087_DanceDB">A_1087_DanceDB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_1402_DanceDB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_1402_DanceDB">A_1402_DanceDB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_1899_DanceDB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_1899_DanceDB">A_1899_DanceDB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_2054_DanceDB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_2054_DanceDB">A_2054_DanceDB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_2284_DanceDB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_2284_DanceDB">A_2284_DanceDB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_2545_DanceDB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_2545_DanceDB">A_2545_DanceDB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_7750_GRAB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_7750_GRAB">A_7750_GRAB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_7667_GRAB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_7667_GRAB">A_7667_GRAB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_9274_GRAB" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_9274_GRAB">A_9274_GRAB</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_10929_HUMAN4D" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_10929_HUMAN4D">A_10929_HUMAN4D</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_11074_HUMAN4D" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_11074_HUMAN4D">A_11074_HUMAN4D</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_12321_SOMA" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_12321_SOMA">A_12321_SOMA</a>
                                        <a class="dropdown-item dropdown-item-action" href="#A_12391_SOMA" id="amass-dropdown" data-toggle="list" role="tab" aria-controls="A_12391_SOMA">A_12391_SOMA</a>
                                    </div>
                                </div>
                            </div>
                            <div class="card" style="padding: 10px !important; margin-top:10px">
                                <div class="tab-content figure" id="nav-tabContent">
                                    <div class="tab-pane fade show active" id="A_103_Transitions" role="tabpanel">
                                        <img class="gif" src="/assets/img/belfusion/hmp_videos/A_103_Transitions.gif">Although the observation window of this sequence clearly showcases a fast rotational dancing step, none of the state-of-theart methods are able to generate a plausible continuation of the observed motion, and all of their predictions abruptly stop rotating. BeLFusion is the only method that generates predictions that slowly decrease its rotational momentum to start performing a different action. 
                                    </div>
                                    <div class="tab-pane fade" id="A_1087_DanceDB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_1087_DanceDB.gif">Similarly to the other state-of-the-art methods, BeLFusion also struggles with modeling high-frequencies.
                                    </div>
                                    <div class="tab-pane fade" id="A_1402_DanceDB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_1402_DanceDB.gif">The first-seen handstand behavior in the observation leads to BeLFusion generating several wrong movement continuations. The fast legs motion during the observation is not reflected in any prediction, although BeLFusion slightly shows it in samples #4 and #7.
                                    </div>
                                    <div class="tab-pane fade" id="A_1899_DanceDB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_1899_DanceDB.gif">BeLFusion is able to detect that the dance moves involve keeping the arms arising while moving or rotating. In comparison, DLow, GSPS, and DivSamp simply predict other unrelated movements. TPK is only able to predict a few samples with fairly good continuations to the dance step.
                                    </div>
                                    <div class="tab-pane fade" id="A_2054_DanceDB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_2054_DanceDB.gif">BeLFusion can predict, up to some extent, the correct continuation of a dance move, while other methods either almost freeze or simply predict an out-of-context movement.
                                    </div>
                                    <div class="tab-pane fade" id="A_2284_DanceDB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_2284_DanceDB.gif">BeLFusion is able to detect that the dance moves involve keeping the arms arising while moving or rotating. In comparison, DLow, GSPS, and DivSamp simply predict other unrelated movements. TPK is only able to predict a few samples with fairly good continuations to the dance step.
                                    </div>
                                    <div class="tab-pane fade" id="A_2545_DanceDB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_2545_DanceDB.gif">BeLFusion is the only method that generates predictions that slowly decrease its motion momentum to start performing a different action.
                                    </div>
                                    <div class="tab-pane fade" id="A_7667_GRAB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_7667_GRAB.gif">BeLFusion adapts the diversity of predictions to the ‘grabbing’ action present in the GRAB dataset. While other methods predict coordinate-wise diverse inaccurate predictions, our model encourages diversity within the short spectrum of the plausible behaviors that can follow.
                                    </div>
                                    <div class="tab-pane fade" id="A_7750_GRAB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_7750_GRAB.gif">BeLFusion adapts the diversity of predictions to the ‘grabbing’ action present in the GRAB dataset. While other methods predict coordinate-wise diverse inaccurate predictions, our model encourages diversity within the short spectrum of the plausible behaviors that can follow.
                                    </div>
                                    <div class="tab-pane fade" id="A_9274_GRAB" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_9274_GRAB.gif">BeLFusion adapts the diversity of predictions to the ‘grabbing’ action present in the GRAB dataset. While other methods predict coordinate-wise diverse inaccurate predictions, our model encourages diversity within the short spectrum of the plausible behaviors that can follow.
                                    </div>
                                    <div class="tab-pane fade" id="A_10929_HUMAN4D" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_10929_HUMAN4D.gif">BeLFusion is the only method that generates predictions that slowly decrease its motion momentum to start performing a different action.
                                    </div>
                                    <div class="tab-pane fade" id="A_11074_HUMAN4D" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_11074_HUMAN4D.gif">BeLFusion is the only able to anticipate the intention of laying down by detecting subtle cues inside the observation window (samples #6 and #8).
                                    </div>
                                    <div class="tab-pane fade" id="A_12321_SOMA" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_12321_SOMA.gif">BeLFusion is the only able to anticipate the intention of laying down by detecting subtle cues inside the observation window (samples #6 and #8).
                                    </div>
                                    <div class="tab-pane fade" id="A_12391_SOMA" role="tabpanel">
                                        <img class="gif lazy" src="/assets/img/belfusion/placeholder_comparison.png" data-src="/assets/img/belfusion/hmp_videos/A_12391_SOMA.gif">BeLFusion is the only method able to infer how a very challenging repetitive stretching movement will follow.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="others" style="text-align: justify;">
                        <h3 style="text-align: center;">Others</h3>
                    </div>
                </div>
                <div id="accordion" style="margin-top:20px">
                    <div class="card">
                        <div class="card-header" id="headingOne" style="text-align: center; padding:0px;">
                            <button id="collapse-behavior" class="btn btn-link dropdown-toggle" data-toggle="collapse" data-target="#collapse-behavior-content" aria-expanded="true" aria-controls="collapseOne" style="font-size: 16px">Examples of behavioral transference to ongoing motions </button>
                        </div>
                        <div id="collapse-behavior-content" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
                            <div style="margin-top:10px; padding: 0px !important">
                                <div class="d-flex justify-content-center" id="list-tab" role="tablist">
                                    <div class="list-group list-group-horizontal" style="max-width: 600px; display: flex;">
                                        <a class="list-group-item list-group-item-action active" id="h36m_b-list" data-toggle="list" href="#h36m_b" role="tab" aria-controls="h36m_b" style="flex: 1; text-align: center;">Human3.6M</a>
                                        <a class="list-group-item list-group-item-action" id="amass_b-list" data-toggle="list" href="#amass_b" role="tab" aria-controls="amass_b" style="flex: 1; text-align: center;">AMASS</a>
                                    </div>
                                </div>
                                <div class="col-12 tab-content figure" id="nav-tabContent" style="margin-top:20px">
                                    <div class="tab-pane fade show active" id="h36m_b" role="tabpanel" aria-labelledby="h36m_b-list">
                                        <div class="row align-items-center justify-content-center">
                                            <b>H1</b>
                                            <img class="gif90 lazy" src="/assets/img/belfusion/placeholder_transfer.png" style="margin-left:20px" data-src="/assets/img/belfusion/bt_videos/H1.gif">
                                        </div>
                                        <div class="row align-items-center justify-content-center">
                                            <b>H2</b>
                                            <img class="gif90 lazy" src="/assets/img/belfusion/placeholder_transfer.png" style="margin-left:20px" data-src="/assets/img/belfusion/bt_videos/H2.gif">
                                        </div>
                                        <div class="row align-items-center justify-content-center">
                                            <b>H3</b>
                                            <img class="gif90 lazy" src="/assets/img/belfusion/placeholder_transfer.png" style="margin-left:20px" data-src="/assets/img/belfusion/bt_videos/H3.gif">
                                        </div>
                                        <p style="margin-top: 10px; margin-bottom: 10px">
                                            The motion tagged as <b>behavior shows the target behavior to be encoded and transferred</b>
                                            . All the other columns show the ongoing motions where the behavior will be transferred to. They are shown with blue and orange skeletons. <b>Once the behavior is transferred, the color of the skeletons switches to green and pink.</b>
                                            <br>
                                            <br>In ‘H1’ (H36M), the walking action or behavior is transferred to the target ongoing motions. For ongoing motions where the person is standing, they start walking towards the direction they are facing (#1, #2, #4, #5). Such transition is smooth and coherent with the observation. For example, the person making a phone call in #7 keeps the arm next to the ear while starting to walk. When sitting or bending down, the movement of the legs is either very little (#3 and #6), or very limited (#8). ‘H2’ and ‘H3’ show the transference of subtle and long-range behaviors, respectively.
                                        </p>
                                    </div>
                                    <div class="tab-pane fade show" id="amass_b" role="tabpanel" aria-labelledby="amass_b-list">
                                        <div class="row align-items-center justify-content-center">
                                            <b>A1</b>
                                            <img class="gif90 lazy" src="/assets/img/belfusion/placeholder_transfer.png" style="margin-left:20px" data-src="/assets/img/belfusion/bt_videos/A1.gif">
                                        </div>
                                        <div class="row align-items-center justify-content-center">
                                            <b>A2</b>
                                            <img class="gif90 lazy" src="/assets/img/belfusion/placeholder_transfer.png" style="margin-left:20px" data-src="/assets/img/belfusion/bt_videos/A2.gif">
                                        </div>
                                        <div class="row align-items-center justify-content-center">
                                            <b>A3</b>
                                            <img class="gif90 lazy" src="/assets/img/belfusion/placeholder_transfer.png" style="margin-left:20px" data-src="/assets/img/belfusion/bt_videos/A3.gif">
                                        </div>
                                        <p style="margin-top: 10px; margin-bottom: 10px">
                                            The motion tagged as <b>behavior shows the target behavior to be encoded and transferred</b>
                                            . All the other columns show the ongoing motions where the behavior will be transferred to. They are shown with blue and orange skeletons. <b>Once the behavior is transferred, the color of the skeletons switches to green and pink.</b>
                                            <br>
                                            <br>For AMASS (cross-dataset scenario), the behavioral encoding faces a huge domain drift. However, we still observe good results at this task. For example, ‘A1’ shows how a stretching movement is successfully transferred to very distinct ongoing motions by generating smooth and realistic transitions. Similarly, ‘A2’ and ‘A3’ are examples of transferring subtle and aggressive behaviors, respectively. Even though the dancing behavior in ‘A3’ was not seen at training time, it is transferred and adapted to the ongoing motion fairly realistically.
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="d-flex align-items-center justify-content-center" style="margin-top: 30px">
                    <div class="project-narrow" id="bibtex" style="text-align: justify;">
                        <h3 style="text-align: center;">BibTeX</h3>
                        <div class="bibtex">
                            <figure class="highlight">
                                <pre>
                                    <code class="language-bibtex" data-lang="bibtex">
                                        <span class="nc">@inproceedings</span>
                                        <span class="p">{</span>
                                        <span class="nl">barquero2023belfusion</span>
                                        <span class="p">,</span>
                                        <span class="na">title</span>
                                        <span class="p">=</span>
                                        <span class="s">{BeLFusion: Latent Diffusion for Behavior-Driven Human Motion Prediction}</span>
                                        <span class="p">,</span>
                                        <span class="na">author</span>
                                        <span class="p">=</span>
                                        <span class="s">{Barquero, German and Escalera, Sergio and Palmero, Cristina}</span>
                                        <span class="p">,</span>
                                        <span class="na">booktitle</span>
                                        <span class="p">=</span>
                                        <span class="s">{Proceedings of the IEEE/CVF International Conference on Computer Vision}</span>
                                        <span class="p">,</span>
                                        <span class="na">year</span>
                                        <span class="p">=</span>
                                        <span class="s">{2023}</span>
                                        <span class="p">}</span>
                                    </code>
                                </pre>
                            </figure>
                        </div>
                    </div>
                </div>
                <p>
                    <img data-src="/assets/img/belfusion/apde.png" class="lazy">
                </p>
            </div>