<script lang="ts">
  // creates a bindinnng that let's outside 
  // components influence the state here
  export let show = true;
  export let isMobile = false;
</script>

{#if show}
    <section class="bg-slate-900" class:fixed={isMobile}>
      www.discord.com
    </section>
{/if}


<style>
  section {
    width: 300px;
    display: flex;
    height: 100dvh;
    position: fixed;
    padding-top: 64px;
    padding-left: 8px;
    padding-right: 8px;
    z-index: 50;
    top: 0;
  }
</style>