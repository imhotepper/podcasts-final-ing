<template>
  <div class="site-wrap">
    <podcasts-header/>

    <div
      class="site-blocks-cover overlay inner-page-cover"
      style="background-image: url(images/hero_bg_2.jpg);"
      data-aos="fade"
      data-stellar-background-ratio="0.5"
    >
      <div class="container">
        <div class="row align-items-center justify-content-center text-center">
          <div class="col-md-7" data-aos="fade-up" data-aos-delay="400">
            <h2 class="text-white font-weight-light mb-2 display-4">About us</h2>
          </div>
        </div>
      </div>
    </div>

    <div class="site-section bg-light">
      <div class="container">
        <div class="row">
          <div class="col-md-12 text-center mb-5" data-aos="fade-up">
            <h2 class="display-4 mb-5 text-black">The Podcaster</h2>
          </div>
          <div class="col-md-6 col-lg-4 text-center mb-5" data-aos="fade-up">
            <img src="images/person_1.jpg" alt="Image" class="img-fluid w-50 rounded-circle mb-3">
            <h2 class="text-black font-weight-light mb-4">Jean Smith</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur ab quas facilis obcaecati non ea, est odit repellat distinctio incidunt, quia aliquam eveniet quod deleniti impedit sapiente atque tenetur porro?</p>
            <p>
              <a href="#" class="pl-0 pr-3">
                <span class="icon-twitter"></span>
              </a>
              <a href="#" class="pl-3 pr-3">
                <span class="icon-instagram"></span>
              </a>
              <a href="#" class="pl-3 pr-3">
                <span class="icon-facebook"></span>
              </a>
            </p>
          </div>
          <div class="col-md-6 col-lg-4 text-center mb-5" data-aos="fade-up">
            <img src="images/person_2.jpg" alt="Image" class="img-fluid w-50 rounded-circle mb-3">
            <h2 class="text-black font-weight-light mb-4">Claire Smith</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur ab quas facilis obcaecati non ea, est odit repellat distinctio incidunt, quia aliquam eveniet quod deleniti impedit sapiente atque tenetur porro?</p>
            <p>
              <a href="#" class="pl-0 pr-3">
                <span class="icon-twitter"></span>
              </a>
              <a href="#" class="pl-3 pr-3">
                <span class="icon-instagram"></span>
              </a>
              <a href="#" class="pl-3 pr-3">
                <span class="icon-facebook"></span>
              </a>
            </p>
          </div>
          <div class="col-md-6 col-lg-4 text-center mb-5" data-aos="fade-up">
            <img src="images/person_4.jpg" alt="Image" class="img-fluid w-50 rounded-circle mb-3">
            <h2 class="text-black font-weight-light mb-4">John Smith</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur ab quas facilis obcaecati non ea, est odit repellat distinctio incidunt, quia aliquam eveniet quod deleniti impedit sapiente atque tenetur porro?</p>
            <p>
              <a href="#" class="pl-0 pr-3">
                <span class="icon-twitter"></span>
              </a>
              <a href="#" class="pl-3 pr-3">
                <span class="icon-instagram"></span>
              </a>
              <a href="#" class="pl-3 pr-3">
                <span class="icon-facebook"></span>
              </a>
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="site-section">
      <div class="container">
        <div class="row" data-aos="fade-up">
          <div class="col-md-12">
            <img src="images/hero_bg_1.jpg" alt="Image" class="img-fluid mb-5">
          </div>
          <div class="col-md-6">
            <p class="lead">Lorem ipsum dolor sit amet,
              <a href="#">consectetur</a> adipisicing elit. Asperiores veritatis quis cumque? Obcaecati quisquam incidunt minima magnam quod quis saepe.
            </p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id accusamus eos quisquam incidunt ut officia inventore at iste facere perferendis, quidem ratione atque quae. Labore consequuntur nobis minima optio praesentium voluptas non sed beatae, quibusdam neque, recusandae vel, dolorem architecto!</p>
          </div>
          <div class="col-md-6">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis consectetur quidem enim minima aut laudantium, eum voluptas asperiores, quod minus quasi porro maxime quas ducimus mollitia. Iure nihil dolorum aliquam!</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis consectetur quidem enim minima aut laudantium, eum voluptas asperiores, quod minus quasi porro maxime quas ducimus mollitia. Iure nihil dolorum aliquam!</p>
          </div>
        </div>
      </div>
    </div>

    <podcasts-footer/>
  </div>
</template>



<script>
import PodcastsFooter from "./PodcastsFooter";
import PodcastsHeader from "./PodcastsHeader";

export default {
  name: "Podcast",
  components: { PodcastsFooter, PodcastsHeader }
};
</script>
