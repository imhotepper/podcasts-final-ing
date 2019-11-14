<template>
 <router-view/>
</template>

<script>
import Podcasts from "./components/Podcasts";
import Podcast from "./components/Podcast";
import About from "./components/About";

import "mediaelement/full";

export default {
  name: "App",
  components: { Podcasts, Podcast, About },
  mounted() {
    var mediaElements = document.querySelectorAll("video, audio"),
      total = mediaElements.length;
   
    for (var i = 0; i < total; i++) {
      new MediaElementPlayer(mediaElements[i], {
        pluginPath: "https://cdn.jsdelivr.net/npm/mediaelement@4.2.7/build/",
        shimScriptAccess: "always",
        success: function() {
          var target = document.body.querySelectorAll(".player"),
            targetTotal = target.length;
          for (var j = 0; j < targetTotal; j++) {
            target[j].style.visibility = "visible";
          }
        }
      });
    }
  }
};
</script>

