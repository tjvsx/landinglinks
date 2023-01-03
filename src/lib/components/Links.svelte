<script>
// @ts-nocheck

const links = [
  {
    title: '0xpm', 
    url: 'https://0xpm.app'
  },
  {
    title: 'EIP-2535 Diamonds ~ Contributor',
    url: 'https://eip2535diamonds.substack.com/p/contributors-to-eip2535-diamonds'
  },
  {
    title: 'Medium', 
    url: 'https://medium.com/@tjvs'
  },
  {
    title: 'GitHub', 
    url: 'https://github.com/tjvsx'
  },
  {
    title: 'Twitter', 
    url: 'https://twitter.com/tjvsx'
  },
  {
    title: 'Blog', 
    url: 'https://tjvanslooten.github.io'
  },
  {
    title: 'Habitat DAO ~ Core Dev', 
    url: 'https://0xhabitat.org/'
  }
]
</script>

<main>
  <section>
    {#each links as {url, title}}
    <a href={url} target='_blank'>
      <div>
        {title}
      </div>
    </a>
    {/each}
  </section>
</main>


<style>
  main {
    position: relative;
    overflow: scroll;
    height: 100%;
    width: 100%;
    mask-image: linear-gradient(180deg, transparent 5%, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 1) 50%, transparent 95%);
    -webkit-mask-image: linear-gradient(180deg, transparent 5%, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 1) 50%, transparent 95%);
    -ms-overflow-style: none;  /* IE and Edge */
    scrollbar-width: none;  /* Firefox */
    z-index: 999;
  }
  section {
    padding:2em;
    position: absolute;
    display: flex;
    flex-direction: column;
    gap: 1em;
    border-radius: 1em;
    width: 100%;
    padding-bottom: 10em;
  }
  main::-webkit-scrollbar {
    display: none;
  }
  div {
    width:100%;
    /* background: rgb(255, 255, 255, 0.9); */
    border: 1px solid;
    align-items: center;
    justify-content: center;
    display: flex;
    height:3em;
    border-radius: .5em;
    transition: 200ms;
    font-size: large;
    background: aliceblue;
    box-shadow: 0 0 5px rgb(100, 100, 100);
  }
  div:hover {
    scale: 1.01;
    transition: 200ms;
  }
  
</style>