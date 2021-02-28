

<div class="leftSideDropdown">
    <div class="wraps">
        <div class="sideBarMenuAccordion">
            <nav>
                <ul>
                    {#each menu_items as item, i}
                        <!--FIRST-->
                        <li class="{item.children && 'dropdown'}" class:active='{item.open}'>
                            <a href="#">{item.name}</a>

                            {#if item.children}

                                {#if item.open}
                                    <ul transition:slide={{duration: 700}}>
                                        {#each item.children as child, j}
                                            <!--SECOND-->
                                            <li class="{child.children && 'dropdown'}"
                                                class:active='{child.open}'>
                                                <a href="#">{child.name}</a>
                                                {#if child.children}
                                                    {#if child.open}
                                                        <ul transition:slide={{duration: 700}}>
                                                            {#each child.children as nephew}
                                                                <!--THIRD-->
                                                                <li>
                                                                    <a href="#">{nephew.name}</a>
                                                                </li>
                                                            {/each}
                                                        </ul>
                                                    {/if}
                                                    <span class="fa fa-angle-{ child.open ? 'up' : 'down'}"
                                                          on:click={e => { dropdown(menu_items[i].children, j)}}></span>
                                                {/if}
                                            </li>
                                        {/each}
                                    </ul>
                                {/if}
                                <span class="fa fa-angle-{ menu_items[i].open ? 'up' : 'down'}"
                                      on:click={e => {dropdown(menu_items, i)}}></span>
                            {/if}
                        </li>
                    {/each}
                </ul>
            </nav>
        </div>
    </div>
</div>

<script>
    import {slide} from 'svelte/transition';
    import {navItems} from "../header/bottom/navItem";

    export let menu_items = navItems

    function dropdown(items, index) {
        items.forEach((it, i) => {
            it.open = (i === index) ? !it.open : false
        })
        menu_items = menu_items
    }

</script>

<style type="text/scss">


  .leftSideDropdown {
    display: inline-block;
    vertical-align: top;
    width: 25%;

    .wraps {
      padding: 0 30px 0 0;

      .sideBarMenuAccordion {
        nav {
          ul {
            li {
              border-top: 1px solid #e8f0f8;
              list-style: none;

              a {
                display: block;
                padding: 15px 40px 15px 0;
                font: 500 18px/20px Montserrat, sans-serif;
                color: #212f3d;
                text-decoration: none;
                transition: color .25s ease 0s;

                &:hover {
                  color: #228bd6;
                }
              }

              ul {
                li {
                  border: 0;

                  a {
                    display: block;
                    padding: 10px 35px 10px 20px;
                    font: 400 16px/18px Montserrat, sans-serif;
                    color: #8d959d;
                    text-decoration: none;
                    position: relative;
                    transition: color .25s ease 0s;
                  }

                }

                li > span {
                  span {
                    top: 0;
                    padding: 12px;
                    right: 7px;
                    font-size: 10px;
                  }
                }
              }
            }

            li > span {
              position: absolute;
              top: 0;
              right: 0;
              font-size: 14px;
              color: #8d959d;
              display: inline-block;
              padding: 18px;
              cursor: pointer;
            }

            li.dropdown {
              position: relative;

            }

            li.active {
              a {
                color: #228bd6;

              }

              ul {
                li {
                  a {
                    color: #8d959d;

                    &:hover {
                      color: #228bd6;
                    }
                  }

                  &.active {
                    a {
                      color: #228bd6;
                    }

                    ul {
                      li {
                        a {
                          color: #8d959d;

                          &:hover {
                            color: #228bd6;
                          }
                        }

                        &.active {
                          color: #228bd6;
                        }
                      }
                    }
                  }
                }
              }
            }

          }
        }
      }
    }
  }

</style>