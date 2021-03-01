<script>
    import Icons from "./mmenu/Icons.svelte";
    import Menu from "./mmenu/Menu.svelte";
    import MainMenu from "./mmenu/MainMenu.svelte";

</script>

<input type="checkbox" id="mobile_menu" name="mobilemenu">
<i class="overlayForMobileMenu"></i>
<div class="mobileMenu">
    <div class="wraps">
        <Icons/>
        <Menu/>
        <MainMenu/>
    </div>
</div>
<label class="hamburger-btn" for="mobile_menu">
    <svg width=28 height=21>
        <line id="top" x1=0 y1=5 x2=32 y2=5/>
        <line id="middle" x1=0 y1=12 x2=32 y2=12/>
        <line id="bottom" x1=0 y1=19 x2=32 y2=19/>
    </svg>
</label>

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
  }

  #mobile_menu:checked ~ .overlayForMobileMenu {
    opacity: 1;
    visibility: visible;
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
    .wraps {
      padding: 15px;
      margin-bottom: 100px;
      height: 90%;
      overflow: auto;
    }
  }

  #mobile_menu:checked ~ .mobileMenu {
    left: 0;
  }


  svg {
    min-height: 24px;
    transition: transform 0.3s ease-in-out;

    line {
      stroke: currentColor;
      stroke-width: 2;
      transition: transform 0.3s ease-in-out;
      color: #228bd6;
    }
  }

  //button {
  //  z-index: 20;
  //  border: none;
  //  background-color: #fff;
  //
  //  &:focus {
  //    outline: none;
  //  }
  //}

  #mobile_menu:checked ~ .hamburger-btn {
    position: absolute;
    z-index: 999998;
    right: 10px;
    top: 10px;
    line {
      transform: scale(1.35)
    }

    #top {
      transform: translate(4px, -1px) rotate(40deg)
    }

    #middle {
      opacity: 0;
    }

    #bottom {
      transform: translate(-11px, 9px) rotate(-40deg)
    }
  }

  #mobile_menu {
    display: none;
  }
</style>