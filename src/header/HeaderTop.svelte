<div class="header-top">
    <div class="wrap">
        <div class="left">
            <ul>
                {#each tabItems as item}
                    <li class=""><a href="">{item}</a></li>
                {/each}
            </ul>
        </div>
        <div class="middle">
            <a href="" class="specialFeatureBtn">
                <i class="fas fa-glasses"></i>
                maxsus imkoniyatlar
            </a>
        </div>
        <div class="right">
            <ul class="region">
                <li>
                    <a href="" on:mouseover={() => {visible = true}} on:mouseleave={() => {visible=false}}>
                        <i class="fas fa-globe-americas"></i>
                        O'zbek
                    </a>
                    {#if visible}
                        <ul class="lang" on:mouseover={() => {visible = true}} on:mouseleave={() => {visible=false}}
                            transition:fly={{y: 10, delay: 100}}>
                            {#each lang as lg}
                                <li><a href="">{lg}</a></li>
                            {/each}
                        </ul>
                    {/if}
                </li>
            </ul>
            <div class="cabinet">
                <a href="" class="cabinetBtn">
                    <i class="fas fa-user-alt"></i>
                    Shaxsiy kabinet
                </a>
            </div>
        </div>
    </div>
</div>

<script>
    import {fly} from 'svelte/transition';

    let visible = false
    let tabItems = ['Jismoniy shaxslarga', 'Biznesga', 'Operatorlarga', 'Agentlarga']
    let lang = ['Русский', 'O\'zbek', 'English']
</script>

<style type="text/scss">

  @mixin headerItem($y, $x, $fontValue) {
    display: block;
    padding: 9px 12px;
    font: 400 12px/$fontValue Montserrat, sans-serif;
    color: #212f3d;
    text-decoration: none;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    transition: color .2s ease 0s;
  }

  @mixin headerItemHover() {
    &:hover {
      background-color: #fff;
      color: #228bd6;

      i {
        color: #228bd6;
      }
    }

    i {
      display: inline-block;
      vertical-align: middle;
      margin-right: 10px;
      font-size: 24px;
      line-height: 22px;
      color: #8d959d;

    }
  }

  @mixin headerListItem($display) {
    display: $display;
    list-style: none;
    vertical-align: middle;
    position: relative;
  }


////////////////////////////////Static properties////////////////////////////////////


  .header-top {
    background-color: #f1f8ff;
    padding: 5px 0 0;

    .wrap {
      display: flex;
      justify-content: space-around;
      margin: 0 auto;
      max-width: 1440px;
      width: 100%;

      .left {
        ul {
          .active {
            a {
              background-color: #fff;
              color: #212f3d;
            }
          }

          li {
            display: inline-block;
            vertical-align: top;

            a {
              @include headerItem(15x, 20px, 12px)
            }
          }
        }
      }

      .middle {
      }
        .right {
          display: flex;
          justify-content: space-between;
          margin: 0 -20px;
          align-items: center;
          min-width: 300px;

          ul.region {
            font-size: 0;
            line-height: 0;
            margin: 0 -12px;

            li {
              @include headerListItem(inline-block);
              a {
                @include headerItem(9px, 12px, 24px);
                @include headerItemHover();
              }

              ul.lang {
                min-width: 100%;
                position: absolute;
                top: 40px;
                z-index: 4;
                overflow: hidden;
                background-color: #fff;
                box-shadow: 0 10px 30px 0 rgba(56, 56, 55, .2);
                border-bottom-left-radius: 4px;
                border-bottom-right-radius: 4px;
                border-top: 2px solid #228bd6;
                transition: all .3s ease 0s;

                li {
                  @include headerListItem(block);

                  a {
                    @include headerItem(9px, 12px, 24px);
                  }
                }
              }
            }
          }

          .cabinet {
            position: relative;

            .cabinetBtn {
              @include headerItem(9px, 20px, 24px);
            }
          }
        }
        a.specialFeatureBtn {
          @include headerItem(12px, 20px, 24px);
          @include headerItemHover();
        }
      }

  }



</style>