<script>
	import Background from '$lib/components/Background.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Foreground from '$lib/components/Foreground.svelte';
  import Links from '$lib/components/Links.svelte'
	import Profile from '$lib/components/Profile.svelte';

  let link = '/about'
</script>

<main>
  <Background />
  <div class='content'>
    <section>
      <div class='bg' />
      <Profile {link} />
      <Links />
    </section>
    <Footer />
  </div>
  <div class='fg'>
    <Foreground />
  </div>
</main>

<style>
  main {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  section {
    width: 100%;
    height: 100%;
    position: relative;
    display: flex;
    flex-direction: column;
    z-index: 999;
  }
  .content {
    height: 100vh;
    display: flex;
    flex-direction: column;
    width: 100%;
    flex-basis: auto;
    max-width: 40em;
    padding: 2.5em 0;
    z-index: 1;
  }
  .bg {
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: -1;
    opacity: 0.9;
  }
  .fg {
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: -1;
  }
  :global(a) {
    text-decoration: none;
    color: black;
	}

</style>