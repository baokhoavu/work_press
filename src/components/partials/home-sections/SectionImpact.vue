<template>
  <section id="cf-impact">
    <div class="content flex px-0 md:px-2 lg:px-6 xl:px-10">
      <div class="right-0 absolute show hidden md:block lg:hidden" style="top: -6rem; right: 5rem;">
        <img
          class="max-w-3/4"
          src="https://dev.causeforce.com/wp-content/uploads/2020/09/Photo_girls_hugging.png"
        />
      </div>
      <div class="left-0 bottom-0 absolute hidden md:block" style>
        <img src="https://causeforce.com/wp-content/uploads/2020/09/bigyellow-aboutsection.png" />
      </div>
      <div class="right-0 top-0 absolute show hidden xl:block" style="top: 20%; right:18%;">
        <img
          class="cf-infi"
          src="https://causeforce.com/wp-content/themes/cf_v2/assets/images/Group-236.svg"
          alt="Logo"
        />
      </div>
      <div class="w-1/8 sm:w-1/5 md:w-1/4 xl:w-1/4 self-center">
        <img
          class="my-0 mr-0 ml-auto hidden lg:block"
          src="https://dev.causeforce.com/wp-content/uploads/2020/09/Photo_girls_hugging.png"
        />
      </div>
      <div
        class="w-6/8 sm:w-3/5 md:w-2/4 xl:w-2/4 px-4 sm:px-2 md:px-4 lg:px-6 ml-0 xl:ml-24 self-center text-center lg:text-left"
      >
        <h1
          class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl font-bold leading-none text-black mb-3 md:mb-5 tracking-wide"
        >
          We
          <br />deliver
          <br />epic
          <span class="gradient-highlight bg-opacity-50">impact.</span>
        </h1>
        <p class="text-base md:text-lg lg:text-xl font-normal text-black">
          Our mission is to deliver impactful fundraising
          solutions to organizations who strive to make the
          world a better place.
        </p>
        <p class="text-base md:text-lg lg:text-xl font-normal text-black text-left">
          <span class="font-bold">18 years</span> experience.
          <br />
          <span class="font-bold">165 fundraising programs</span> with global impact.
          <br />
          <span class="font-bold">Over $1 billion in donations</span> raised for our clients.
        </p>
        <p class="text-base md:text-lg lg:text-xl font-normal text-black xl:pr-3">
          We are the industry leading peer-to-peer fundraising
          agency. Let us help build a strong community of
          supporters for your cause and raise the funds you
          need to do the important work you love.
        </p>
        <div>
          <a
            href="#cf-vision"
            class="inline-block text-sm px-6 py-5 leading-none border text-white font-bold bg-teal-500 border-teal-500 hover:border-teal-500 hover:text-teal-500 hover:bg-white lg:mt-4 xl:mt-0 tracking-widest shadow-lg"
          >WORK WITH US</a>
        </div>
      </div>
      <div class="w-1/8 sm:w-1/5 md:w-1/4 xl:w-1/4"></div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style type="postcss" scoped>
#cf-impact {
  background: #ddf1f2;
  max-height: 720px;
}

.absolute {
  z-index: -1;
}
.absolute.show {
  z-index: 999;
}

.cf-infi {
  max-width: 100px;
  width: fit-content;
  height: auto;
}

.content {
  position: relative;
  height: 600px;
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  background: linear-gradient(
    65deg,
    #ddf1f2 22%,
    white 22.1% 81.7%,
    #ddf1f2 81.8%
  );
}

p.text-xl {
  line-height: 1.75rem;
}
.gradient-highlight {
  background: linear-gradient(
    transparent 52%,
    #ddf1f2 52% 85%,
    transparent 85% 100%
  );
}

@media screen and (min-width: 1024px) {
  .content {
    background: linear-gradient(
      65deg,
      #ddf1f2 27%,
      white 27.1% 76.7%,
      #ddf1f2 76.8%
    );
  }
}
</style>
