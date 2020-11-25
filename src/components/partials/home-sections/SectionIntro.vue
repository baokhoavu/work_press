<template>
  <section id="cf-intro">
    <div class="content flex px-0 lg:px-6 xl:px-10">
      <div
        class="absolute-img-wrapper absolute show-mobile bottom-0 hidden md:block xl:top-0 xl:mt-8"
      >
        <!-- <img
          class="max-w-1/3 md:max-w-3/4 xl:max-w-full opacity-0"
          v-for="(img, index) in images"
          :key="index"
          :src="img.src"
          :alt="img.alt"
        />-->
        <transition name="fade-change" mode="out-in">
          <img
            key="1"
            v-if="show"
            class="max-w-1/3 md:max-w-1/2 lg:max-w-2/3 xl:max-w-full"
            :src="images[imgIndex % 4].src"
          />
          <img
            key="2"
            v-else
            class="max-w-1/3 md:max-w-1/2 lg:max-w-2/3 xl:max-w-full"
            :src="images[(imgIndex % 4)].src"
          />
        </transition>
      </div>
      <div
        class="absolute mb-8 sm:mb-24 md:mb-32 lg:mb-64 xl:mb-0 xl:mt-16 xl:mr-12 right-0 bottom-0 xl:bottom-auto xl:top-0"
      >
        <img src="https://dev.causeforce.com/wp-content/uploads/2020/09/Teal_circle.png" />
      </div>
      <div class="absolute show mt-8 hidden bottom-0 xl:block lg:bottom-0">
        <img src="https://causeforce.com/wp-content/uploads/2020/09/Yellow_circle_fill.png" />
        <!-- <h2 style="bottom:20%;right:20%;" class="absolute inner text-white leading-none font-extrabold text-4xl">
          $1
          <br />BILLION
          <br />
          <span class="font-extrabold text-xl">
            FOR OUR
            <br />CLIENTS
          </span>
          <br />
        </h2>-->
      </div>
      <div class="w-1/5 md:w-1/4 lg:w-1/3"></div>
      <div class="w-3/5 md:w-2/4 lg:w-1/3 p-9 pt-6 sm:pt-0 self-center text-center xl:text-left">
        <h1
          class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl text-center xl:text-left font-bold leading-none text-white md:mb-4 lg:mb-6 xl:mb-8 tracking-wide"
        >
          We
          <span class="gradient-highlight bg-opacity-50">believe</span> you
          make the world a better place.
        </h1>
        <p
          class="text-base md:text-lg lg:text-xl mb-0 xl:mb-5 font-normal text-white text-center xl:text-left"
        >That's why we are passionate about supporting your goals.</p>
        <p
          class="text-base md:text-lg lg:text-xl sm:pb-10 xl:pb-0 font-normal text-white text-center xl:text-left xl:pr-12"
        >Fundraising has changed, but it doesn’t have to be a challenge.</p>
        <a
          href="#cf-vision"
          class="text-yellow-500 font-bold tracking-widest xl:mr-5 pb-2 border-b border-yellow-500 border-solid xl:pr-1"
          style
        >ASK US HOW</a>
      </div>
      <div class="w-1/5 md:w-1/4 lg:w-1/3"></div>
    </div>
  </section>
</template>

<script>
/**
 * Timer object as a function
 */
// function Timer(fn, t) {

// }
let timer;

export default {
  data() {
    return {
      images: [
        { src: "https://causeforce.com/wp-content/uploads/2020/09/family.jpg" },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/iStock_Man_BlueBack.jpg"
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/iStock_Woman_PinkBack.jpg"
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/crew-jumping.jpg"
        }
      ],
      transitionTimer: 5000, // 5 seconds per image
      imgIndex: 0,
      show: true
    };
  },
  methods: {
    Timer: function(fn, t) {
      var timedFunction = setInterval(fn, t);

      this.stop = function() {
        if (timedFunction) {
          clearInterval(timedFunction);
          timedFunction = null;
        }
        return this;
      };

      this.start = function() {
        if (!timedFunction) {
          this.stop();
          timedFunction = setInterval(fn, t);
        }
        return this;
      };

      this.reset = function(time) {
        t = time;
        return this.stop().start();
      };
    },
    change: function() {
      this.show = !this.show;
      if (this.imgIndex === 3) {
        this.imgIndex = 0;
      } else {
        this.imgIndex++;
      }
    }
  },
  mounted() {
    timer = new this.Timer(this.change, this.transitionTimer);
    // setTimeout(this.change, 1000);
  },
  computed: {}
};
</script>

<style type="postcss" scoped>
#cf-intro {
  max-height: 720px;
}

.absolute {
  z-index: -1;
}
.absolute.show {
  z-index: 10;
}
.absolute.show .inner {
  z-index: 11;
}

.absolute-img-wrapper img {
  -webkit-transition: opacity 1s ease-in-out;
  -moz-transition: opacity 1s ease-in-out;
  -o-transition: opacity 1s ease-in-out;
  transition: opacity 1s ease-in-out;
}

.object-left-top {
  margin-top: 2rem;
}

.content {
  position: relative;
  height: 600px;
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  background: linear-gradient(
    115deg,
    transparent 22%,
    #006699 22.1% 81.7%,
    transparent 81.8%
  );
}

.gradient-highlight {
  background: linear-gradient(
    transparent 52%,
    #05b7aa 52% 85%,
    transparent 85% 100%
  );
}

.lg\:self-center {
  padding-bottom: 0;
}

p.text-2xl {
  line-height: 1.75rem;
}

a.underline {
  text-underline-position: under;
  letter-spacing: 0.2rem;
}

/* changes fade animation start */

.fade-change-enter,
.fade-change-leave-to {
  opacity: 0;
}

.fade-change-enter-active,
.fade-change-leave-active {
  transition: all 1s ease-in;
}

/* changes fade animation end */

@media screen and (min-width: 1024px) {
  .content {
    background: linear-gradient(
      115deg,
      transparent 27%,
      #006699 27.1% 76.7%,
      transparent 76.8%
    );
  }

  .p-9 {
    padding-top: 3.5rem;
  }

  .lg\:bottom-0 {
    bottom: -3rem;
  }
}

@media screen and (min-width: 1280px) {
  /* h1.xl\:text-6xl {
    font-size: 3.9rem;
  } */
}

@media screen and (max-width: 1279px) {
  .absolute.show-mobile {
    z-index: 999;
    bottom: -3rem;
  }
}
</style>
