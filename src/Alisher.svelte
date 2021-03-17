    <svelte:head>
     
    <script src="https://kit.fontawesome.com/yourcode.js" crossorigin="anonymous"></script>
    </svelte:head>
<section class="section3">
    <div class="container">
        <div class="wrap">
            <div class="mainTitle">
                <h2>Ommabop tariflar</h2>
            </div>
            <div class="mainPopularTarifs swiper-container swiper-container-initialized swiper-container-horizontal">
                <Swiper class="swiper-wrapper" {options}>

                    



                    {#each first as slide} 
                    <div class="swiper-slide item swiper-slide-active" >
                        {#if slide.title}
                        <div class="head" style="background-color:#228bd6;">
                            <a href="">
                                <span class="title">{slide.title}</span>
                                <span class="category">{slide.category}</span>
                                <img class="lazy loaded" src="https://uztelecom.uz/images/svg/phone-1.svg" alt=""  data-was-processed="true">
                            </a>
                        </div>

                        <div class="body">
                            <a href="">
                                <ul>
                                    <li>
                                        <span class="icon icon-phone-4"></span>
                                        <span class="key1">{slide.key1}</span>
                                        <span class="value1"><strong>{slide.value1}</strong></span>
                                    </li>
                                    
                                    <li>
                                        <span class="icon icon-www"></span>
                                        <span class="key2">{slide.key2}</span>
                                        <span class="value2">{slide.value2}</span>
                                    </li>
                                                                                                            
                                    <li>
                                        <span class="icon icon-sms"></span>
                                        <span class="key3">{slide.key3}</span>
                                        <span class="value3">{slide.value3}</span>
                                    </li>
                                </ul>
                                
                                <div class="total">
                                    <span class="key">Abonent to‘lovi oyiga</span>
                                    <span class="value">
                                        <strong>99 000</strong> so'm
                                    </span>
                                    <span class="btn"><span class="icon-chevrone-right"></span></span>
                                </div>
                            </a>
                           
                        </div>
                         {/if}
                    </div>
                    {/each}
                    


                    

                    
                    {#each second as slide} 
                    <div class="swiper-slide item">
                        {#if slide.title}
                        <div class="head" style="background-color:#1bb367;">
                            <a href="">
                                <span class="title">{slide.title}</span>
                                <span class="category">{slide.category}</span>
                                <img class="lazy" src="https://uztelecom.uz/images/svg/phone-2.svg" alt="">
                            </a>
                        </div>
                        <div class="body">
                            <a href="">
                                <ul>
                                    <li>
                                        <span class="icon icon-phone-4"></span>
                                        <span class="key1">{slide.key1}</span>
                                        <span class="value1"><strong>{slide.value1}</strong></span>
                                    </li>
                                                                                                            
                                    <li>
                                        <span class="icon icon-www"></span>
                                        <span class="key2">{slide.key2}</span>
                                        <span class="value2">{slide.value2}</span>
                                    </li>
                                                            
                                    <li>
                                        <span class="icon icon-sms"></span>
                                        <span class="key3">{slide.key3}</span>
                                        <span class="value3">{slide.value3}</span>
                                    </li>
                                </ul>
                                
                                <div class="total">
                                    <span class="key">Abonent to‘lovi oyiga</span>
                                    <span class="value">
                                        <strong>9 900</strong> so'm
                                    </span>
                                    <span class="btn"><span class="icon-chevrone-right"></span></span>
                                </div>
                            </a>
                        </div>
                        {/if}
                    </div>
                    {/each}




                    
                    {#each third as slide} 
                    <div class="swiper-slide item">
                        {#if slide.title}
                        <div class="head" style="background-color:#228bd6;">
                            <a href="https://uztelecom.uz/uz/jismoniy-shaxslarga/internet-2/tariflar-2/unlim-21/unlim-10-11">
                                <span class="title">{slide.title}</span>
                                <span class="category">{slide.category}</span>
                                <img class="lazy" src="https://uztelecom.uz/images/svg/router.svg" alt="">
                            </a>
                        </div>
                        <div class="body">
                            <a href="https://uztelecom.uz/uz/jismoniy-shaxslarga/internet-2/tariflar-2/unlim-21/unlim-10-11">
                                <ul>
                                    <li>
                                        <span class="icon icon-www"></span>
                                        <span class="key1">{slide.key1}</span>
                                        <span class="value1"><strong>{slide.value1}</strong></span>
                                    </li>
                                    
                                    <li>
                                        <span class="icon icon-arrow-in"></span>
                                        <span class="key2">{slide.key2}</span>
                                        <span class="value2">{slide.value2}</span>
                                    </li>
                                </ul>
                            
                                <div class="total">
                                    <span class="key">Abonent to‘lovi oyiga</span>
                                    <span class="value"><strong>119 000 </strong> so'm</span>
                                    <span class="btn"><span class="icon-chevrone-right"></span></span>
                                </div>
                            </a>
                        </div>
                        {/if}
                    </div>
                    {/each}


                    



                    {#each IPTV as slide} 
                    <div class="swiper-slide item">
                        {#if slide.title}
                        <div class="head" style="background-color:#e6007e;">
                            <a href="https://uztelecom.uz/uz/jismoniy-shaxslarga/iptv-2/tariflar-3/iptv-5">
                                <span class="title">{slide.title}</span>
                                <span class="category">{slide.category}</span>
                                <img class="lazy" src="https://uztelecom.uz/images/svg/monitor.svg" alt="">
                            </a>
                        </div>
                        <div class="body">
                            <a href="https://uztelecom.uz/uz/jismoniy-shaxslarga/iptv-2/tariflar-3/iptv-5">
                                <ul>
                                    <li>
                                        <span class="icon icon-monitor-2"></span>
                                        <span class="key1">{slide.key1}</span>
                                        <span class="value1"><strong>{slide.value1}</strong></span>
                                    </li>
                                                                                                            
                                    <li>
                                        <span class="icon icon-eye"></span>
                                        <span class="key2">{slide.key2}</span>
                                        <span class="value2">{slide.value2}</span>
                                    </li>
                                </ul>
                                                                
                                <div class="total">
                                    <span class="key">Abonent to‘lovi oyiga</span>
                                    <span class="value"><strong>15 000 </strong> so'm</span>
                                    <span class="btn"><span class="icon-chevrone-right"></span></span>
                                </div>
                            </a>
                        </div>
                        {/if}
                    </div>
                    {/each}
                    
                    


                    {#each office as slide} 
                    <div class="swiper-slide item" style="width: 361.333px; margin-right: 10px;">
                        {#if slide.title}
                        <div class="head" style="background-color:#0046e6;">
                            <a href="https://uztelecom.uz/uz/jismoniy-shaxslarga/uy-telefoni/tariflar-7/shahar-tarmogi">
                                <span class="title">{slide.title}</span>
                                <span class="category">{slide.category}</span>
                                <img class="lazy" src="https://uztelecom.uz/images/svg/phone-3.svg" alt="">
                            </a>
                        </div>
                        <div class="body">
                            <a href="https://uztelecom.uz/uz/jismoniy-shaxslarga/uy-telefoni/tariflar-7/shahar-tarmogi">
                                <ul>
                                    <li>
                                        <span class="icon icon-phone-4"></span>
                                        <span class="key1">{slide.key1}</span>
                                        <span class="value1"><strong>{slide.value1}</strong></span>
                                    </li>
                                    
                                    <li>
                                        <span class="icon icon-phone-4"></span>
                                        <span class="key2">{slide.key2}</span>
                                        <span class="value2">{slide.value2}</span>
                                    </li>
                                </ul>
                                                                
                                <div class="total">
                                    <span class="key">Abonent to‘lovi oyiga</span>
                                    <span class="value"><strong>5 800</strong> so'm</span>
                                    <span class="btn"><span class="icon-chevrone-right"></span></span>
                                </div>
                            </a>
                        </div>
                        {/if}
                    </div>
                    {/each}

                    
                   
                </Swiper>
                <span class="swiper-notification" aria-live="assertive" aria-atomic="true"></span>
             </div>


            <div class="btns">
                 <div class="swiper-button-next" id="nextA" ></div>
                    <div class="swiper-button-prev" id="prevA"></div>
            </div>
        </div>
    </div>
</section>

<script>
    import { one, two, three, ofis, iptv} from "./section5";
    import { Swiper } from 'svelte-swiper';

    const options = {
        slidesPerView: 5,
      spaceBetween: 30,
      slidesPerGroup: 1,
    pagination: {
      el: '.swiper-pagination',
      clickable: true,
    },
    navigation: {
      nextEl: '#nextA',
      prevEl: '#prevA',
    },
  };
  export let first = one;
  export let  second = two;
  export let  third = three;
  export let  IPTV = iptv;
  export let  office = ofis;
</script>

<style type="text/scss">
   .section3{
	padding: 100px 0 70px 0;
    background-color: white;
	.container{
	
		.wrap{
			position: relative;
			.mainTitle{
				margin-bottom: 40px;
				h2{
					font: 500 36px/48px mont; color:black;
				}
			}
			.mainPopularTarifs{
				padding: 0 10px 50px 10px;
				margin: 0 -10px;
              
				.item{
					height: auto;
                    background-color: #f1f8ff;
					transition: all 350ms ease 0s;
                  
                   

					.head{
						padding: 20px 20px;
						font-size:0; line-height:0;
						position: relative;
                     
						a{
							text-decoration: none;
							.title{
								display: block;
								font: 700 24px/34px mont; color:white;
							}
							.category{
								display: block;
								font: 400 14px/14px mont; color:rgba(white, 0.5);
							}
							img{
								display:inline-block;
								//max-height: 50px; max-width: 60px;
								max-height: 35px; max-width: 35px;
								width: 100%; height: 100%;
								position: absolute;
								//top: 50%;
								bottom: -15px;
								//right: 20px;
								right: 0px;
								transform: translateY(-50%);
							}
						}
					}
					.body{
						padding: 30px 20px 25px 20px;
						font-size:0; line-height:0;
                        
						a{
							text-decoration:none;
							display: block;
							ul{
								padding-bottom: 20px; margin-bottom: 20px;
								border-bottom: 1px solid #c5d7e8;
								min-height:155px;
								li{
									list-style: none;
									display: block;
									padding-left: 45px; margin-bottom: 20px;
									position: relative;
									.icon{
										position: absolute; top:0; left:0;
										font-size:24px; color:#a6bed4;
									}
									.key1, .key2, .key3, .key4{
										display: block; margin-bottom:3px;
										font: 400 14px/14px mont; color:black;
									}
									.value1, .value2, .value3, .value4{
										display: block;
										font: 500 20px/20px mont; color:black;
										strong{
											font: 700 24px/24px mont;
										}
									}
									&:last-child{
										margin-bottom:0;
									}
								}
							}
							.total{
								position: relative;
								.key{
									display: block; margin-bottom: 5px;
									font: 400 14px/14px mont; color:black;
								}
								.value{
									display: block;
									font: 700 18px/18px mont; color:black;
									strong{
										font: 700 30px/30px mont;
									}
								}
								.btn{
									position: absolute; top:50%; right:-20px;
									transform: translateY(-50%);
									text-decoration:none;
									display: flex; align-items: center; justify-content:center;
									width: 40px; height: 40px;
									background-color:yellow; border-radius: 100%;
									text-decoration:none;
									opacity:0; visibility: hidden;
									transition: all 250ms ease 0s;
									span{
										font-size: 14px; color:black;
									}
								}
							}
						}
					}
					&:hover{
						background-color:white;
						box-shadow: 0px 20px 40px 0px rgba(34, 139, 214, 0.15);
						z-index:1;
						.body{
							
							.total{
								
								.btn{
									right:0;
									opacity: 1; visibility: visible;
								}
							}
						}
					}
				}
			}
			// Popular tarifs Business
			.mainPopularTarifsBusiness{
				padding: 0 10px 50px 10px;
				margin: 0 -10px;
				.swiper-wrapper{
					
				}
				.item{
					border-radius: 6px; overflow: hidden;
					height: auto;
					background-color:blanchedalmond;
					transition: all 350ms ease 0s;
					.head{
						padding: 20px 20px;
						font-size:0; line-height:0;
						background-color:blue;
						position: relative;
						a{
							text-decoration: none; 
							.title{ 
								display: block;
								font: 700 24px/34px mont; color:white; 
							}
							.category{
								display: block;
								font: 400 14px/14px mont; color:rgba(white, 0.5);
							}
							img{
								display:inline-block;
								max-height: 50px; max-width: 60px;
								position: absolute; 
								top: 50%;
								right: 20px;
								transform: translateY(-50%);
							}
							.head-icon{
								display:inline-block;
								position: absolute; top: 27px; right: 20px;
								font-size:24px; color:rgba(white, 0.3);
							}
						}
					}
					.body{
						padding: 40px 30px 30px 30px;
						font-size:0; line-height:0;
						a{
							text-decoration:none;
							display: block;
							ul{
								padding-bottom: 20px; margin-bottom: 25px;
								min-height:155px;
								li{
									list-style: none;
									display: block;
									padding-left: 0; margin-bottom: 20px;
									position: relative;
									font: 400 12px/24px mont; color:black;
									.icon{
										position: absolute; top:0; left:0;
										font-size:24px; color:#a6bed4;
									}
									span{
										font: 500 20px/24px mont; color:black;
									}
									strong{
										font: 700 24px/24px mont; color:black;
									}
									&:last-child{
										margin-bottom:0;
									}
								}
							}
							.total{
								position: relative;
								.value{
									display: block;
									font: 400 14px/24px mont; color:black; 
									strong{
										font: 700 30px/30px mont;
									}
								}
								.btn{
									position: absolute; top:50%; right:-20px;
									transform: translateY(-50%);
									text-decoration:none;
									display: flex; align-items: center; justify-content:center;
									width: 40px; height: 40px;
									background-color:#01b463; border-radius: 100%;
									text-decoration:none;
									opacity:0; visibility: hidden;
									transition: all 250ms ease 0s;
									span{
										font-size: 14px; color:white;
									}
								}
							}
						}
					}
					&:hover{
						background-color:white;
						box-shadow: 0px 20px 40px 0px rgba(34, 139, 214, 0.15);
						z-index:1;
						.body{
							
							.total{
								
								.btn{
									right:0;
									opacity: 1; visibility: visible;
								}
							}
						}
					}
				}	
			}
			.btns{
				position: absolute; 
				top: 50%; 
				left:0; right:0;
				transform: translateY(-50%);
				z-index: 9;
				.btnArrow {
					position: absolute;
					width: auto;
					height: auto;
					background: none;
					margin:0; line-height:0;
					span{
						color:black;
						font-size:54px;
					}
					&.swiper-button-prev{ 
						left: -75px;
					}
					&.swiper-button-next{ 
						right: -75px;
					}
				}
			}
		}
	}
}


@media only screen and (max-width : 1600px) {
	
	.section3 .container .wrap .btns{
		transform: none; 
		max-width: 70px; width:100%; 
		left: inherit;
		right: 10px; top: 0;
	}
	.section3 .container .wrap .btns .btnArrow span{ font-size:34px; }
	.section3 .container .wrap .btns .btnArrow.swiper-button-prev{ left: 0; }
	.section3 .container .wrap .btns .btnArrow.swiper-button-next{ right: 0; }
	
}

@media only screen and (max-width : 1500px) {
	
	.section3 .container .wrap .btns{ right: 70px; }
	.section3 .container .wrap .mainPopularTarifs .item .head a .title{ font-size:20px; line-height:30px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a ul li{ padding-left:35px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a ul li .value strong{ font-size:20px; line-height:20px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a ul li .icon{ font-size:17px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a ul li .value{ font-size:16px; line-height:16px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a .total .value strong{ font-size:22px; line-height:22px; }
	
	.section3 .container .wrap .mainPopularTarifs .item .head a img{ max-width:35px; max-height: 30px; }
	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body {
		padding: 20px 20px 20px 20px;
	}	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .head a .title{ font-size:18px; line-height:18px; }
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a ul li strong{ font-size:18px; line-height:18px; }
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a ul li span{ font-size:18px; line-height:18px; }
	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a .total .value strong{ font-size:22px; line-height:22px; }
	
}

@media only screen and (max-width : 1170px) {
	
	.section3{ overflow: hidden; }
	
	.section3 .container .wrap .btns{ right: 15px; }
	
}
@media only screen and (max-width : 992px) {
	
	.section3 {
		padding: 40px 0 20px 0;
	}
	.section3 .container .wrap .mainTitle h2{ font-size:22px; line-height:38px; }
	
	.section3 .container .wrap .mainPopularTarifs .item .head a .title{ font-size:18px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a ul li .value strong{ font-size:20px; line-height:20px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a .total .value strong{ font-size:20px; line-height:20px; }
	.section3 .container .wrap .mainPopularTarifs .item .body a ul li .value{ font-size: 16px; }	
	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .head a .title{ font-size:18px; }
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a ul li .value strong{ font-size:20px; line-height:20px; }
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a .total .value strong{ font-size:20px; line-height:20px; }
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a ul li .value{ font-size: 16px; }
	
}

@media only screen and (max-width : 480px) {
	
	.section3 .container .wrap .btns{ max-width:70px; }
	.section3 .container .wrap .mainTitle h2{ font-size:18px; }
	
	.section3 .container .wrap .mainPopularTarifs{ padding: 0 20px 0  20px; }
	.section3 .container .wrap .mainPopularTarifsBusiness{ padding: 0 20px 0  20px; }
	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body {
		padding: 30px 20px 30px 20px;
	}	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a ul {
		padding-bottom: 10px;
		margin-bottom: 15px;
		min-height: 155px;
	}	
	.section3 .container .wrap .mainPopularTarifsBusiness .item .body a ul li{ margin-bottom:10px; }
	
	
}


</style>