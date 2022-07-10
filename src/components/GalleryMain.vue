<script setup lang="ts">
import { reactive } from 'vue'
import Modal from './Modal.vue';
const modal = reactive<{
  open: boolean
  activeIndex: number
}>({
  open: false,
  activeIndex: 0
});
const openModal = (index: number) => {
  modal.open = true;
  modal.activeIndex = index;
};
</script>
<template>
  <article>
    <div class="bg-primary-pastel py-2 md:(flex gap-18 justify-center) xl:(flex gap-18 justify-center)">
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary">Format:</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary">30:30</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary">40:40</div>
      <div class="text-20px leading-normal md:text-24px xl:text-24px text-primary">140:140</div>
    </div>
    <div class="up">
      <div class="down">
        <h2 class="text-white text-36px py-7 md:(text-secondary text-48px) xl:(text-primary text-56px py-12)">Galerie
        </h2>
        <div class="flex flex-wrap gap-19 justify-center">
          <div @click="openModal(index)" v-for="(n, index) in 9"
            class="bg-green-500 min-w-80 min-h-80 xl:(min-w-90 min-h-90)">{{
                n
            }}</div>
        </div>
      </div>
    </div>
    <Modal v-model="modal.open">
      <template v-slot:header>{{ modal.activeIndex + 1 }}</template>
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