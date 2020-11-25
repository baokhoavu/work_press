<template>
  <div
    class="w-1/2 h-full card-wrapper mx-auto"
    v-bind:class="{ 'is-active': isActive }"
    v-on:click="flipCard(card.method)"
  >
    <div class="card">
      <div class="card-front p-3 sm:p-6 lg:p-12 w-full" v-bind:class="card.bgcolor">
        <h2
          class="text-sm md:text-base lg:text-lg text-white font-bold mb-2 lg:mb-6"
        >{{ card.title }}</h2>
        <p class="text-sm text-base lg:text-2xl leading-none text-white font-light">{{ card.text }}</p>
      </div>
      <div class="card-back px-2 py-3 sm:px-4 sm:py-6 lg:p-12 w-full" v-bind:class="card.bgcolor">
        <ul class="list-disc list-inside leading-none lg:leading-normal">
          <li
            class="text-sm md:text-base lg:text-xl text-white font-light pb-1 lg:pb-0"
            v-for="(service, index) in card.altservices"
            :key="index"
          >{{ service }}</li>
        </ul>
        <!-- <p class="text-2xl leading-none text-center text-white font-light">{{ card.alttext }}</p> -->
      </div>
    </div>
  </div>
</template>

<style type="postcss" scoped>
.card-wrapper {
  perspective: 1000px;
  height: 170px;
  width: 200px;
  max-width: 50%;
}

.card {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: left;
  transition: transform 0.6s;
  transform-style: preserve-3d;
}

.card-wrapper:hover {
  cursor: pointer;
}
.card-wrapper:hover .card {
  box-shadow: 0px 3px 8px 1px rgba(0, 0, 0, 0.5);
}

.card-wrapper.is-active .card {
  transform: rotateY(180deg);
}

.card-front,
.card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.card-back {
  transform: rotateY(180deg);
}

@media screen and (min-width: 640px) {
  .card-wrapper {
    height: 190px;
    width: 200px;
  }
}

@media screen and (min-width: 768px) {
}

@media screen and (min-width: 1024px) {
  .card-wrapper {
    height: 310px;
    width: 50%;
  }
}

@media screen and (min-width: 1280px) {
}
</style>

<script>
export default {
  props: {
    card: Object
  },
  data: function() {
    return {
      isActive: false
    };
  },
  methods: {
    flipCard: function(method) {
      if (method === "flip") {
        this.isActive = !this.isActive;
      } else {
      }
    }
  }
};
</script>
