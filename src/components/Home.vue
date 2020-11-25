<template>
  <div class="page page--home">
    <section-intro />
    <section-impact />
    <section-solutions />
    <section-experiences />
    <section-videos />
    <section-testimonial />
    <section-us />
    <section-vision />
    <section-form />
    <!-- <recent-posts-widget limit="5" class="mb-10"
      >Recent Posts</recent-posts-widget
    >
    <pages-widget limit="5">Pages</pages-widget>-->
  </div>
</template>

<script>
import RecentPostsWidget from "./widgets/RecentPosts.vue";
import PagesWidget from "./widgets/Pages.vue";
import SectionIntro from "./partials/home-sections/SectionIntro.vue";
import SectionImpact from "./partials/home-sections/SectionImpact.vue";
import SectionSolutions from "./partials/home-sections/SectionSolutions.vue";
import SectionExperiences from "./partials/home-sections/SectionExperiences.vue";
import SectionForm from "./partials/home-sections/SectionForm.vue";
import SectionTestimonial from "./partials/home-sections/SectionTestimonial.vue";
import SectionUs from "./partials/home-sections/SectionUs.vue";
import SectionVision from "./partials/home-sections/SectionVision.vue";
import SectionVideos from "./partials/home-sections/SectionVideo.vue";

var fadeInElements = [];

export default {
  components: {
    RecentPostsWidget,
    PagesWidget,
    sectionIntro: SectionIntro,
    sectionImpact: SectionImpact,
    sectionSolutions: SectionSolutions,
    sectionExperiences: SectionExperiences,
    sectionForm: SectionForm,
    sectionTestimonial: SectionTestimonial,
    sectionUs: SectionUs,
    sectionVision: SectionVision,
    sectionVideos: SectionVideos
  },
  methods: {
    isElementVisible: function(el) {
      var rect = el.getBoundingClientRect();
      var elemTop = rect.top + 300; // 300 px buffer
      var elemBottom = rect.bottom;
      return elemTop < window.innerHeight && elemBottom >= 0;
    },
    handleScroll: function(event) {
      for (var i = 0; i < fadeInElements.length; i++) {
        var elem = fadeInElements[i];
        if (this.isElementVisible(elem)) {
          elem.style.opacity = "1";
          // elem.style.transform = "scale(1)";
          elem.style.transform = "translateY(0px)";
          fadeInElements.splice(i, 1); // only allow it to run once
        }
      }
    }
  },
  mounted() {
    this.$nextTick(function() {
      // console.log("next tick fired");
      fadeInElements = Array.from(document.getElementsByClassName("fade-in"));
      // console.log(fadeInElements);
      document.addEventListener("scroll", this.handleScroll);

      // move contact form
      document
        .getElementById("cf-form-holder")
        .appendChild(document.getElementById("wpcf7-f89-o1"));
    });
  }
};
</script>

<style type="postcss">
.page--home {
  width: 100%;
  margin: 0 auto;
}

.fade-in {
  opacity: 0;
  transition: 0.3s all ease-out;
  transform: translateY(-10px);
}
</style>
