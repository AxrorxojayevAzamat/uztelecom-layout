<nav class="icons">
    <ul>
        <li class:active='{cabinet_show}'>
            <a href="#" on:click={() => {lang_show = false; cabinet_show = !cabinet_show}}>
                <span class="fas fa-user-alt"></span>
            </a>
            <ul class="lang">
                {#each cabinetdata as cabinet}
                    <li>
                        <a href="#">{cabinet}</a>
                    </li>
                {/each}
            </ul>
        </li>
        <li class:active='{lang_show}'>
            <a href="#" on:click={() => {cabinet_show = false; lang_show = !lang_show}}>{langs[1]}</a>
            <ul class="lang">
                {#each langs as lang}
                    <li>
                        <a href="#">{lang}</a>
                    </li>
                {/each}
            </ul>
        </li>
    </ul>
</nav>

<script>
    let langs = ['Русский', 'O\'zbek', 'English'], lang_show = false
    let cabinetdata = ['Shaxsiy kabinet', 'Virtual ofis'], cabinet_show = false
</script>

<style type="text/scss">
    nav.icons {
      margin-bottom: 20px;
      ul {
        text-align: center;
        margin: 0 -10px;
        li {
          list-style: none;
          display: inline-block;
          vertical-align: middle;
          padding: 0 10px;
          min-height: 25px;
          position: relative;
          &.active {
            ul {
              opacity: 1;
              visibility: visible;
            }
            a {
              color: #228bd6;
            }
          }
          a {
            padding: 5px;
            border-radius: 6px;
            font: 500 12px/12px Montserrat,sans-serif;
            color: rgba(33,47,61,.6);
            text-decoration: none;
            span {
              font-size: 20px;
            }
          }
          ul {
            position: absolute;
            left: 0;
            top: 30px;
            z-index: 4;
            overflow: hidden;
            background-color: #fff;
            box-shadow: 0 10px 30px 0 rgba(56, 56, 55, .2);
            border-bottom-left-radius: 4px;
            border-bottom-right-radius: 4px;
            border-top: 2px solid #228bd6;
            opacity: 0;
            visibility: hidden;
            transition: all .3s ease 0s;
            &.lang {
              text-align: left;
              li {
                a {
                  min-width: 80px;
                  white-space: nowrap;
                }
              }
            }
            li {
              padding: 0;
              a {
                display: block;
                min-width: 190px;
                padding: 10px;
              }
            }
          }
        }
      }
    }
</style>