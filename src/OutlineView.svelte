<script>

  export let top = "0";
  export let width = "200px";
</script>

<style>

nav {
  position: fixed;
  height: 100%;
  bottom: 0; }

</style>
<nav style="width: {width}; top: {top}">
  <slot name="nav"/>
</nav>
<main style="margin-left: {width}">
  <slot/>
</main>
