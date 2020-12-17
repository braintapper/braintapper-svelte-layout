<script lang="coffeescript">

  export top = "0"
  export width = "200px"
</script>

<style lang="sass">

  nav
    position: fixed
    height: 100%

    bottom: 0



</style>
<nav style="width: {width}; top: {top}">
  <slot name="nav"/>
</nav>
<main style="margin-left: {width}">
  <slot/>
</main>
