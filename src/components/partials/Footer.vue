<template>
  <footer
    class="site-footer bg-white text-black flex items-center text-center justify-between justify-center flex-wrap pt-5 lg:pt-10 flex-col"
  >
    <div id="social-icons" class="mb-5 w-full flex flex-row justify-center">
      <a
        href="https://www.facebook.com/CauseforceLLC"
        rel="nofollow"
        class="m-4"
        target="_blank"
        alt="Our Facebook page"
        title="Visit our facebook page"
      >
        <svg
          id="Facebook"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="#000"
        >
          <rect id="Padding" width="24" height="24" fill="none" />
          <path
            id="Facebook-2"
            data-name="Facebook"
            d="M47.592,266h5.639v-14.12h3.933l.42-4.727H53.231v-2.692c0-1.114.224-1.555,1.3-1.555h3.051V238h-3.9c-4.2,0-6.088,1.847-6.088,5.384v3.769H44.66v4.787h2.932Z"
            transform="translate(-36.785 -237.996)"
          />
        </svg>
      </a>

      <a
        href="https://www.linkedin.com/company/causeforce"
        rel="nofollow"
        class="m-4"
        target="_blank"
        alt="Our LinkedIn page"
        title="Visit our linkedin page"
      >
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <path
            d="M0 0v24h24v-24h-24zm8 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.397-2.586 7-2.777 7 2.476v6.759z"
          />
        </svg>
      </a>

      <a
        href="https://www.youtube.com/channel/UCquDkiJJSOefG32WapLl88g"
        rel="nofollow"
        class="m-4"
        target="_blank"
        alt="Our YouTube channel"
        title="Visit our YouTube Channel"
      >
        <img
          src="https://causeforce.com/wp-content/uploads/2020/09/youtube.svg"
          style="max-width: 24px;"
        />
      </a>
    </div>
    <div class="mb-5 w-full justify-center">
      <div class="flex flex-column text-center justify-center lg:flex-row">
        <p
          class="text-sm font-medium tracking-widest font-black p-4 self-center text-right w-1/4 sm:w-1/5"
        >LOS ANGELES</p>
        <img
          src="https://dev.causeforce.com/wp-content/uploads/2017/11/android-chrome-384x384.png"
          alt="Causeforce Logo"
          class="w-2/4 sm:w-3/5 logo"
          style="max-height:192px;"
        />
        <p
          class="text-sm font-medium tracking-widest font-black p-4 self-center text-left w-1/4 sm:w-1/5"
        >TORONTO</p>
      </div>
    </div>
    <div class="mb-5 w-full">
      <img
        src="https://dev.causeforce.com/wp-content/uploads/2020/09/CF-Logo-Grey-update_nologo.png"
        alt="Causeforce LLC"
        class="max-w-xs justify-center my-0 mx-auto"
        style="max-height:76px; height:auto;"
      />
    </div>
    <div class="mb-0 w-full">
      <a
        href="../privacy-policy/"
        class="font-normal text-sm tracking-wider my-2 self-center text-center"
      >PRIVACY POLICY</a>
      <p
        class="font-medium text-sm tracking-wider my-2 self-center text-center"
      >&copy;2020 CauseForce&reg;. All rights reserved.</p>
      <p
        class="font-medium text-xs tracking-wider pt-5 my-2 self-center text-center italic"
      >Photo credit (below): Clark Tibbs, Unsplash</p>
    </div>
    <div id="neon-bar" class="w-full">
      <img
        class="mx-auto my-0"
        src="https://causeforce.com/wp-content/uploads/2020/09/neon-footer.png"
      />
    </div>
  </footer>
</template>

<style type="postcss" scoped>
#neon-bar {
  background: #1b6a87;
  height: 100%;
}

img.logo {
  max-width: 12rem;
}

@media screen and (max-width: 420px) {
  img.logo {
    max-width: 8rem;
  }
}
</style>
