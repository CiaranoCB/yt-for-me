<script lang="ts">
  // creates a bindinnng that let's outside 
  // components influence the state here
  export let show = true;
  export let isMobile = false;
</script>

{#if show}
    <section class="bg-slate-900">
      SideNav that should hide on small screen
    </section>
{/if}


<style>
  section {
    width: 300px;
  }
</style>