---
layout: project_page
permalink: /

title: Modality-agnostic Domain Generalizable Medical Image Segmentation by Multi-Frequency in Multi-Scale Attention
authors:
    Ju-Hyeon Nam<sup>1</sup>, Nur Suriza Syazwany<sup>1</sup>, Su Jung Kim<sup>1</sup>, Sang-Chul Lee<sup>1,2</sup>
affiliations:
    Department of Electrical and Computer Engineering, Inha University<sup>1</sup>
    DeepCardio<sup>2</sup>
paper:
video:
code:
---

<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
Generalizability in deep neural networks plays a pivotal role in medical image segmentation. However, deep learning-based medical image analyses tend to overlook the importance of frequency variance, which is critical element for achieving a model that is both modality-agnostic and domain-generalizable.  Additionally, various models fail to account for the potential information loss that can arise from multi-task learning under deep supervision, a factor that can impair the model’s representation ability. To address these challenges, we propose a Modality-agnostic Domain Generalizable Network (MADGNet) for medical image segmentation, which comprises two key components: a Multi-Frequency in Multi-Scale Attention (MFMSA) block and Ensemble Sub-Decoding Module (E-SDM). The MFMSA block refines the process of spatial feature extraction, particularly in capturing boundary features, by incorporating multi-frequency and multi-scale features, thereby offering informative cues for tissue outline and anatomical structures. Moreover, we propose E-SDM to mitigate information loss in multi-task learning with deep supervision, especially during substantial upsampling from low resolution. We evaluate the segmentation performance of MADGNet across six modalities and fifteen datasets. Through extensive experiments, we demonstrate that MADGNet consistently outperforms  state-of-the-art models across various modalities, showcasing superior segmentation performance.  This affirms MADGNet as a robust solution for medical image segmentation that excels in diverse imaging scenarios.
        </div>
    </div>
</div>

## Method Overview
we propose a novel attention mechanism called Multi-Frequency in Multi-Scale Attention (MFMSA) block. This block employs multi-frequency channel attention (MFCA) with 2D Discrete Cosine Transform (2D DCT) to produce a channel attention map by extracting frequency statistics. Subsequently, multi-scale spatial attention (MSSA) is applied to extract discriminative boundary features and aggregate them from each scale. Additionally, we introduce a Ensemble Sub-Decoding Module (E-SDM) to prevent information loss caused by drastic upsampling during multi-task learning with deep supervision. The resulting model, MADGNet, which mainly comprises the MFMSA block and E-SDM, achieved the highest segmentation performance in various modalities and clinical settings.

![MADGNet](/static/image/MADGNet.png)

*Figure 1:  (Left) The overall architecture of the proposed MADGNet mainly comprises MFMSA block and E-SDM. (Right) MFMSA block contains $S$ scale branches ($S = 3$ in this figure) where the $s$-th branch input feature map are downsampled into $\eta^{s - 1}$ ($\eta = \frac{1}{2}$ in this figure). As our MFMSA block considers two dimensions (scale and frequency), MADGNet achieves the highest performance in various modalities and other clinical settings. Additionally, since E-SDM predicts a core task from sub-tasks, the final output is more accurate than when processed parallelly.*

![Ensemble](/static/image/Ensemble.png)

*Figure 2:  Comparison of multi-task learning method between (Left) parallel and (Right) ensemble manners.*

## Table: Comparison of Computable and Non-Computable Numbers

| Computable Numbers | Non-Computable Numbers |
|-------------------|-----------------------|
| Rational numbers, e.g., 1/2, 3/4 | Transcendental numbers, e.g., π, e |
| Algebraic numbers, e.g., √2, ∛3 | Non-algebraic numbers, e.g., √2 + √3 |
| Numbers with finite decimal representations | Numbers with infinite, non-repeating decimal representations |

He used the concept of a universal Turing machine to prove that the set of computable functions is recursively enumerable, meaning it can be listed by an algorithm.

## Significance
Turing's paper laid the foundation for the theory of computation and had a profound impact on the development of computer science. The Turing machine became a fundamental concept in theoretical computer science, serving as a theoretical model for studying the limits and capabilities of computation. Turing's work also influenced the development of programming languages, algorithms, and the design of modern computers.

## Citation
```
@article{turing1936computable,
  title={On computable numbers, with an application to the Entscheidungsproblem},
  author={Turing, Alan Mathison},
  journal={Journal of Mathematics},
  volume={58},
  number={345-363},
  pages={5},
  year={1936}
}
```
