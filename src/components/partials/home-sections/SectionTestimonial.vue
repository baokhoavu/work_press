<template>
  <section id="cf-testimonial">
    <div
      class="content flex lg:flex-wrap flex-col lg:flex-row xl:py-10 px-0 md:px-2 lg:px-6 xl:px-10"
    >
      <div class="mt-10 absolute hidden lg:block">
        <img
          class="ml-40"
          src="https://dev.causeforce.com/wp-content/uploads/2020/09/Teal_circle.png"
        />
      </div>
      <div class="bottom-0 right-0 absolute show" style="bottom: 4rem; right: 7rem;">
        <!-- <img
          class="circle"
          src="https://causeforce.com/wp-content/uploads/2020/09/yellow-for-logos-testimonialsection.png"
        />
        <img
          style="max-width:128px;position:absolute;bottom:38%;right:28%;"
          class="logo"
          src="https://causeforce.com/wp-content/uploads/2020/09/UCI.jpg"
        />-->
      </div>
      <div class="w-0 lg:w-1/3 self-center xl:self-end">
        <video class="hidden xl:block shadow-lg" width="320" height controls>
          <source
            src="https://causeforce.com/wp-content/uploads/video/Video_cropped.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div
        class="w-2/3 sm:w-1/2 lg:w-1/3 pt-8 pb-0 sm:py-3 lg:pt-0 lg:pr-5 self-center xl:self-end"
      >
        <h2
          class="text-sm sm:text-base md:text-lg lg:text-xl text-center lg:text-left sm:text-white font-bold tracking-widest leading-none pb-4 lg:pb-8"
        >CLIENT LOVE</h2>
        <h2
          class="text-sm sm:text-base lg:text-xl text-center lg:text-left sm:text-white font-normal leading-none mb-3 lg:mb-5"
        >
          “The four 'Rs' you want from a great
          fundraising partner and supplier
          (are) Reliability, Responsibility, you
          want them to be Responsive and
          most of all you want Results.
        </h2>
        <h2
          class="text-sm sm:text-base lg:text-xl text-center lg:text-left sm:text-white font-normal leading-none mb-0"
        >CauseForce produces results.</h2>
        <h2
          class="text-sm sm:text-base lg:text-xl text-center lg:text-left sm:text-white font-normal leading-none mb-3 lg:mb-10"
        >
          In this every challenging COVID era,
          it’s so important to have a partner at
          a very experienced organization like
          CauseForce.”
        </h2>
        <p class="text-sm sm:text-base md:text-lg lg:text-xl font-normal leading-none text-white">
          Paul Alofs -
          <span class="text-sm md:text-base font-bold">FORMER CEO</span>
          <br />
          <span class="text-sm md:text-base font-bold">PRINCESS MARGARET CANCER FOUNDATION</span>
        </p>
      </div>
      <div class="w-full lg:w-1/3 relative self-center lg:self-end" style="max-width:282px">
        <img
          class="circle mb-5"
          src="https://causeforce.com/wp-content/uploads/2020/09/yellow-for-logos-testimonialsection.png"
        />
        <div class="absolute-img-wrapper">
          <transition name="fade-change" mode="out-in">
            <img
              key="1"
              v-if="show"
              v-bind:style="images[imgIndex % images.length].styles"
              class="logo absolute"
              :src="images[imgIndex % images.length].src"
            />
            <img
              key="2"
              v-else
              v-bind:style="images[imgIndex % images.length].styles"
              class="logo absolute"
              :src="images[imgIndex % images.length].src"
            />
          </transition>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
let testimonialTimer;

export default {
  data() {
    return {
      images: [
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/Canadian-Tire-Jumpstart-Logo_copy.png",
          styles: { "max-width": "145px", bottom: "31%", right: "23.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/CHOC.png",
          styles: { "max-width": "145px", bottom: "37%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/Canary.png",
          styles: { "max-width": "145px", bottom: "37%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/PFC_copy.png",
          styles: { "max-width": "145px", bottom: "41%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/UCI.png",
          styles: { "max-width": "128px", bottom: "41%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/BCCANCER_Foundation_PMS.png",
          styles: { "max-width": "145px", bottom: "43%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/13-06-24_ACF_logo_CMYK_copy.png",
          styles: { "max-width": "145px", bottom: "44%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/SMG_Logo_Color-Med_res.png",
          styles: { "max-width": "145px", bottom: "41%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/mJF.png",
          styles: { "max-width": "145px", bottom: "45%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/RWBH.png",
          styles: { "max-width": "145px", bottom: "30%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/MS.png",
          styles: { "max-width": "145px", bottom: "41%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/MDAnderson_logo.png",
          styles: { "max-width": "145px", bottom: "39%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/MCU.png",
          styles: { "max-width": "145px", bottom: "44%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/pmcf.png",
          styles: { "max-width": "145px", bottom: "48%", right: "23.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/ccrf_vert_3c.png",
          styles: { "max-width": "145px", bottom: "41%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/Volunteers+of+America(blank)-formatted.png",
          styles: { "max-width": "145px", bottom: "29%", right: "24.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/PMAC_FOUNDATION_CMYK_HORIZONTAL.png",
          styles: { "max-width": "145px", bottom: "47%", right: "23.5%" }
        },
        {
          src:
            "https://causeforce.com/wp-content/uploads/2020/09/client-logos/Cerebral_Palsy_Alliance.png",
          styles: { "max-width": "145px", bottom: "43%", right: "25.5%" }
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
      if (this.imgIndex === this.images.length - 1) {
        this.imgIndex = 0;
      } else {
        this.imgIndex++;
      }
    }
  },
  mounted() {
    testimonialTimer = new this.Timer(this.change, this.transitionTimer);
  }
};
</script>

<style type="postcss" scoped>
#cf-testimonial {
  max-height: 720px;
}

.absolute {
  z-index: -1;
}
.absolute.show {
  z-index: 10;
}

.absolute.show .circle {
  z-index: 11;
}
.absolute.logo {
  z-index: 12;
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
    #0d9db3 22.1% 81.7%,
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
      #0d9db3 27.1% 76.7%,
      transparent 76.8%
    );
  }
}
</style>
