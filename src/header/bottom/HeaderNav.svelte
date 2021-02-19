<nav>
    <ul>
        <HeaderNavDropdown/>
    </ul>
</nav>

<script>
    import HeaderNavDropdown from "./HeaderNavDropdown.svelte";
</script>

<style type="text/scss">
  nav {
    padding-right: 40px;

    ul {
      //line-height: 0;
      margin: 0 -30px;

    }
  }
  @media only screen and (max-width: 992px) {
    nav {
      display: none;
    }
  }
</style>