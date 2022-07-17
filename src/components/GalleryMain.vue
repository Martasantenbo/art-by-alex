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
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(30)">
        30:30</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(70)">
        40:40</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary cursor-pointer" @click="result(100)">
        140:140</div>
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
            class="min-w-80 min-h-80 max-w-80 max-h-80 xl:(min-w-90 min-h-90) overflow-hidden">
            <img :src="n.image" width="350" height="350">
          </div>
        </div>
      </div>
    </div>
    <Modal v-model="modal.open">

      <template v-slot:header>
        <h1 class="text-primary text-32px">{{ resultPaintings[modal.activeIndex].header }}</h1>
      </template>
      <template v-slot:content>
        <div class="flex justify-center gap-20">
          <img :src="resultPaintings[modal.activeIndex].image" />
          <video controls>
            <source :src="resultPaintings[modal.activeIndex].video" type="video/mp4" />
          </video>
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

.down {
  @apply pb-40;
  background-image: url("../assets/images/gallery-down.svg");
  background-repeat: no-repeat;
  background-position: bottom right;
}
</style>