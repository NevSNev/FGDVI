# FloED: Advanced Video Inpainting Using Optical Flow-Guided Efficient Diffusion

## 📄 [Paper](https://arxiv.org/pdf/2412.00857) | [arXiv](https://arxiv.org/abs/2412.00857)
<div>
    <h4 align="left">
    <a href="https://arxiv.org/abs/2412.00857" target='_blank'>
    <img src="https://img.shields.io/badge/arXiv-2311.15368-b31b1b.svg">
    </a>
    </h4>
</div>


---

## Abstract

Recently, diffusion-based methods have achieved great improvements in the video inpainting task. However, these methods still face many challenges, such as maintaining temporal consistency and the time-consuming issue. This paper proposes an advanced video inpainting framework using optical Flow-guided Efficient Diffusion, called FloED. 

Specifically, FloED employs a dual-branch architecture, where a flow branch first restores corrupted flow and a multi-scale flow adapter provides motion guidance to the main inpainting branch. Additionally, a training-free latent interpolation method is proposed to accelerate the multi-step denoising process using flow warping. Further introducing a flow attention cache mechanism, FloED efficiently reduces the computational cost brought by incorporating optical flow. Comprehensive experiments in both background restoration and object removal tasks demonstrate that FloED outperforms state-of-the-art methods from the perspective of both performance and efficiency.

---

## Method Overview

![Method Overview](static/FloED/Fig_0.jpg)

Our method employs a dual-branch architecture implemented through a two-stage training approach:

1. **Motion Layer Optimization**: We first focus on the upper branch, optimizing the motion layer to adapt specifically to the video inpainting domain.
2. **Flow Branch and Adapter**: We use a dedicated flow branch complemented by a **multi-scale flow adapter**, which provides flow guidance covering upblocks of the primary UNet. During the inference phase, we enhance efficiency by integrating the **flow attention cache**.
3. **Latent Interpolation**: We introduce a **training-free latent interpolation** technique that leverages optical flow to speed up the multi-step denoising process. Complemented by a flow attention cache mechanism, FloED efficiently reduces the additional computational costs introduced by the flow.

![Flow Details](static/FloED/Fig_1.jpg)

---

## Qualitative Comparison on Background Restoration

### Example 1: Water and Ice Scene

<video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Comparison_1.mp4" type="video/mp4">
</video>

*“Water appears to be flowing, the rock is covered in ice.”*

---

## Qualitative Comparison on Object Removal

### Example 2: Staircases Scene

<video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Comparison_2.mp4" type="video/mp4">
</video>

*“A series of staircases, 8K.”*

---

## Comparative Videos

### VideoComposer vs. CoCoCo vs. Propainter vs. Ours

#### VideoComposer

<video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/VC.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“VideoComposer”*

#### CoCoCo

<video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/COCOCO.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“CoCoCo”*

#### Propainter

<video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/propainter.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“Propainter”*

#### Ours

<video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/woman2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“Ours”*

---

## Qualitative Results on Object Removal

### Source Videos

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/woman2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/fire.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/man2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/woman1.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/man.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/car.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/blackswan.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/OR/bike.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

### Processed Videos

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/Output/man2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A series of staircases, 8K.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/Output/woman2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A living room with the white tall bookshelf.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/Output/man.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A body of sea with a setting sun.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/Output/car.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Billowing dust and sandy terrain.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/Output/blackswan.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A green lake with sparkling surface.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="static/FloED/Output/bike.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A large outdoor area with a dirt track.”*

---

## Qualitative Results on Background Restoration

### Source Videos

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/wave.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/cloud.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/coast.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/coast2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/flame.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/mist.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/star.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

### Processed Videos

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/wave.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“The golden lake surface at sunset.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/cloud.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“The blue sky filled with huge clouds.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/coast.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Sea waves crashing against the cliffs.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/coast2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Water appears to be flowing with iced rock.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/flame.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Large fire burning on logs in the fireplace.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/mist.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Mist draping the mountains like snow.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/Output/star.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Beautiful starry sky accompanied by a shooting star“*

---

## 📚 BibTeX

```bibtex
@article{gu2024advanced,
  title={Advanced Video Inpainting Using Optical Flow-Guided Efficient Diffusion},
  author={Gu, Bohai and Luo, Hao and Guo, Song and Dong, Peiran},
  journal={arXiv preprint arXiv:2412.00857},
  year={2024}
}
