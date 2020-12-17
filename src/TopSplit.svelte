<script lang="coffeescript">

  export headerSize = "100px"
  export footerSize = "100px"
  export contentScrollable = true
  export header = true
  export footer = true

  `$: contentStyle = contentScrollable ? "overflow-y: scroll" : "overflow-y: hidden"`

</script>

<style lang="sass">
  main
    width: 100%
    height: 100%
    overflow: hidden

  section
    overflow-x: hidden

  header, footer
    overflow: visible




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
