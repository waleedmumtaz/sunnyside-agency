<script>
  import Footer from './lib/Footer.svelte'
  import Header from './lib/Header.svelte'
  import MainContent from './lib/MainContent.svelte'
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link
    rel="preconnect"
    href="https://fonts.gstatic.com"
    crossorigin="anonymous"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Barlow:wght@600&family=Fraunces:wght@700;900&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<div class="min-h-screen">
  <Header />
  <MainContent />
  <Footer />
</div>
