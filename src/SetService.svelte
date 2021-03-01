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
                                        <span class="fas fa-{item.icon}"></span>
                                        <span class="title">{item.name}</span>
                                    </a>
                                </div>
                            </div>
                        {/each}
                    </div>
                </div>
            </div>
<div class="col-right">
        <div class="wraps">
        <iframe width="450px" height="407px" style="width:100%;" src="https://oplata.kapitalbank.uz/uz/uztelecom" frameborder="0"></iframe>
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
                icon: 'circle'
            },
            {
                name: 'CDMA tariflar',
                icon: 'circle'
            },
            {
                name: 'Internet tariflar',
                icon: 'layer-group'
            },
            {
                name: 'GSM qoplangan hudud',
                icon: 'signal'
            },
            {
                name: 'Saytni TAS-IX tarmog`i uchun tekshirish',
                icon: 'wifi'
            },
            {
                name: 'Tezlikni tekshirish',
                icon: 'tachometer-alt'
            },
            {
                name: 'Ofislarimiz',
                icon: 'street-view'
            },
            {
                name: 'Telefon apparatlari va qurilmalar',
                icon: 'mobile-alt'
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
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
      

      .wrap {
        font-size: 0;
    line-height: 0;
    margin: 0 -15px;
    
        @media only screen and (max-width: 1170px)
        {
          padding: 0 15px;

        }
        @media only screen and (max-width: 1500px)
        {
         
        }   

        .col-right
        {
          width: 33.333334%;
          @media only screen and (max-width: 992px)
                 {
                      width: 100%;
                 }
        }
        .col-left {
          display: inline-block;
          vertical-align: top;
          width: 66.6666666%;
          @media only screen and (max-width: 992px)
          {
            width: 100%;
            margin-bottom: 30px;
          }

          .wraps {
            padding: 0 15px;
           


          
          
            .list {
              font-size: 0;
              line-height: 0;
              margin: 0 -15px;

   
              @media only screen and (max-width: 140px)
              {
                margin: 0 -5px;
                
              }   
             
              @media only screen and (max-width: 480px)
              {
                margin: 0 -5px;
                
              }   
           
                

              .item {
                list-style: none;
                width: 25%;
                display: inline-block;
                vertical-align: top;
                margin-bottom: 30px;
                @media only screen and (max-width: 1400px)
              {    
                
                margin-bottom: 20px;
                
             
              }  
              
              @media only screen and (max-width: 700px)
              {  
                
                  width: 33.333333%;
                
             
              }  
             
            
                @media only screen and (max-width: 480px)
              {
                width: 50%;
                margin-bottom: 10px;
                
              }   
             
                
          
             
                .item__wraps {
                  padding: 0 15px;
                  text-align: center;
     
                @media only screen and (max-width: 480px)
              {
                padding: 0 5px;
              }   
           

           
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


             
                    @media only screen and (max-width: 480px)
              {
                padding: 20px 5px;
              }   
           
                    span {
                      font-size: 72px;
                      color: #8d959d;
                      display: block;
                      margin-bottom: 34px;
                      transition: color .25s ease 0s;
                      @media only screen and (max-width: 1400px)
              {    
                
                font-size: 52px;
                
             
              }  
     
                @media only screen and (max-width: 480px)
              {
                margin-bottom: 20px;
              }   
           
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
    .img{
       padding-left: 69px;
       padding-right: 150px;
       margin-bottom: 25px;
       overflow: hidden;
     }

  }
//   @media only screen and (max-width: 480px)
//   {
//     .set-service .container .wrap .col-left .wraps .list{
//     margin: 0 -5px;
// }
//   }



 
</style>
