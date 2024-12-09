# FloED <br><sub> Advanced Video Inpainting Using Optical Flow-Guided Efficient Diffusion </sub>

[![arXiv](https://img.shields.io/badge/arXiv-2412.00857-b31b1b)](https://arxiv.org/abs/2412.00857)
[![Project Page](https://img.shields.io/badge/Project-Website-orange)](https://nevsnev.github.io/FloED)


> [Bohai Gu]<sup>1,2</sup>,
> [Hao Luo] <sup>2</sup>,
> [Song Guo]<sup>1</sup>,
> [Peiran Dong]<sup>1</sup>,
> <sup>1</sup> Hong Kong University of Science and Technology
> <sup>2</sup> Alibaba 

## Method Overview

![Method Overview](static/FloED/Fig_0.jpg)
 <div class="content has-text-justified">
          <p>
            Recently, diffusion-based methods have achieved great improvements in the video inpainting task. However, these methods still face many challenges, such as maintaining temporal consistency and the time-consuming issue.
            This paper proposes an advanced video inpainting framework using optical Flow-guided Efficient Diffusion, called FloED. 
            Specifically, FloED employs a dual-branch architecture, where a flow branch first restores corrupted flow and a multi-scale flow adapter provides motion guidance to the main inpainting branch.
            Additionally, a training-free latent interpolation method is proposed to accelerate the multi-step denoising process using flow warping. Further introducing a flow attention cache mechanism, FLoED efficiently reduces the computational cost brought by incorporating optical flow.
            Comprehensive experiments in both background restoration and object removal tasks demonstrate that FloED outperforms state-of-the-art methods from the perspective of both performance and efficiency.
          </p>
        </div>

---

## Qualitative Comparison on Background Restoration

### Example 1: Water and Ice Scene

<video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Comparison_1.mp4" type="video/mp4">
</video>

*“Water appears to be flowing, the rock is covered in ice.”*

---

## Qualitative Comparison on Object Removal

### Example 2: Staircases Scene

<video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Comparison_2.mp4" type="video/mp4">
</video>

*“A series of staircases, 8K.”*

---

## Comparative Videos

### VideoComposer vs. CoCoCo vs. Propainter vs. Ours

#### VideoComposer

<video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/VC.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“VideoComposer”*

#### CoCoCo

<video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/COCOCO.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“CoCoCo”*

#### Propainter

<video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/propainter.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“Propainter”*

#### Ours

<video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/woman2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*“Ours”*

---

## Qualitative Results on Object Removal

### Source Videos

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/woman2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="shttps://github.com/NevSNev/FloED-main/tree/main/tatic/FloED/OR/fire.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/man2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/woman1.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/man.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/car.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/blackswan.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/OR/bike.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

### Processed Videos

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/man2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A series of staircases, 8K.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/woman2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A living room with the white tall bookshelf.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/man.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A body of sea with a setting sun.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/car.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Billowing dust and sandy terrain.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/blackswan.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A green lake with sparkling surface.”*

- <video autoplay controls muted loop playsinline height="50%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/bike.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“A large outdoor area with a dirt track.”*

---

## Qualitative Results on Background Restoration

### Source Videos

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/BR/wave.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/BR/cloud.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="static/FloED/BR/coast.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/BR/coast2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/BR/flame.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/BR/mist.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/BR/star.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“source”*

### Processed Videos

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/wave.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“The golden lake surface at sunset.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/cloud.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“The blue sky filled with huge clouds.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/coast.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Sea waves crashing against the cliffs.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/coast2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Water appears to be flowing with iced rock.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/flame.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Large fire burning on logs in the fireplace.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/mist.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  *“Mist draping the mountains like snow.“*

- <video autoplay controls muted loop playsinline height="100%">
  <source src="https://github.com/NevSNev/FloED-main/tree/main/static/FloED/Output/star.mp4" type="video/mp4">
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
