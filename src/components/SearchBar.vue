<template>
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
</template>

<script>
export default {
  name: "SearchBar"
};
</script>

