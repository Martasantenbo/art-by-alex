<script setup lang="ts">
import { reactive, ref } from 'vue'
import Modal from './Modal.vue';
import { paintings } from './paintings'
const modal = reactive<{
  open: boolean
  activeIndex: number
}>({
  open: false,
  activeIndex: 0
});
const resultPaintings = ref(paintings)
const openModal = (index: number) => {
  modal.open = true;
  modal.activeIndex = index;
};
const result = (n: number) => {
  resultPaintings.value = n == 0 ? paintings : paintings.filter(x => x.format == n);
};

</script>
<template>
  <article>
    <div class="bg-primary-pastel py-3 md:(flex gap-11 justify-center) xl:(flex gap-11 justify-center)">
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary">Format:</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(4040)">
        40:40</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(3060)">
        30:60</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(3070)">
        30:70</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(5060)">
        50:60</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(5070)">
        50:70</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(6080)">
        60:80</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(0)">All
      </div>
    </div>

    <div class="up">
      <div class="down">
        <h2
          class="text-white text-36px py-7 font-header md:(text-secondary text-48px) xl:(text-primary text-56px py-12)">
          Galerie
        </h2>
        <div class="flex flex-wrap gap-19 justify-center">
          <div @click="openModal(index)" v-for="(n, index) in resultPaintings"
            class="min-w-80 min-h-80 max-w-80 max-h-80 cursor-pointer xl:(min-w-90 min-h-90) overflow-hidden">
            <img :src="n.image" width="350" height="350" :class="{ 'grscl': !n.available }">
          </div>
        </div>
      </div>
    </div>
    <Modal v-model="modal.open">

      <template v-slot:header>
        <h1 class="text-primary text-24px md:text-32px xl:text-32px">{{ resultPaintings[modal.activeIndex].header }}
        </h1>
      </template>
      <template v-slot:content>
        <div class="flex justify-center gap-5 overflow-auto md:gap-20 xl:gap-20">
          <div class="flex items-center max-h-50 max-w-50 md:(max-h-100 max-w-100) xl:(max-h-100 max-w-100)">
            <img :src="resultPaintings[modal.activeIndex].image" />
          </div>
          <video controls muted class="max-h-50 max-w-50 md:(max-h-100 max-w-100) xl:(max-h-100 max-w-100)">
            <source :src="resultPaintings[modal.activeIndex].video" type="video/mp4" />
          </video>
        </div>
      </template>
      <template v-slot:footer>
        <div v-if="resultPaintings[modal.activeIndex].available"
          class="flex justify-center text-16 px gap-4 pt-2 md:(gap-6 pt-4 text-24px) xl:(gap-6 pt-4 text-24px)">
          <h2 class="text-primary">Price: {{ resultPaintings[modal.activeIndex].price }},-
          </h2>
          <a :href="`mailto:info@artbyalex.cz?subject=Obraz ${resultPaintings[modal.activeIndex].header}`"
            class="cursor-pointer">Contact if
            interested</a>
        </div>
        <div v-else
          class="flex justify-center text-16 px gap-4 pt-2 md:(gap-6 pt-4 text-24px) xl:(gap-6 pt-4 text-24px)">
          Unavailable
        </div>
      </template>

    </Modal>
  </article>
</template>
<style scoped lang="scss">
.up {
  background-image: url("../assets/images/gallery-up.svg");
  background-repeat: no-repeat;
}

.grscl {
  filter: grayscale(80%) saturate(50%);
}

.down {
  @apply pb-40;
  background-image: url("../assets/images/gallery-down.svg");
  background-repeat: no-repeat;
  background-position: bottom right;
}
</style>