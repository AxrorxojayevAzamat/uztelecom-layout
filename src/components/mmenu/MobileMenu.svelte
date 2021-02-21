<script>
    import {open} from "../mobile-menu";
    import Icons from "./Icons.svelte";
    import Menu from "./Menu.svelte";
    import MainMenu from "./MainMenu.svelte";

    let show
    open.subscribe(value => {
        show = value
    })
</script>

<i class="overlayForMobileMenu" class:active='{show}' on:click={() => { open.update( o => !o)}}></i>
<div class="mobileMenu" class:active='{show}'>
    <div class="wraps">
        <Icons/>
        <Menu/>
        <MainMenu/>
    </div>
</div>

<style type="text/scss">
  .overlayForMobileMenu {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 99999;
    background-color: rgba(33, 47, 61, .8);
    opacity: 0;
    visibility: hidden;
    transition: all .35s ease 0s;

    &.active {
      opacity: 1;
      visibility: visible;
    }
  }

  .mobileMenu {
    position: fixed;
    top: 0;
    width: 100%;
    max-width: 280px;
    height: 100%;
    z-index: 999991;
    background-color: #f1f8ff;
    left: -100%;
    box-shadow: 0 3px 15px 0 rgba(33, 47, 61, 0.5);
    transition: all .35s ease 0s;

    &.active {
      left: 0;
    }
    .wraps {
      padding: 15px;
      margin-bottom: 100px;
      height: 90%;
      overflow: auto;
    }
  }
</style>