<script>
  import Logo from './Logo.svelte'
</script>

<footer>
  <div
    id="contact"
    class="flex flex-col justify-center items-center bg-cstm-primary-dark-moderate-cyan bg-opacity-70 px-6 py-10 gap-10"
  >
    <div class="md:scale-150">
      <Logo fillColor="#25564b" />
    </div>
    <ul
      class="w-full flex justify-around items-center font-barlow text-cstm-primary-dark-desaturated-cyan md:max-w-xs"
    >
      <li class="md:hover:text-white"><a href="/#about">About</a></li>
      <li class="md:hover:text-white"><a href="/#services">Services</a></li>
      <li class="md:hover:text-white"><a href="/#projects">Projects</a></li>
    </ul>
    <div class="flex items-center gap-8">
      <a href="/#" class="w-full hover:-translate-y-1 transition-all">
        <img
          src="/assets/icon-facebook.svg"
          alt="facebook icon"
          class="w-full"
        />
      </a>
      <a href="/#" class="w-full hover:-translate-y-1 transition-all">
        <img
          src="/assets/icon-instagram.svg"
          alt="instagram icon"
          class="w-full"
        />
      </a>
      <a href="/#" class="w-full hover:-translate-y-1 transition-all">
        <img src="/assets/icon-twitter.svg" alt="twitter icon" class="w-full" />
      </a>
      <a href="/#" class="w-full hover:-translate-y-1 transition-all">
        <img
          src="/assets/icon-pinterest.svg"
          alt="pinterest icon"
          class="w-full"
        />
      </a>
    </div>
  </div>
  <div
    class="bg-cstm-primary-dark-moderate-cyan bg-opacity-70 px-6 pb-1 text-sm font-barlow text-center"
  >
    Challenge by <a
      href="https://www.frontendmentor.io?ref=challenge"
      target="_blank"
      class="underline">Frontend Mentor</a
    >. Coded by
    <a href="https://github.com/waleedmumtaz" target="_blank" class="underline"
      >Waleed Mumtaz</a
    >.
  </div>
</footer>
