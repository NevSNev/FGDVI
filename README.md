<section class="hero">
  <div class="hero-body">
    <div class="container is-max-desktop">
      <div class="columns is-centered">
        <div class="column has-text-centered">
          <h1 class="title is-1 publication-title">
            <span style="font-weight: 1000;">FloED:</span>
            <span>Advanced Video Inpainting Using Optical <span style="font-weight: 1000;">Flo</span>w-Guided <span style="font-weight: 1000;">E</span>fficient <span style="font-weight: 1000;">D</span>iffusion</span>
          </h1>
     <div class="is-size-5 publication-authors">
       <ul style="list-style: none; padding: 0; display: inline-block;">
         <li style="display: inline; margin-right: 10px;">Bohai Gu<sup>1,2</sup></li>,
         <li style="display: inline; margin-right: 10px;">Hao Luo<sup>2*</sup></li>,
         <li style="display: inline; margin-right: 10px;">Song Guo<sup>1*</sup></li>,
         <li style="display: inline;">Peiran Dong<sup>1</sup></li>
       </ul>
     </div>

<div class="is-size-5 publication-authors">
  <span class="author-block"><sup>1</sup> Hong Kong University of Science and Technology</span><br>
  <span class="author-block"><sup>2</sup> Alibaba Group</span><br>
  <span class="author-block"><sup>*</sup> Co-Corresponding authors</span> 
</div>

          <div class="column has-text-centered">
            <div class="publication-links">
              <!-- PDF Link. -->
              <span class="link-block">
                <a href="https://arxiv.org/pdf/2412.00857"
                   class="external-link button is-normal is-rounded is-dark" target="_blank">
                  <span class="icon">
                      <i class="fas fa-file-pdf"></i>
                  </span>
                  <span>Paper</span>
                </a>
              </span>
              <span class="link-block">
                <a href="https://arxiv.org/abs/2412.00857" target="_blank"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="ai ai-arxiv"></i>
                  </span>
                  <span>arXiv</span>
                </a>
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- 
<section class="hero teaser">
  <div class="container is-max-desktop">
    <div class="hero-body">
      <video id="teaser" autoplay muted loop playsinline controls width="100%">
        <source src="./static/videos/teaser_vid.mp4"
                type="video/mp4">
      </video>
      <h2 class="subtitle has-text-centered">
        RadSplat enables high-quality real-time rendering of complex large-scale scenes at 900+ FPS.
      </h2>
    </div>
  </div>
</section>
 -->
<section class="section">
  <div class="container is-max-desktop">
    <!-- Abstract. -->
    <div class="columns is-centered has-text-centered">
      <div class="column is-four-fifths">
        <h2 class="title is-3">Abstract</h2>
        <div class="content has-text-justified">
          <p>
            Recently, diffusion-based methods have achieved great improvements in the video inpainting task. However, these methods still face many challenges, such as maintaining temporal consistency and the time-consuming issue.
            This paper proposes an advanced video inpainting framework using optical Flow-guided Efficient Diffusion, called FloED. 
            Specifically, FloED employs a dual-branch architecture, where a flow branch first restores corrupted flow and a multi-scale flow adapter provides motion guidance to the main inpainting branch.
            Additionally, a training-free latent interpolation method is proposed to accelerate the multi-step denoising process using flow warping. Further introducing a flow attention cache mechanism, FLoED efficiently reduces the computational cost brought by incorporating optical flow.
            Comprehensive experiments in both background restoration and object removal tasks demonstrate that FloED outperforms state-of-the-art methods from the perspective of both performance and efficiency.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="section">
  <div class="container is-max-desktop">
    <h2 class="title is-3">Method Overview</h2>
    <div class="is-centered has-text-centered"><img src="static/FloED/Fig_0.jpg" alt="" width="100%"></div>
    <p style="padding-top: 0.5rem; padding-bottom: 0.5rem;">
      Our method employs a dual-branch architecture implemented through a two-stage training approach:
      <ol style="padding-left: 1.5rem;">
      <li>we first focus on the upper branch, optimizing the motion layer to adapt specifically to the video inpainting domain. </li>
      <li>we use a dedicated flow branch complemented by <span class="text-bold">a multi-scale flow adapter</span>, which provides flow guidance covering upblocks of primary UNet. During the inference phase, we enhance efficiency by integrating the  <span class="text-bold">flow attention cache</span>.</li>
      <li>We introduce a  <span class="text-bold">training-free latent interpolation </span>technique that leverages optical flow to speed up the multi-step denoising process. Complemented by a flow attention cache mechanism, FloED efficiently reduces the additional computational costs introduced by the flow. 
      </ol>
    </p>
        <p style="padding-top: 0.5rem; padding-bottom: 0.5rem;">
    <div class="is-centered has-text-centered"><img src="static/FloED/Fig_1.jpg" alt="" width="80%"> </div>

  </div>
</section>

<section class="section">
  <div class="container is-max-desktop">
    <h2 class="title is-3">Qualitative Comparison on Background Restoration</h2>
    <div class="columns is-centered">

      <!-- Visual Effects. -->
      <div class="column">
        <div class="content">
          <!-- <h2 class="title is-4">Comparison to 3DGS</h2> -->

          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Comparison_1.mp4"
                    type="video/mp4">
          </video>
<p style="text-align: center; font-size: 24px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
  "Water appears to be flowing, the rock is covered in ice."
</p>
        </div>
      </div>
      <!--/ Visual Effects. -->
    </div>
  </div>
</section>



<section class="section">
  <div class="container is-max-desktop">
    <h2 class="title is-3">Qualitative Comparison on Object Removal</h2>
    <div class="columns is-centered">

      <!-- Visual Effects. -->
      <div class="column">
        <div class="content">
          <!-- <h2 class="title is-4">Comparison to 3DGS</h2> -->

          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Comparison_2.mp4"
                    type="video/mp4">
          </video>
