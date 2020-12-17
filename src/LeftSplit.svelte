<script lang="coffeescript">

  

  export contentScrollable = true

  export navWidth = "56px"

  export navClasses = undefined
  export contentClasses = undefined

  `$: contentStyle = contentScrollable ? "overflow-y: scroll" : "overflow-y: hidden"`

</script>

<style lang="sass">
  main
    width: 100%
    min-width: 700px
    height: 100%
    overflow: hidden
    display: flex
    flex-direction: row

    nav
      height: 100%
      overflow-y: hidden
      overflow: visible
      flex: 0 1 auto
    section
      height: 100%
      width: 100%
      overflow-x: hidden
      overflow-y: auto
      flex: 1
      box-sizing: border-box
      max-height: 100%




</style>

<main>
  <nav class={navClasses} style="width: {navWidth}"><slot name="nav">nav</slot></nav>
  <section class={contentClasses}><slot>content</slot></section>
</main>
