<template>
  <section id="cf-experiences">
    <div class="content flex flex-wrap flex-column px-0 md:px-2 lg:px-6 xl:px-10">
      <div class="object-left-top absolute hidden lg:block"></div>
      <div class="w-full flex flex-wrap pt-5 sm:justify-center">
        <div class="w-1/4 lg:self-center"></div>
        <div class="w-2/4 flex flex-col self-center xl:flex-row">
          <div class="self-center mb-2 sm:mb-5 xl:mb-0 xl:self-start xl:pr-4">
            <h1
              class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl font-bold leading-none text-black tracking-wide"
            >
              We
              <br />create epic
              <br />
              <span class="gradient-highlight bg-opacity-50">experiences.</span>
            </h1>
          </div>
          <div class="self-center xl:self-end">
            <a
              href="#cf-vision"
              class="inline-block text-sm px-3 md:px-4 py-4 lg:px-6 lg:py-5 mb-3 whitespace-no-wrap leading-none font-bold text-cfteal-100 bg-white hover:text-teal-500 lg:mt-4 xl:mt-0 tracking-widest shadow-lg"
            >START YOURS NOW</a>
          </div>
        </div>
        <div class="w-1/4"></div>
      </div>
      <div
        id="story-box-wrapper"
        class="mx-auto w-full flex sm:flex-wrap flex-col sm:flex-row sm:mb-5 sm:justify-center"
      >
        <div
          class="mb-3 sm:mb-0 sm:w-1/3 px-6 self-center fade-in sm:self-start"
          v-for="event in events"
          :key="event.id"
          :class="event.align"
        >
          <img :src="event.img" class="mb-3 shadow-lg" />
          <div>
            <h2
              style="max-width: 260px;"
              class="text-sm text-cfdarkblue-100 font-medium mb-0"
            >{{ event.eventname }}</h2>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      events: [
        {
          id: "0",
          img:
            "https://dev.causeforce.com/wp-content/uploads/2020/09/Photo_1_experience.png",
          eventname:
            "We deliver fully integrated complex scalable live and virtual events and experiences from concept to completion. Our team also offers flexible and a la carte services where and when you need them.",
          eventtype: "Ride",
          align: "lg:self-end"
        },
        {
          id: "1",
          img:
            "https://dev.causeforce.com/wp-content/uploads/2020/09/Photo_2_experience.png",
          eventname:
            "We have a deep understanding of the participant journey and the know-how to engage supporters and sponsors to maximize results and build a community.",
          align: "lg:self-start"
        },
        {
          id: "2",
          img:
            "https://dev.causeforce.com/wp-content/uploads/2020/09/Photo_3_experience.png",
          eventname:
            "We leverage technology solutions to reach a new generation of donors who are looking for unique virtual fundraising experiences that tap into their passions for tech and gaming.",
          align: "lg:self-center"
        }
      ]
    };
  }
};
</script>

<style type="postcss" scoped>
#cf-experiences {
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
    65deg,
    transparent 22%,
    #ddf1f2 22.1% 81.7%,
    transparent 81.8%
  );
}

p.text-xl {
  line-height: 1.75rem;
}

.gradient-highlight {
  background: linear-gradient(
    transparent 52%,
    #ffd447 52% 85%,
    transparent 85% 100%
  );
}

#story-box-wrapper {
  max-height: 391px;
  overflow: auto;
}

@media screen and (min-width: 640px) and (max-width: 1023px) {
  img.shadow-lg {
    max-width: 202px;
  }
}
@media screen and (min-width: 640px) {
  #story-box-wrapper {
    max-height: none;
  }
}

@media screen and (min-width: 1024px) {
  .content {
    background: linear-gradient(
      65deg,
      transparent 27%,
      #ddf1f2 27.1% 76.7%,
      transparent 76.8%
    );
  }
}
</style>
