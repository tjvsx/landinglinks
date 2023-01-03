<script>
  import pic from '$lib/assets/pic.jpg'

  /**
	 * @type {any}
	 */
   export let link;
</script>

<a href={link}>
  <section>
    <img alt="profile_picture" src={pic} />
    <h1>TJ VanSlooten ⚽️ 👨🏻‍💻</h1>
  </section>
</a>

<style>
  section {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
  img {
    height:7em;
    width:7em;
    border-radius: 50%;
  }
  h1 {
    font-size: x-large;
  }
  a {
    z-index: 999;
  }
</style>

<!-- 

  TODO:
- on click profile, open bio
 -->