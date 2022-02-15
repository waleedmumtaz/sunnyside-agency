<script>
  import { slide } from 'svelte/transition'
  import Logo from './Logo.svelte'

  let isNavOpen = false

  const toggleNav = () => {
    isNavOpen = !isNavOpen
  }
</script>

<header>
  <!-- mobile nav -->
  <div class="md:hidden relative">
    <img
      src="/assets/mobile/image-header.jpg"
      alt="half sliced orange with blue background"
      class="w-full"
    />
    <div class="w-full absolute inset-0 px-6 pt-8">
      <nav class="flex justify-between items-center relative">
        <Logo />
        <button
          on:click|preventDefault={toggleNav}
          class={`${isNavOpen ? 'opacity-50' : ''} relative z-20`}
        >
          <img src="/assets/icon-hamburger.svg" alt="hamburger menu" />
        </button>
        {#if isNavOpen}
          <div
            transition:slide
            class={`${
              isNavOpen
                ? 'absolute top-16 w-full text-center font-barlow py-10 z-10'
                : 'hidden'
            } bg-white`}
          >
            <div class="relative">
              <ul class="text-cstm-neutral-dark-grayish-blue text-xl space-y-8">
                <li><a href="/#about">About</a></li>
                <li><a href="/#services">Services</a></li>
                <li><a href="/#projects">Projects</a></li>
                <li
                  class="bg-cstm-primary-yellow text-cstm-neutral-very-dark-desaturated-blue w-fit mx-auto rounded-full px-8 py-4 uppercase font-fraunces font-bold text-base"
                >
                  <a href="/#contact"> Contact </a>
                </li>
              </ul>
              <div
                class="w-6 overflow-hidden inline-block absolute -top-[6.5rem] right-0"
              >
                <div
                  class="h-16 bg-white rotate-45 transform origin-bottom-left"
                />
              </div>
            </div>
          </div>
        {/if}
      </nav>
    </div>
    <div
      class="absolute inset-0 px-6 flex flex-col justify-center items-center gap-16 text-white font-fraunces text-center"
    >
      <h1 class="uppercase text-5xl">We are creatives</h1>
      <img src="/assets/icon-arrow-down.svg" alt="down pointing arrow" />
    </div>
  </div>

  <!-- desktop nav -->
  <div class="hidden md:block relative">
    <img
      src="/assets/desktop/image-header.jpg"
      alt="half sliced orange with blue background"
    />
    <div class="absolute inset-0 px-10 pt-12">
      <nav class="flex justify-between items-center relative z-10">
        <div class="scale-125 origin-left">
          <Logo />
        </div>
        <ul
          class="flex justify-between items-center space-x-16 font-barlow text-white"
        >
          <li><a href="/#about">About</a></li>
          <li><a href="/#services">Services</a></li>
          <li><a href="/#projects">Projects</a></li>
          <li>
            <a
              href="/#contact"
              class="bg-white hover:bg-opacity-25 text-cstm-neutral-very-dark-desaturated-blue hover:text-white transition-all w-fit mx-auto rounded-full px-8 py-4 uppercase font-fraunces font-bold text-base"
              >Contact</a
            >
          </li>
        </ul>
      </nav>
    </div>
    <div
      class="absolute inset-0 px-6 flex flex-col justify-center items-center gap-16 md:gap-10 text-white font-fraunces text-center"
    >
      <h1 class="uppercase text-6xl tracking-widest">We are creatives</h1>
      <img src="/assets/icon-arrow-down.svg" alt="down pointing arrow" />
    </div>
  </div>
</header>
