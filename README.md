# FloED <br><sub> Advanced Video Inpainting Using Optical Flow-Guided Efficient Diffusion </sub>

> Bohai Gu <sup>1,2</sup>,
> Hao Luo <sup>2</sup>,
> Song Guo <sup>1</sup>,
> Peiran Dong <sup>1</sup>,

> <sup>1</sup> Hong Kong University of Science and Technology
> <sup>2</sup> Alibaba Group

[![arXiv](https://img.shields.io/badge/arXiv-2412.00857-b31b1b)](https://arxiv.org/abs/2412.00857)
[![Project Page](https://img.shields.io/badge/Project-Website-orange)](https://nevsnev.github.io/FloED)




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



For more visualization results, please check our [project page](https://nevsnev.github.io/FloED).

## Code coming soon.


## 📚 BibTeX

```bibtex
@article{gu2024advanced,
  title={Advanced Video Inpainting Using Optical Flow-Guided Efficient Diffusion},
  author={Gu, Bohai and Luo, Hao and Guo, Song and Dong, Peiran},
  journal={arXiv preprint arXiv:2412.00857},
  year={2024}
}
