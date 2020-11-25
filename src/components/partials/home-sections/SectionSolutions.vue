<template>
  <section id="cf-solutions">
    <div class="content flex flex-col lg:flex-row px-0 md:px-2 lg:px-6 xl:px-10">
      <div class="object-left-top absolute hidden lg:block"></div>
      <div class="lg:w-1/3 pt-4 lg:pt-10 max-w-lg lg:max-w-none self-center lg:self-start text-center lg:text-left">
        <h1
          class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl font-bold leading-none text-black mb-2 lg:mb-6 tracking-wide"
        >
          We
          <br class="hidden lg:block"/>offer
          <br class="hidden lg:block"/>
          <span class="gradient-highlight bg-opacity-50">solutions.</span>
        </h1>
        <p class="text-base md:text-lg lg:text-xl font-normal text-black xl:pr-4">
          Our wide range of customizable and
          turn-key solutions are designed to help
          not-for-profit clients create engaging
          fundraising programs for a changing world.
        </p>
        <a
          href="#cf-vision"
          class="text-base text-yellow-500 lg:text-cfteal-100 font-bold tracking-widest border-b border-yellow-500 lg:border-cfteallight-100 border-solid lg:pr-1"
        >LET'S TALK ABOUT YOUR GOAL</a>
      </div>
      <div id="cards-holder" class="lg:w-2/3 px-0 lg:px-8 pt-3 lg:pt-10 pb-2 lg:pb-0 self-center lg:self-start">
        <div class="flex flex-wrap fade-in">
          <card v-for="card in cards" :card="card" :key="card.index" /><card>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Card from "../../widgets/Card.vue";

export default {
  components: {
    card: Card
  },
  data() {
    return {
      cards: [
        {
          index: 1,
          bgcolor: "bg-yellow-500",
          title: "Discover.",
          text: "Cause/Brand Development, Marketing & Strategy & Consulting",
          altservices: ["Branding & Content", "Media & Acquisition", "Digital Marketing"],
          method: "flip",
          alignment: "mx-auto"
        },
        {
          index: 2,
          bgcolor: "bg-cfgreen-100",
          title: "Implement.",
          text: "P2P Technology Solutions",
          altservices: ["Digital Platform Audits", "UX/UI", "Analytics & Research"],
          method: "flip",
          alignment: "mx-auto"
        },
        {
          index: 3,
          bgcolor: "bg-cfteallight-100",
          title: "Engage.",
          text: "Participant Journey & Sponsorship",
          altservices: ["Donor/Participant Relations", "Sponsorship Acquisition & Management"],
          method: "flip",
          alignment: "mx-auto"
        },
        {
          index: 4,
          bgcolor: "bg-cfblue-100",
          title: "Participate.",
          text: "Live & Virtual Experiences",
          altservices: ["Live Event Production", "Virtual Event Services", "Route Design & Logistics", "Volunteer Management"],
          method: "flip",
          alignment: "mx-auto"
        }
      ]
    };
  }
};
</script>

<style type="postcss" scoped>
#cf-solutions {
  max-height: 720px;
}

.absolute {
  z-index: -1;
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
    #0d9db3 22.1% 81.7%,
    transparent 81.8%
  );
}

p.text-xl {
  line-height: 1.75rem;
}

a.lg\:pr-1 {
  letter-spacing: 0.2rem;
  overflow-wrap: normal;
  display: inline-flex;
  padding-bottom: 10px;
}

.gradient-highlight {
  background: linear-gradient(
    transparent 52%,
    #ddf1f2 52% 85%,
    transparent 85% 100%
  );
}

#cards-holder {
  max-width: 100%;
}
@media screen and (min-width: 400px) {
  #cards-holder {
  max-width: 400px;
}
}

@media screen and (min-width: 768px) {

}

@media screen and (min-width: 1024px) {
  .content {
    background: linear-gradient(
      115deg,
      transparent 27%,
      #0d9db3 27.1% 76.7%,
      transparent 76.8%
    );
  }

  a.lg\:pr-1 {
    max-width: 134px;
  }

  #cards-holder {
    max-width: none;
  }
}
</style>
