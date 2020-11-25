<template>
  <nav
    class="site-header flex items-center justify-between flex-wrap bg-teal-500 py-2 px-2 xl:pb-0 xl:pt-6 xl:px-10"
  >
    <div class="site-header__interior flex items-center flex-shrink-0 text-white mr-6">
      <router-link to="/">
        <img
          src="https://dev.causeforce.com/wp-content/uploads/2020/09/CF-Logo-Grey-update_nologo.png"
          alt="Causeforce LLC"
          class="w-0 sm:w-full sm:max-w-xs"
          style="max-width: 15rem; max-height: 57px; align-self: center;"
        />
        <img
          class="cf-infi"
          src="https://causeforce.com/wp-content/themes/cf_v2/assets/images/Group-236.svg"
          alt="Logo"
        />
      </router-link>
    </div>
    <div id="mobile-nav-wrapper" class="block relative xl:hidden">
      <button
        class="flex items-center px-3 py-2 border rounded text-black border-cfblue-100 hover:border-white"
        @click="show = !show"
      >
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button>
      <ul id="mobile-nav" class="absolute right-0 self-start" v-if="show">
        <li
          class="items-center cursor-pointer flex text-sm justify-center list-none bg-white px-1 py-1 border border-solid border-cfblue-100"
          v-for="(item,index) in items"
          :key="index"
          @click="scroll(item.destination)"
        >{{ item.title }}</li>
      </ul>
    </div>
    <div
      id="desktop-nav-wrapper"
      class="w-full block flex-grow justify-end hidden xl:flex lg:items-center lg:w-auto"
    >
      <div class="text-sm font-bold xl:flex-grow">
        <a href="#cf-about" class="block mt-4 lg:inline-block lg:mt-0 text-black mr-6">About</a>
        <a href="#cf-solutions" class="block mt-4 lg:inline-block lg:mt-0 text-black mr-6">Services</a>
        <a
          href="#cf-experiences"
          class="block mt-4 lg:inline-block lg:mt-0 text-black mr-6"
        >Experiences</a>
        <a
          href="#cf-testimonial"
          class="block mt-4 lg:inline-block lg:mt-0 text-black mr-6"
        >Client Love</a>
        <a href="#cf-vision" class="block mt-4 lg:inline-block lg:mt-0 text-black">Contact</a>
      </div>
      <div>
        <a
          href="#cf-vision"
          class="inline-block font-bold text-sm px-6 py-5 leading-none border text-white bg-cfteal-100 border-cfteal-100 hover:text-cfteal-100 hover:bg-white mt-4 lg:mt-0 tracking-widest"
        >WORK WITH US</a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "About", destination: "cf-about" },
        { title: "Services", destination: "cf-solutions" },
        { title: "Experiences", destination: "cf-experiences" },
        { title: "Client Love", destination: "cf-testimonial" },
        { title: "Contact", destination: "cf-vision" }
      ],
      show: false
    };
  },
  methods: {
    scroll: function(destination) {
      var element = document.getElementById(destination);
      element.scrollIntoView();
    }
  }
};
</script>

<style type="postcss" scoped>
nav {
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
}

ul#mobile-nav {
  z-index: 999;
}

#mobile-nav li {
  transition: all 0.3s ease;
}

a.router-link-active {
  display: flex;
}

.cf-infi {
  max-width: 50px;
  margin-left: 10px;
}

.flex-grow,
.lg\:flex-grow {
  flex-grow: 0.2;
}

.logo-cls-1 {
  fill: #ffffff;
}

.site-header {
  background: #fff;
}

.tracking-widest {
  letter-spacing: 0.2rem;
}
</style>
