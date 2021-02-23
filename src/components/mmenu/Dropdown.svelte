{#each menu_items as item, i}
    <!--FIRST-->
    <li class="menu-item">
        <a href="#">{item.name}</a>
        {#if item.children}
            {#if item.open}
                <ul class="dropdown-1" transition:slide={{duration: 700}}>
                    {#each item.children as child, j}
                        <!--SECOND-->
                        <li class="item-1" class:active='{child.open}'>
                            <a href="#" class="link-1">{child.name}</a>
                            {#if child.children}
                                {#if child.open}
                                    <ul class="dropdown-2" transition:slide={{duration: 700}}>
                                        {#each child.children as nephew}
                                            <!--THIRD-->
                                            <li class="item-2">
                                                <a href="#">{nephew.name}</a>
                                            </li>
                                        {/each}
                                    </ul>
                                {/if}
                                <span class="fa fa-angle-down"
                                      on:click={() => {menu_items[i].children[j].open = !menu_items[i].children[j].open}}></span>
                            {/if}
                        </li>
                    {/each}
                </ul>
            {/if}
            <span class="fa fa-angle-down" on:click={() => {menu_items[i].open = !menu_items[i].open}}></span>
        {/if}
    </li>
{/each}

<script>
    import {slide} from 'svelte/transition';

    export let menu_items = []

</script>

<style type="text/scss">
  li.menu-item {
    position: relative;
    display: block;
    vertical-align: middle;

    a {
      display: block;
      padding: 10px;
      font: 500 16px/22px Montserrat, sans-serif;
      color: #212f3d;
      text-decoration: none;
      transition: color .25s ease 0s;
    }

    ul, .dropdown-1 {
      display: block;
      border-top: 0;
      padding: 0;
      margin: 0;
      background-color: #fff;
      box-shadow: none;
      position: relative;
      min-height: 0;
      height: auto;
      overflow: hidden;

      li, .item-1 {
        display: block;
        position: relative;
        border-bottom: 1px solid #f1f8ff;
        border-radius: 6px;
        transition: all .25s ease 0s;

        a {
          font: 500 14px/14px Montserrat, sans-serif;
          color: #212f3d;
          text-decoration: none;
          min-width: auto;
          padding: 10px 15px;
          border-radius: 5px;
          position: relative;
        }

        ul, .dropdown-2 {
          display: block;
          padding: 10px 15px;
          position: relative;
          left: 0;
          top: 0;
          background-color: #fff;

          li, .item-2 {
            position: relative;
            display: block;
            border-bottom: 1px solid #f1f8ff;
            border-radius: 6px;

            a {
              font: 400 13px/18px Montserrat, sans-serif;
              color: #212f3d;
            }
          }
        }

        &.active {
          a.link-1 {
            background-color: #228bd6;
            color: #fff;
          }
        }
      }

    }

    span {
      position: absolute;
      top: 0;
      right: 0;
      font-size: 14px;
      color: #8d959d;
      margin-top: -4px;
      display: inline-block;
      padding: 18px;
      cursor: pointer;
    }
  }

</style>