<p style="text-align: center; font-size: 24px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
  "A series of staircases, 8K."
</p>
        </div>
      </div>
      <!--/ Visual Effects. -->
    </div>
  </div>
</section>

<section class="section">
  <div class="container is-max-desktop">
    <div class="columns is-centered">

      <!-- Visual Effects. -->
      <div class="column">
        <div class="content">
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/VC.mp4"
                    type="video/mp4">
          </video>
          <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            VideoComposer
           </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/COCOCO.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            CoCoCo
          </p>
        </div>
      </div>

      <div class="column">
        <div class="columns is-centered">
          <div class="column content">
                              <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/propainter.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
                Propainter
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/woman2.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
                Ours
          </p>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>


<section class="section">
  <div class="container is-max-desktop">
    <h2 class="title is-3">Qualitative Results on Object Removal</h2>
    <div class="columns is-centered">
      <!-- Visual Effects. -->
      <div class="column">
        <div class="content">
          <video autoplay controls muted loop playsinline height="50%">
            <source src="static/FloED/OR/woman2.mp4"
                    type="video/mp4">
          </video>
        </div>
      </div>
      <div class="column">
        <div class="content">
          <video autoplay controls muted loop playsinline height="50%">
            <source src="static/FloED/Output/woman.mp4"
                    type="video/mp4">
          </video>
        </div>
      </div>
      <div class="column">
        <div class="content">
          <video autoplay controls muted loop playsinline height="50%">
            <source src="static/FloED/OR/fire.mp4"
                    type="video/mp4">
            </video>
          </div>
        </div>
      <div class="column">
        <div class="content">
          <video autoplay controls muted loop playsinline height="50%">
            <source src="static/FloED/Output/fire.mp4"
                    type="video/mp4">
          </video>
        </div>
      </div>

      </div>

    <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            "Forest with a stream running through it."    
             "Fire burning in a fireplace, with a log burning."     
          </p>

    <div class="columns is-centered">

      <!-- Visual Effects. -->
      <div class="column">
        <div class="content">
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/OR/man2.mp4"
                    type="video/mp4">
          </video>
    <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/OR/woman1.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/OR/man.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
           <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/OR/car.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/OR/blackswan.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/OR/bike.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
        </div>
      </div>

      <div class="column">
        <div class="columns is-centered">
          <div class="column content">
                              <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/man2.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            "A series of staircases, 8K."
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/woman2.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            "A living room with the white tall bookshelf."
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/man.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            "A body of sea  with a setting sun.“
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/car.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “Billowing dust and sandy terrain.”
          </p>
                              <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/blackswan.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “A green lake with sparkling surface.”
          </p>
          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/bike.mp4"
                    type="video/mp4">
          </video>
           <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “A large outdoor area with a dirt track.”
          </p>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>

<section class="section">
  <div class="container is-max-desktop">
    <h2 class="title is-3">Qualitative Results on Background Restoration</h2>

    <div class="columns is-centered">

      <!-- Visual Effects. -->
      <div class="column">
        <div class="content">
          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/wave.mp4"
                    type="video/mp4">
          </video>
                        <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/cloud.mp4"
                    type="video/mp4">
          </video>
                        <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/coast.mp4"
                    type="video/mp4">
          </video>
                        <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/coast2.mp4"
                    type="video/mp4">
          </video>
                        <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/flame.mp4"
                    type="video/mp4">
          </video>
                        <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
           <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/mist.mp4"
                    type="video/mp4">
          </video>
                        <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/BR/star.mp4"
                    type="video/mp4">
          </video>
              <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            source
          </p>

        </div>
      </div>

      <div class="column">
        <div class="columns is-centered">
          <div class="column content">
          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/wave.mp4"
                    type="video/mp4">
          </video>
                                  <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “The golden lake surface at sunset.“
          </p>
          <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/cloud.mp4"
                    type="video/mp4">
          </video>
                                            <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “The blue sky filled with huge clouds.“
          </p>
                              <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/coast.mp4"
                    type="video/mp4">
          </video>
                                            <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “Sea waves crashing against the cliffs.“
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/coast2.mp4"
                    type="video/mp4">
          </video>
                                            <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “Water appers to be flowing with iced rock.“
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/blame.mp4"
                    type="video/mp4">
          </video>
                                            <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “Large fire burning on logs in the fireplace.“
          </p>
                    <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/mist.mp4"
                    type="video/mp4">
          </video>
                                            <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            "Mist draping the mountains like snow.“
          </p>
                              <video autoplay controls muted loop playsinline height="100%">
            <source src="static/FloED/Output/star.mp4"
                    type="video/mp4">
          </video>
                                  <p style="text-align: center; font-size: 24px;  margin-bottom: 20px; font-family: 'Times', 'Times New Roman', serif;font-style: italic;">
            “Beautiful starry sky accompanied by a shooting star“
          </p>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>


<section class="section" id="BibTeX">
  <div class="container is-max-desktop content">
    <h2 class="title">BibTeX</h2>
    <pre><code> 
@article{gu2024advanced,
  title={Advanced Video Inpainting Using Optical Flow-Guided Efficient Diffusion},
  author={Gu, Bohai and Luo, Hao and Guo, Song and Dong, Peiran},
  journal={arXiv preprint arXiv:2412.00857},
  year={2024}
}
  </code></pre>
  </div>
</section>




<!-- <section class="section">
  <div class="container is-max-desktop content">
    <h2 class="title">Acknowledgements</h2>
    <p>
      We would like to thank .

The website is built on top of the <a </a>.
    </p>
  </div>
</section> -->
