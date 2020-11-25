<template>
  <section id="cf-us">
    <div class="content flex flex-wrap flex-column px-0 md:px-2 lg:px-6 xl:px-10">
      <div class="mb-10 absolute hidden bottom-0 lg:block">
        <img
          class="ml-16"
          src="https://dev.causeforce.com/wp-content/uploads/2020/09/Yellow_circle.png"
        />
      </div>
      <div class="flex flex-wrap pt-5 my-5 content-center sm:content-end sm:justify-center">
        <div class="w-1/3 px-8 hidden lg:block lg:self-end lg:mb-24">
          <div class="pl-4 lg:pl-32">
            <h1 class="text-5xl font-bold leading-none text-black tracking-wide">
              Our
              <br />strength
              <br />is epic
              <br />impact
            </h1>
          </div>
        </div>
        <div class="w-full lg:w-2/3 px-8 lg:self-center">
          <div class="w-3/4 mx-auto">
            <img
              class="mb-3 sm:mb-6 lg:mb-10 shadow-xl"
              src="https://dev.causeforce.com/wp-content/uploads/2020/09/CF_TEAM-SIGNS.png"
              style="max-width: 100%;"
            />
          </div>
          <div class="block justify-center mb-3 md:mb-6 lg:hidden">
            <h1
              class="text-3xl md:text-4xl lg:text-5xl font-bold leading-none text-black tracking-wide text-center"
            >Our strength is epic impact</h1>
          </div>
          <div
            class="align-center flex flex-wrap justify-center lg:justify-end lg:mx-10 w-3/4 mx-auto"
          >
            <img
              src="https://dev.causeforce.com/wp-content/uploads/2020/09/CF-Logo-Grey-update_nologo.png"
              alt="Causeforce LLC"
              class="mb-3 sm:mb-0 max-w-xs lg:max-w-sm logo"
              style="max-height: 92px;"
            />
            <img
              class="cf-infi"
              src="https://causeforce.com/wp-content/themes/cf_v2/assets/images/Group-236.svg"
              alt="Logo"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style type="postcss" scoped>
#cf-us {
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

.cf-infi {
  max-width: 50px;
}

@media screen and (max-width: 420px) {
  img.logo {
    max-width: 100% !important;
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
