{#each navItems as item}
    <li class="nav-item">
        <a href="">{item.name}</a>
        <ul class="first-dropdown">
            {#each item.children as child}
                <li class="first-dropdown-item">
                    <a href="">{child.name}
                        {#if child.children}<span class="fa fa-angle-right"></span>{/if}
                    </a>
                    {#if child.children}
                        <ul class="second-dropdown">
                            {#each child.children as nephew}
                                <li class="second-dropdown-item">
                                    <a href="">{nephew.name}</a>
                                </li>
                            {/each}
                        </ul>
                    {/if}
                </li>
            {/each}
        </ul>
    </li>
{/each}


<script>
    import {navItems} from "./navItem";

    export let items = []
</script>

<style type="text/scss">
  li.nav-item {
    list-style: none;
    display: inline-block;
    vertical-align: middle;
    position: relative;
    &:nth-last-child(-n+2) {
      ul {
        right: 0;
      }
    }
    a {
      display: block;
      padding: 20px 30px;
      font: 500 16px/22px Montserrat, sans-serif;
      color: #212f3d;
      text-decoration: none;
      transition: color .25s ease 0s;

      @media only screen and (max-width: 1400px) {
        padding: 20px 15px;
        font-size: 16px;
      }
      @media only screen and (max-width: 1240px) {
        padding: 15px 10px;
        font-size: 13px;
      }
    }



    ul.first-dropdown {
      position: absolute;
      z-index: 9;
      border-top: 2px solid #228bd6;
      padding: 10px 15px;
      margin: 0;
      background-color: #fff;
      opacity: 0;
      visibility: hidden;
      top: 60px;
      box-shadow: 0 20px 40px 0 rgba(0, 52, 85, .2);

      li.first-dropdown-item {
        display: block;
        border-bottom: 1px solid #f1f8ff;
        border-radius: 6px;
        position: relative;
        transition: all .1s ease 0s;

        a {
          display: block;
          font: 500 18px/18px Montserrat, sans-serif;
          color: #212f3d;
          text-decoration: none;
          min-width: 300px;
          padding: 10px 15px;
          border-radius: 5px;
          position: relative;

          @media only screen and (max-width: 1400px) {
            min-width: 240px;
          }
          @media only screen and (max-width: 1240px) {
            min-width: 200px;
          }

          span {
            position: absolute;
            right: 5px;
            top: 0;
            font-size: 18px;
            color: #8d959d;
            padding: 12px;
          }
        }

        ul.second-dropdown {
          padding: 10px 15px 18px;
          position: absolute;
          left: 105%;
          top: -12px;
          background-color: #fff;
          border-top: 2px solid #228bd6;
          border-left: 2px solid #228bd6;
          opacity: 0;
          visibility: hidden;
          box-shadow: 0 20px 40px 0 rgba(0, 52, 85, .2);

          @media only screen and (max-width: 1240px) {
            padding: 10px 15px;
          }

          li.second-dropdown-item {
            display: block;
            border-bottom: 1px solid #f1f8ff;
            border-radius: 6px;
            position: relative;
            transition: all .1s ease 0s;

            &:last-child {
              border-bottom: 0;
            }
          }
        }

        &:hover {
          a {
            background-color: #f1f8ff;
            color: #228bd6;
          }

          ul {
            opacity: 1;
            visibility: visible;

            li {
              a {
                color: #212f3d;
                background-color: #fff;

                &:hover {
                  background-color: #f1f8ff;
                  color: #228bd6;
                }
              }
            }
          }
        }

        &::before, &:after {
          content: "";
          position: absolute;
          top: 0;
          bottom: 0;
          width: 15px;

        }

        &::before {
          left: -15px;
        }

        &::after {
          right: -15px;
        }

        &:last-child {
          border-bottom: 0;
        }
      }

      &::before {
        position: absolute;
        content: "";
        top: -20px;
        width: 100%;
        height: 20px;
        left: 0;
      }
    }

    &:hover {
      a {
        color: #228bd6;
      }

      ul {
        opacity: 1;
        visibility: visible;
      }
    }


  }

</style>