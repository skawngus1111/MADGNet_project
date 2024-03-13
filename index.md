---
layout: project_page
permalink: /

title: Modality-agnostic Domain Generalizable Medical Image Segmentation by Multi-Frequency in Multi-Scale Attention
authors:
    Ju-Hyeon Nam<sup>1</sup>, Nur Suriza Syazwany<sup>1</sup>, Su Jung Kim<sup>1</sup>, Sang-Chul Lee<sup>1,2</sup>
affiliations:
    Department of Electrical and Computer Engineering, Inha University<sup>1</sup>
    DeepCardio<sup>2</sup>
paper (To be released): https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
video (To be released): https://www.youtube.com/results?search_query=turing+machine
code (To be released): https://github.com/topics/turing-machines
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
we propose a novel attention mechanism called Multi-Frequency in Multi-Scale Attention (MFMSA) block. This block employs multi-frequency channel attention (MFCA) with 2D Discrete Cosine Transform (2D DCT) to produce a channel attention map by extracting frequency statistics. Subsequently, multi-scale spatial attention (MSSA) is applied to extract discriminative boundary features and aggregate them from each scale.

## Objective
Turing's main objective in this paper was to investigate the notion of computability and its relation to the Entscheidungsproblem (the decision problem), which is concerned with determining whether a given mathematical statement is provable or not.


## Key Ideas
1. Turing first presented the concept of a "computable number," which refers to a number that can be computed by an algorithm or a definite step-by-step process.
2. He introduced the notion of a Turing machine, an abstract computational device consisting of an infinite tape divided into cells and a read-write head. The machine can read and write symbols on the tape, move the head left or right, and transition between states based on a set of rules.
3. Turing demonstrated that the set of computable numbers is enumerable, meaning it can be listed in a systematic way, even though it is not necessarily countable.
4. He proved the existence of non-computable numbers, which cannot be computed by any Turing machine.
5. Turing showed that the Entscheidungsproblem is undecidable, meaning there is no algorithm that can determine, for any given mathematical statement, whether it is provable or not.

![Turing Machine](/static/image/Turing_machine.png)

*Figure 1: A representation of a Turing Machine. Source: [Wiki](https://en.wikipedia.org/wiki/Turing_machine).*

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
