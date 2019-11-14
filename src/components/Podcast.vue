<template>
  <div class="site-wrap" v-if="podcast">
    <podcasts-header/>

    <div
      class="site-blocks-cover overlay inner-page-cover"
      style="background-image: url(images/hero_bg_2.jpg);"
      data-aos="fade"
      data-stellar-background-ratio="0.5"
    >
      <div class="container">
        <div class="row align-items-center justify-content-center text-center">
          <div class="col-md-8" data-aos="fade-up" data-aos-delay="400">
            <h2 class="text-white font-weight-light mb-2 display-4">{{podcast.title}}</h2>
            <div class="text-white mb-3">
              <span class="text-white-opacity-05">
                <small>
                  By {{podcast.producerName}}
                  <span class="sep">/</span>
                  {{podcast.publishedDate}}
                </small>
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container site-section">
      <div class="player mb-5">
        <audio id="player2" preload="none" controls style="max-width: 100%">
          <source :src="podcast.mp3" type="audio/mp3">
        </audio>
      </div>

      <div class="row justify-content-center">
        <div class="col-md-10">
          <p>
            <span v-html="podcast.description"></span>
          </p>
        </div>
      </div>
    </div>

    <podcasts-footer/>
  </div>
</template>


<script>
import PodcastsFooter from "./PodcastsFooter";
import PodcastsHeader from "./PodcastsHeader";

import { mapState, mapActions } from "vuex";

export default {
  name: "Podcast",
  components: { PodcastsFooter, PodcastsHeader },
  computed: { ...mapState(["podcast"]) },

  methods: {
     ...mapActions(['loadPodcast'])
  },
  created() {
    this.loadPodcast(this.$route.params.id);
  }
};
</script>
