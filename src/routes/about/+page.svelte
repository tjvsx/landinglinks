<script>
	import About from '$lib/components/About.svelte';
  import Background from '$lib/components/Background.svelte';
	import Footer from '$lib/components/Footer.svelte';
  import Links from '$lib/components/Links.svelte'
	import Profile from '$lib/components/Profile.svelte';

  let link = '/'
</script>

<main>
  <Background />
  <div>
    <section>
      <Profile {link} />
      <About />
    </section>
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
  div {
    height: 100vh;
    display: flex;
    flex-direction: column;
    width: 100%;
    flex-basis: auto;
    max-width: 40em;
    padding:2.5em 0;
  }

</style>