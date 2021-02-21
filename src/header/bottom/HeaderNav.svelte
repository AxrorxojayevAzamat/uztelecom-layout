<nav>
    <ul>
        <HeaderNavDropdown/>
    </ul>
    <HeaderSearch {show_search}/>
</nav>
<a href="#" class="searchBtn" on:click={() => {show_search = !show_search}}>
    <span class="fas fa-{show_search ? 'times' : 'search'}"></span>
</a>
<div class="hamburger">
    <Hamburger/>
</div>

<script>
    import HeaderNavDropdown from "./HeaderNavDropdown.svelte";
    import HeaderSearch from "./HeaderSearch.svelte";
    import Hamburger from "../../components/Hamburger.svelte";

    let show_search = false

</script>

<style type="text/scss">
  nav {
    padding-right: 55px;

    ul {
      //line-height: 0;
      margin: 0 -30px;

      @media only screen and (max-width: 992px) {
        display: none;
      }
    }
  }

  .searchBtn {
    text-decoration: none;
    display: inline-block;
    padding-left: 0;
    position: absolute;
    right: 0;
    @media only screen and (max-width: 1500px) {
      padding-left: 0;
      right: 25px;
    }
    @media only screen and (max-width: 1240px) {
      padding-left: 0;
      right: 20px;
    }
    @media only screen and (max-width: 992px) {
      right: 60px;
    }

    span {
      font-size: 16px;
      color: #212f3d;
    }
  }

  .hamburger {
    display: none;
    padding: 15px 0 6px 15px;
    @media only screen and (max-width: 992px) {
      display: block;
    }
  }

</style>