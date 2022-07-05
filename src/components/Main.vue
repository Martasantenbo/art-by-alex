<script setup lang="ts">
</script>
<template>
  <article>
    <div class="min-h-11 bg-primary-pastel xl:min-h-21"></div>
    <img src="../assets/images/painting-up.png" />
    <div class="min-h-11 bg-primary-pastel xl:min-h-21"></div>
    <h2 class="text-secondary text-48px -mt-5 xl:(text-72px text-right pr-25 -mt-10)">Galerie</h2>
    <div class="main">
      <div class="flex gap-8 justify-center xl:(gap-20)">
        <div class="w-25 h-60 bg-green-500 xl:(w-88 h-138)">
          <img src="../assets/images/image-one.png" />
        </div>
        <div class="w-25 h-60 bg-green-500 xl:(w-88 h-138)">
          <img src="../assets/images/image-two.png" />
        </div>
        <div class="w-25 h-60 bg-green-500 xl:(w-88 h-138)">
          <img src="../assets/images/image-three.png" />
        </div>
      </div>

      <router-link to="/gallery" class="text-primary text-20px mt-5 inline-block xl:(mt-10 text-28px)">Click to see
        gallery
      </router-link>

      <h2 class="text-primary text-36px mb-3 mt-9 pl-4 xl:(mb-5 mt-17 pl-8 text-left text-56px text-secondary)">Header
      </h2>
      <div class="mx-4 p-4 bg-primary-pastel bg-opacity-90 text-left xl:(mx-9 p-9 min-w-302)">
        <p class="column-rule text-12px text-primary xl:(text-left text-18px)">Lorem ipsum dolor sit amet,
          consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.
          Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.Lorem ipsum dolor sit amet, consectetuer
          adipiscing
          elit. Vivamus
          luctus egestas leo. Nullam rhoncus aliquam metus. Donec ipsum massa, ullamcorper in, auctor et, scelerisque
          sed,
          est. Vivamus ac leo pretium faucibus. Fusce aliquam vestibulum ipsum. Praesent id justo in neque elementum
          ultrices. Nulla non arcu lacinia neque faucibus fringilla. Mauris tincidunt sem sed arcu. Sed elit dui,
          pellentesque a, faucibus vel, interdum nec, diam. Class aptent taciti sociosqu ad litora torquent per conubia
          nostra, per inceptos hymenaeos. Pellentesque ipsum. Aliquam ornare wisi eu metus. Fusce dui leo, imperdiet in,
          aliquam sit amet, feugiat eu, orci. Pellentesque ipsum.</p>
      </div>
    </div>
  </article>
</template>
<style scoped lang="scss">
.column-rule {
  column-count: 2;
  column-gap: 142px;
}


.main {
  @apply py-10 xl: (pt-70 pb-40);
}

@media screen and (max-width:1279px) {
  .column-rule {
    column-count: 1;
  }
}

@media screen and(min-width:1280px) {
  .main {
    background-image: url("../assets/images/homepage.svg");
    background-repeat: no-repeat;
    background-position: bottom right;
  }
}
</style>
