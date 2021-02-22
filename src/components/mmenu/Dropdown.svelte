{#each menu_items as item, i}
    <li class="dropdown" class:active='{item.open === true}'> <!--FIRST-->
        <a href="#" on:click={() => {menu_items[i].open = !menu_items[i].open}}>{item.name}
            {#if item.children}<span class="fa fa-angle-down btn"></span>{/if}
        </a>
        {#if item.children}
            <ul>
                {#each item.children as child, j}
                    <li class="dropdown" class:active='{child.open === true}'>  <!--SECOND-->
                        <a href="#" on:click={() => {menu_items[i].children[j].open = !menu_items[i].children[j].open}}>{child.name}
                            {#if child.children}<span class="fa fa-angle-down btn"></span>{/if}
                        </a>
                        {#if child.children}
                            <ul>
                                {#each child.children as nephew}
                                    <li> <!--THIRD-->
                                        <a href="#">{nephew.name}</a>
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
    import {  afterUpdate } from 'svelte';
    export let menu_items = []
    afterUpdate(() => {
        console.log(menu_items)
    });
</script>

<style type="text/scss">
  li {
    list-style: none;
    display: block;
    vertical-align: middle;
    position: relative;
    &:hover {
      opacity: 1;
      visibility: visible;
      top: 0;
    }
    &.dropdown {
      position: relative;
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
        &:hover {
          color: #8d959d;
        }
      }
      .btn {
        display: inline-block;
        margin-bottom: 0;
        font-weight: 400;
        text-align: center;
        vertical-align: middle;
        touch-action: manipulation;
        cursor: pointer;
        background-image: none;
        border: 1px solid transparent;
        white-space: nowrap;
        padding: 7px 12px;
        font-size: 13px;
        line-height: 1.5384616;
        border-radius: 3px;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
      }
    }
    a {
      display: block;
      padding: 10px;
      font: 500 16px/22px Montserrat, sans-serif;
      color: #212f3d;
      text-decoration: none;
      transition: color .25s ease 0s;
    }

    ul {
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

      li {
        display: block;
        border-bottom: 1px solid #f1f8ff;
        border-radius: 6px;
        position: static;
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
        ul {
          padding: 10px 15px;
          position: relative;
          left: 0;
          top: 0;
          background-color: #fff;
          display: none;
          li {
            position: relative;
            a {
              font: 400 13px/18px Montserrat,sans-serif;
              color: #212f3d
            }

          }
        }
        &.dropdown {
          position: absolute;
          top: 0;
          right: 0;
          font-size: 14px;
          margin-top: -7px;
          color: #8d959d;
          display: inline-block;
          padding: 18px 19px;
          cursor: pointer;
          span {
            position: absolute;
            top: 0;
            right: 0;
            font-size: 14px;
            margin-top: -7px;
            color: #8d959d;
            display: inline-block;
            padding: 18px 19px;
            cursor: pointer;
          }
        }
        &.active {
          a {
            background-color: #228bd6;
            color: #fff;
          }
          ul {
            display: block;
          }
        }
      }
    }




    &.active {
      ul {
        height: auto;
        display: block;
      }
    }
  }

</style>