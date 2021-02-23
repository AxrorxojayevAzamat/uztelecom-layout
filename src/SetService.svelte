<section class="set-service">
    <div class="img">
        <img src={bgImage} alt="">
    </div>
    <div class="container">
        <div class="wrap">
            <div class="col-left">
                <div class="wraps">
                    <div class="list">
                        {#each items as item }
                            <div class="item">
                                <div class="item__wraps">
                                    <a href="">
                                        <span class="far fa-{item.icon}"></span>
                                        <span class="title">{item.name}</span>
                                    </a>
                                </div>
                            </div>
                        {/each}
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<script>
    let bgImage = 'https://uztelecom.uz/images/1380x210_UZ.png';

    let items =
        [
            {
                name: 'GSM tariflar',
                icon: 'comment-dots'
            },
            {
                name: 'CDMA tariflar',
                icon: 'comment'
            },
            {
                name: 'Internet tariflar',
                icon: 'comment-alt'
            },
            {
                name: 'GSM qoplangan hudud',
                icon: 'comments'
            },
            {
                name: 'Saytni TAS-IX tarmog`i uchun tekshirish',
                icon: 'frown'
            },
            {
                name: 'Tezlikni tekshirish',
                icon: 'meh'
            },
            {
                name: 'Ofislarimiz',
                icon: 'smile'
            },
            {
                name: 'Telefon apparatlari va qurilmalar',
                icon: 'map'
            },
        ];
</script>

<style type="text/scss">
  .set-service {
    padding: 60px 0 30px;
    background-color: #f1f8ff;
    position: relative;
    overflow: hidden;
    .container {
      position: relative;
      z-index: 1;
      max-width: 1440px;
      margin: 0 auto;
      width: 100%;
      .wrap {
        font-size: 0;
        line-height: 0;
        margin: 0 -15px;
        padding: 0 15px;

        .col-left {
          display: inline-block;
          vertical-align: top;
          width: 66.66666667%;

          .wraps {
            padding: 0 15px;

            .list {
              font-size: 0;
              line-height: 0;
              margin: 0 -15px;

              .item {
                list-style: none;
                width: 25%;
                display: inline-block;
                vertical-align: top;
                margin-bottom: 30px;

                .item__wraps {
                  padding: 0 15px;
                  text-align: center;

                  a {
                    display: block;
                    font: 500 16px/16px Montserrat, sans-serif;
                    color: #212f3d;
                    text-decoration: none;
                    border-radius: 6px;
                    background-color: #fff;
                    box-shadow: 0 3px 5px 0 rgba(33, 47, 61, .06);
                    padding: 30px 5px 20px;
                    transition: all .35s ease 0s;

                    span {
                      font-size: 72px;
                      color: #8d959d;
                      display: block;
                      margin-bottom: 34px;
                      transition: color .25s ease 0s;

                      &.title {
                        display: inline-block;
                        min-height: 32px;
                        font: 500 16px/16px Montserrat, sans-serif;
                        color: #212f3d;
                        margin-bottom: 0;
                      }
                    }

                    &:hover {
                      box-shadow: 0 20px 40px 0 rgba(34, 139, 214, .15);

                      span {
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
</style>
