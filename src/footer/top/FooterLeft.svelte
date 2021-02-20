<div class="wraps">
    {#each pages as page}
        <nav>
            <h3>{page.title}</h3>
            <ul>
                {#each page.subpages as subpage}
                    <li>
                        <a href="">{subpage}</a>
                    </li>
                {/each}
            </ul>
        </nav>
    {/each}
</div>

<script>
    import {pages} from "./pages";
</script>

<style type="text/scss">
  .wraps {
    margin: 0 -15px;

    nav {
      width: 25%;
      display: inline-block;
      vertical-align: top;

      h3 {
        font: 700 18px/18px Montserrat, sans-serif;
        color: #212f3d;
        margin-bottom: 30px;
        padding: 0 15px;
      }

      ul {
        padding: 0 15px;

        li {
          list-style: none;
          margin-bottom: 15px;

          a {
            display: block;
            font: 400 14px/22px Montserrat, sans-serif;
            color: #8d959d;
            text-decoration: none;
            transition: color .25s ease 0s;

            &:hover {
              color: #228bd6;
              text-decoration: underline;
            }
          }
        }
      }
    }
  }
</style>