<template>
  <div class="site-wrap">
    <podcasts-header/>

    <div
      class="site-blocks-cover overlay"
      style="background-image: url(images/hero_bg_1.jpg);"
      data-aos="fade"
      data-stellar-background-ratio="0.5"
    >
      <div class="container">
        <div class="row align-items-center justify-content-center text-center">
          <div class="col-md-8" data-aos="fade-up" data-aos-delay="400">
            <h2
              class="text-white font-weight-light mb-2 display-4"
            >Episode 09: How To Create Web Page Using Bootstrap 4</h2>
            <div class="text-white mb-4">
              <span class="text-white-opacity-05">
                <small>By Mike Smith | 16 September 2017 | 1:30:20</small>
              </span>
            </div>
            <p>
              <a
                href="single-post.html"
                class="btn btn-primary btn-sm py-3 px-4 small"
              >Read The Transcript</a>
            </p>

            <div class="player">
              <audio id="player2" preload="none" controls style="max-width: 100%">
                <source
                  src="http://www.largesound.com/ashborytour/sound/AshboryBYU.mp3"
                  type="audio/mp3"
                >
              </audio>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="site-section bg-light">
      <div class="container">
        <div class="row mb-5" data-aos="fade-up">
          <div class="col-md-12 text-center">
            <h2 class="font-weight-bold text-black">Recent Podcasts</h2>
          </div>
        </div>

        <div
          v-show="podcasts"
          v-for="show in podcasts"
          :key="show.id"
          class="d-block d-md-flex podcast-entry bg-white mb-5"
          data-aos="fade-up"
        >
          <div class="image" :style="{'background-image': 'url(' + randomPic() + ')'}"></div>
          <div class="text">
            <h3 class="font-weight-light">
              <router-link :to="`/${show.id}`">{{show.title}}</router-link>
            </h3>
            <div class="text-white mb-3">
              <span class="text-black-opacity-05">
                <small>
                  By {{show.producerName}}
                  <span class="sep">/</span>
                  {{show.publishedDate}}
                </small>
              </span>
            </div>

            <div class="player">
              <audio id="player2" preload="none" controls style="max-width:100%">
                <source :src="show.mp3" type="audio/mp3">
              </audio>
            </div>
          </div>
        </div>
      </div>

      <div class="container" data-aos="fade-up">
        <div class="row">
          <div class="col-md-12 text-center">
            <div class="site-block-27">
              <ul class="text-center">
                <li>
                  <a @click.prevent="prevPage" v-if=" first === false" href="#">&lt;</a>
                </li>

                <li>
                  <a @click.prevent="nextPage" v-if=" last === false" href="#">&gt;</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div
      class="site-blocks-cover overlay inner-page-cover"
      style="background-image: url(images/hero_bg_1.jpg);"
      data-aos="fade"
      data-stellar-background-ratio="0.5"
    >
      <div class="container">
        <div class="row align-items-center justify-content-center text-center">
          <div class="col-md-8" data-aos="fade-up" data-aos-delay="400">
            <h2>Search</h2>
            <p
              class="mb-7"
            >Lorem ipsum dolor sit amet, consectetur adipisicing elit nihil saepe libero sit odio obcaecati veniam.</p>
            <form action="#" method="post" class="site-block-subscribe">
              <div class="input-group mb-5">
                <input
                  type="text"
                  class="form-control border-secondary text-white bg-transparent"
                  placeholder="What are you searching for ..."
                  aria-describedby="button-addon2"
                >
                <div class="input-group-append">
                  <button class="btn btn-primary" type="button" id="button-addon2">search</button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>

    <PodcastsFooter/>
  </div>
</template>

<script>
import PodcastsFooter from "./PodcastsFooter";
import PodcastsHeader from "./PodcastsHeader";

import { mapState, mapActions } from "vuex";

export default {
  name: "podcasts",
  components: { PodcastsFooter, PodcastsHeader },
  computed: { ...mapState(["last", "first", "podcasts"]) },
  methods: {
    ...mapActions(["loadPodcasts", "prevPage", "nextPage"]),
    randomPic: function() {
      let pic = "images/img_" + (Math.round(Math.random() * 4) + 1) + ".jpg";
      return pic;
    }
  },
  created() {
    this.loadPodcasts();
  }
};
</script>

