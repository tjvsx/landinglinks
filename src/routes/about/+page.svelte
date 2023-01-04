<script>
	import About from '$lib/components/About.svelte';
  import Background from '$lib/components/Background.svelte';
	import Footer from '$lib/components/Footer.svelte';
  import Links from '$lib/components/Links.svelte'
	import Profile from '$lib/components/Profile.svelte';
  import Foreground from '$lib/components/Foreground.svelte';

  let link = '/'
</script>

<main>
  <Background />
  <div class='content'>
    <section>
      <Profile {link} />
      <About />
    </section>
    <div class='fg'>
      <Foreground />
    </div>
    <Footer />
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
    display: flex;
    flex-direction: column;
  }
  .content {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 40em;
    padding: 2.5em 0;
  }

</style>