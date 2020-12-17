<script>

  export let headerSize = "100px";
  export let footerSize = "100px";
  export let contentScrollable = true;
  export let header = true;
  export let footer = true;

  $: contentStyle = contentScrollable ? "overflow-y: scroll" : "overflow-y: hidden";

</script>

<style>
main {
  width: 100%;
  height: 100%;
  overflow: hidden; }

section {
  overflow-x: hidden; }

header, footer {
  overflow: visible; }


</style>

<main layout="column">
  {#if header}
  <header style="height: {headerSize}" flex="initial"><slot name="header"/></header>
  {/if}
  <section flex style={contentStyle}><slot/></section>
  {#if footer}
  <footer style="height: {footerSize}"flex="initial"><slot name="footer"/></footer>
  {/if}
</main>
