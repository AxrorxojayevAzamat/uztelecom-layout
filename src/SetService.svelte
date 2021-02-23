<section class="set-service">
    <div class="img">
        <img src={bgImage} alt="">
    </div>
    <div>
        {#each item as item }
            <a class="card" href={('./:name', {item}, {item})}>
                <h3>{item.name}</h3>
            </a>
        {/each}
    </div>
</section>

<script>
    let bgImage = 'https://uztelecom.uz/images/1380x210_UZ.png';

    let item =
        [
            {name: 'GSM tariflar'},
            {name: 'CDMA tariflar'},
            {name: 'Internet tariflar'},
            {name: 'GSM qoplangan hudud'},
            {name: 'Saytni TAS-IX tarmog`i uchun tekshirish'},
            {name: 'Tezlikni tekshirish'},
            {name: 'Ofislarimiz'},
            {name: 'Telefon apparatlari va qurilmalar'},
        ];
</script>

<style type="text/scss">
  section.set-service {
    background-image: url("https://uztelecom.uz/images/section2-pattern-1.png");
    background-size: cover;
  }

  .img {
    img {
      width: 1300px;
      height: 220px;
      padding-left: 22px;
      cursor: pointer;
    }
  }

  :global(.card) {
    background: white;
    width: 150px;
    height: 150px;
    display: inline-block;
    box-shadow: 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    margin: 24px;
  }

  div {
    height: 100%;
    display: grid;
    grid-template-columns: repeat(4, 2fr);
    width: 600px;
    padding-left: 60px;
    padding-right: 60px;
    padding-top: 50px;

    a {
      padding: 42px 34px;
      text-align: center;
      margin-bottom: 0;
      border-radius: 5px;

      h3 {
        color: #212f3d;
        font-size: 20px;
        font: 500 16px/16px Montserrat, sans-serif;
        margin-bottom: 0;
        margin-top: 150px;
      }
    }
  }
</style>
