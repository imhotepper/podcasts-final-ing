<template>
  <header class="site-navbar py-4 absolute transparent" role="banner">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-3" data-aos="fade-down">
          <h1>
            <router-link to="/" class="text-white h2">Podca</router-link>
          </h1>
        </div>
        <div class="col-9" data-aos="fade-down"></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "PodcastsHeader"
};
</script>

