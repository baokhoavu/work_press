<template>
  <section id="cf-vision">
    <div class="content flex px-0 md:px-2 lg:px-6 xl:px-10">
      <div class="w-0 lg:w-1/5"></div>
      <div class="w-full lg:w-3/5 text-center px-4 lg:px-0 py-2 sm:py-4 md:py-6 lg:py-8 xl:py-10">
        <h1
          class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl font-bold leading-none text-black my-10 tracking-wide"
        >
          We see your
          <span class="gradient-highlight">vision.</span>
        </h1>
        <p class="text-base md:text-lg lg:text-xl xl:text-2xl font-normal text-black">
          Imagine a world where you have everything you need to make a difference.
          CauseForce has the expertise to make your vision a reality with our impactful
          peer-to-peer fundraising solutions and technologies designed to engage
          supporters in an ever-changing world.
        </p>
        <div class="pt-0 md:pt-3 lg:pt-5">
          <a
            href="#cf-form"
            class="inline-block text-sm px-3 py-4 lg:px-6 lg:py-5 leading-none border text-white font-bold bg-cfteallight-100 border-cfteallight-100 hover:text-cfteallight-100 hover:bg-white mt-4 lg:mt-0 tracking-widest shadow-lg"
          >LET'S CHANGE THE WORLD</a>
        </div>
      </div>
      <div class="w-0 lg:w-1/5"></div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style type="postcss" scoped>
.content {
  position: relative;
  max-height: 720px;
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  height: auto !important;
}

.gradient-highlight {
  background: linear-gradient(
    transparent 52%,
    #ddf1f2 52% 85%,
    transparent 85% 100%
  );
}

.lg\:self-center {
  padding-bottom: 0;
}

p.text-2xl {
  line-height: 1.75rem;
}
</style>
