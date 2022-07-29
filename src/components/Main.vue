<script setup lang="ts">
</script>
<template>
  <article>
    <div class="min-h-11 bg-primary-pastel xl:min-h-21"></div>
    <img src="../assets/images/painting-up.png" width="1280" />
    <div class="min-h-11 bg-primary-pastel xl:min-h-21"></div>
    <router-link to="/gallery"
      class="text-secondary text-48px -mt-5 font-header inline-block md:(text-60px pl-18 pr-18 -mt-8) xl:(text-72px pr-25 pl-242 -mt-10)">
      Galerie
    </router-link>
    <div class="main">
      <div class="flex gap-8 justify-center xl:(gap-20)">
        <div class="w-25 h-45 md:(w-45 h-80) xl:(w-88 h-138)">
          <img src="../assets/images/image-one.png" />
        </div>
        <div class="w-25 h-45 md:(w-45 h-80) xl:(w-88 h-138)">
          <img src="../assets/images/image-two.png" />
        </div>
        <div class="w-25 h-45 md:(w-45 h-80) xl:(w-88 h-138)">
          <img src="../assets/images/image-three.png" />
        </div>
      </div>

      <router-link to="/gallery"
        class="text-primary text-20px inline-block font-text md:text-24px xl:(mt-10 text-28px)">Click to
        see
        gallery
      </router-link>

      <h2
        class="text-primary text-36px mb-3 mt-9 pl-4 font-header md:(text-44px text-left pl-5)xl:(mb-5 mt-17 pl-8 text-left text-56px)">
        Art by Alex
      </h2>
      <div class="mx-4 p-4 bg-primary-pastel bg-opacity-85 text-left xl:(mx-9 p-9 min-w-302)">
        <p
          class="column-rule leading-normal text-12px text-primary font-text md:(text-16px leading-normal) xl:(text-18px leading-normal)">
          Jmenuji se Alex a maluji abstraktní autorské obrazy, nejčastěji akrylovými barvami na plátno.
          Všechno to začalo vlastně dost nenápadně. Své první obrazy jsem malovala především sama
          pro sebe. Baví mě vytvářet akrylové abstrakce a pozorovat, jak se dílo vyvíjí. Mám ráda barvy
          a jejich vzájemné propojování.
          Umělecká tvorba pro mě byla dlouhou dobu hlavně formou relaxace. Pak se ale objevil první
          člověk, který viděl můj obraz a chtěl si ho koupit. Jednoho dne prostě zazvonil a byl tu. Měl
          pocit, že by moje dílo mohlo být originálním dárkem a zároveň mou práci finančně ocenil.
          Kupodivu to netrvalo dlouho a objevil se další zájemce. A pak další… a když těch lidí najednou
          bylo víc, než bych jako příležitostná malířka čekala, rozhodla jsem se vytvořit místo, kde se se
          mnou jednoduše spojíte.
          V galerii si můžete vybrat obraz, který vás zaujme, nebo si objednejte svůj vlastní, který pro
          vás na zakázku namaluji.
          <br>
          <br>Vítejte na webu Art by Alex.
        </p>
      </div>
    </div>
  </article>
</template>
<style scoped lang="scss">
.column-rule {
  column-count: 2;
  column-gap: 60px;
}


.main {
  @apply py-10 xl: (pt-114 pb-40);
}

@media screen and (max-width:767px) {
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
