<template>
  <section id="cf-videos">
    <div class="flex py-8 xl:py-10 flex-wrap">
      <div class="w-full py-5 xl:py-8 justify-center text-center">
        <h1
          class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl text-center font-bold leading-none text-white md:mb-4 lg:mb-6 xl:mb-8 tracking-wide"
        >
          We share
          <span class="gradient-highlight bg-opacity-50">success</span> stories.
        </h1>
      </div>
      <div class="w-full flex flex-wrap pb-0 md:pb-4 lg:pb-10 justify-center">
        <div class="px-5 relative fade-in xl:block">
          <img
            class="shadow-lg"
            src="https://causeforce.com/wp-content/uploads/2020/09/Video1.png"
            @click="openModal(); showVideo(0);"
          />
          <img
            class="absolute"
            src="https://causeforce.com/wp-content/uploads/2020/09/play-button.png"
            @click="openModal(); showVideo(0);"
          />
        </div>
        <div class="px-5 relative fade-in hidden xl:block">
          <img
            class="shadow-lg"
            src="https://causeforce.com/wp-content/uploads/2020/09/Video2.png"
            @click="openModal(); showVideo(1);"
          />
          <img
            class="absolute"
            src="https://causeforce.com/wp-content/uploads/2020/09/play-button.png"
            @click="openModal(); showVideo(1);"
          />
        </div>
        <div class="px-5 relative fade-in hidden xl:block">
          <img
            class="shadow-lg"
            src="https://causeforce.com/wp-content/uploads/2020/09/Video3.png"
            @click="openModal(); showVideo(2);"
          />
          <img
            class="absolute"
            src="https://causeforce.com/wp-content/uploads/2020/09/play-button.png"
            @click="openModal(); showVideo(2);"
          />
        </div>
      </div>
      <div class="w-full py-4 md:py-6 lg:py-10 justify-center text-center">
        <a
          href="https://www.youtube.com/channel/UCquDkiJJSOefG32WapLl88g"
          target="_blank"
          rel="noopener"
          class="inline-block text-sm px-6 py-5 mb-3 whitespace-no-wrap leading-none font-bold text-cfteal-100 bg-white hover:text-teal-500 mt-4 xl:mt-0 tracking-widest shadow-lg"
        >VIEW MORE</a>
      </div>
    </div>
    <div id="modal" v-on:click="closeModal">
      <span class="close cursor" v-on:click="closeModal">&times;</span>
    </div>
    <div id="gallery-wrapper">
      <div class="video-wrapper justify-center">
        <iframe
          class="self-center"
          width="560"
          height="315"
          src="https://www.youtube.com/embed/kbCWkAhYdgw?rel=0"
          frameborder="0"
          allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
      <div class="video-wrapper justify-center">
        <iframe
          class="self-center"
          width="560"
          height="315"
          src="https://www.youtube.com/embed/eqmiUgwQxV0?rel=0"
          frameborder="0"
          allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
      <div class="video-wrapper justify-center">
        <iframe
          class="self-center"
          width="560"
          height="315"
          src="https://www.youtube.com/embed/eAMhf2mudxo?rel=0"
          frameborder="0"
          allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>
  </section>
</template>

<style type="postcss" scoped>
#cf-videos {
  background: #006699;
}

.gradient-highlight {
  background: linear-gradient(
    transparent 52%,
    #05b7aa 52% 85%,
    transparent 85% 100%
  );
}

.fade-in:hover {
  cursor: pointer;
}

/* modal gallery */
#modal {
  display: none;
  position: fixed;
  z-index: 999;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background: rgba(0, 0, 0, 0.7);
  transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.3s;
  opacity: 0;
}
#modal.active {
  opacity: 1;
}

#gallery-wrapper {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  max-width: 84%;
  max-height: 84%;
  width: 84%;
  height: 84%;
  overflow: auto;
  background: #000;
  margin: auto;
  flex-direction: column;
  transition: cubic-bezier(0.075, 0.82, 0.165, 1);
}
#gallery-wrapper.active {
  opacity: 1;
}

.video-wrapper {
  display: none;
  height: 100%;
}

/* The Close Button */
.close {
  color: white;
  position: absolute;
  top: 10px;
  right: 25px;
  font-size: 35px;
  font-weight: bold;
}

img.absolute {
  bottom: 37%;
  right: 43%;
  max-width: 50px;
}
</style>

<script>
export default {
  methods: {
    /* modal functions */
    openModal: function() {
      document.getElementById("modal").style.display = "block";
      document.getElementById("gallery-wrapper").style.display = "flex";
      document.getElementById("modal").classList.add("active");
      document.getElementById("gallery-wrapper").classList.add("active");
    },
    closeModal: function() {
      document.getElementById("modal").style.display = "none";
      document.getElementById("gallery-wrapper").style.display = "none";
      document.getElementById("modal").classList.remove("active");
      document.getElementById("gallery-wrapper").classList.remove("active");
    },
    showVideo: function(n) {
      var i;
      var videos = document.querySelectorAll(".video-wrapper");
      for (i = 0; i < videos.length; i++) {
        videos[i].style.display = "none";
      }
      videos[n].style.display = "flex";
    }
  }
};
</script>