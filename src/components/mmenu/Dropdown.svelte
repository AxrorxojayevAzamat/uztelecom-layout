{#each menu_items as item}
    <li class="nav-item">
        <a href="">{item.name}
            {#if item.children}<span class="fa fa-angle-down"></span>{/if}
        </a>
        {#if item.children}
            <ul class="second-dropdown">
                {#each item.children as child}
                    <li class="second-dropdown-item">
                        <a href="">{child.name}
                            {#if child.children}<span class="fa fa-angle-down"></span>{/if}
                        </a>
                        {#if child.children}
                            <ul class="third-dropdown">
                                {#each child.children as nephew}
                                    <li class="third-dropdown-item">
                                        <a href="">{nephew.name}</a>
                                    </li>
                                {/each}
                            </ul>
                        {/if}
                    </li>
                {/each}
            </ul>
        {/if}
    </li>
{/each}

<script>
    export let menu_items = []
</script>

<style type="text/scss">
    li.menu-item {
      position: relative;
      list-style: none;
      display: block;
      vertical-align: middle;
      a {
        display: block;
        padding: 10px;
        font: 500 16px/22px Montserrat,sans-serif;
        color: #212f3d;
        text-decoration: none;
        transition: color .25s ease 0s;
      }
      ul.second-dropdown {
        display: none;
        border-top: 0;
        padding: 0;
        margin: 0;
        background-color: #fff;
        box-shadow: none;
        position: relative;
        min-height: 0;
        height: auto;
        overflow: hidden;
        li.second-dropdown-item {
          display: block;
          border-bottom: 1px solid #f1f8ff;
          border-radius: 6px;
          position: static;
          transition: all .25s ease 0s;
          &.active {
            a {
              background-color: #228bd6;
              color: #fff;
            }
          }
          a {
            font: 500 14px/14px Montserrat,sans-serif;
            color: #212f3d;
            text-decoration: none;
            min-width: auto;
            padding: 10px 15px;
            border-radius: 5px;
            position: relative;
          }
          ul.third-dropdown {
            padding: 10px 15px;
            position: relative;
            left: 0;
            top: 0;
            background-color: #fff;
            display: none;
            li.third-dropdown-item {
              padding: 10px 15px;
              position: relative;
              left: 0;
              top: 0;
              background-color: #fff;
              display: none;

            }
          }
        }
      }
    }
</style>