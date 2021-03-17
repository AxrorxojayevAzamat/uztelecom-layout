<svelte:head>
	<link href="https://fonts.googleapis.com/icon?family=Material+Icons"
      rel="stylesheet">
</svelte:head>
<section class="section5" >
    <div class="container">
        <div class="wrap" >
                        <div class="columns" >
                         <div class="column w-4" >
                     <div class="column__wraps">
                        <div class="mainTitle">
                            <h2>
                                <a href="https://uztelecom.uz/uz/yangiliklar/yangiliklar">
                                    Yangiliklar
                                </a>
                            </h2>
                            
                        </div>
                        <div class="columnNewsActions " id="columnNewsActions-0">
                         
						   <Swiper class="swiper-wrapper" {options}>
								  {#each first as slide} 
                            <div class="swiper-slide item swiper-slide-active" style="width: 400px; margin-right: 30px;">
                                    <div class="wraps">
										{#if slide.title}
                                        <a href="https://uztelecom.uz/uz/yangiliklar/yangiliklar/uztelecom-xodimlari-umumxalq-xayriya-hasharida-ishtirok-etmoqda">
                                            <span class="title">{slide.title}</span>
                                            <span class="teaser">{slide.teaser}</span>
                                        </a>
                                        <span class="date">{slide.data}</span>
                                        <ul>
                                        </ul>
										{/if}
                                    </div>
                                </div>
								{/each}
                            
								
								<!-- <div class="swiper-button-next" slot="button-next"></div>
								<div class="swiper-button-prev" slot="button-prev"></div> -->
                        </Swiper>
                       
                      </div>
                      </div>  


					  
				     <div class="column__wraps">
                        <div class="mainTitle">
                            <h2>
                                <a href="https://uztelecom.uz/uz/yangiliklar/yangiliklar">
                                    Aksiyalar
                                </a>
                            </h2>
                            
                        </div>
                        <div class="columnNewsActions " id="columnNewsActions-0">
                         
						   <Swiper class="swiper-wrapper" {options}>
								  {#each second as slide} 
                            <div class="swiper-slide item swiper-slide-active" style="width: 400px; margin-right: 30px;">
                                    <div class="wraps">
										{#if slide.title}
                                        <a href="https://uztelecom.uz/uz/yangiliklar/yangiliklar/uztelecom-xodimlari-umumxalq-xayriya-hasharida-ishtirok-etmoqda">
                                            <span class="title">{slide.title}</span>
                                            <span class="teaser">{slide.teaser}</span>
                                        </a>
                                        <span class="date">{slide.data}</span>
                                        <ul>
                                        </ul>
										{/if}
                                    </div>
                                </div>
								{/each}
                            
								
								<!-- <div class="swiper-button-next" slot="button-next"></div>
								<div class="swiper-button-prev" slot="button-prev"></div> -->
                        </Swiper>
                       
                      </div>
                      </div>  
						  


				     <div class="column__wraps">
                        <div class="mainTitle">
                            <h2>
                                <a href="https://uztelecom.uz/uz/yangiliklar/yangiliklar">
                                    Xabarnomalar
                                </a>
                            </h2>
                            
                        </div>
                        <div class="columnNewsActions " id="columnNewsActions-0">
                         
						   <Swiper class="swiper-wrapper" {options}>
								  {#each third as slide} 
                            <div class="swiper-slide item swiper-slide-active" style="width: 400px; margin-right: 30px;">
                                    <div class="wraps">
										{#if slide.title}
                                        <a href="https://uztelecom.uz/uz/yangiliklar/yangiliklar/uztelecom-xodimlari-umumxalq-xayriya-hasharida-ishtirok-etmoqda">
                                            <span class="title">{slide.title}</span>
                                            <span class="teaser">{slide.teaser}</span>
                                        </a>
                                        <span class="date">{slide.data}</span>
                                        <ul>
                                        </ul>
										{/if}
                                    </div>
                                </div>
								{/each}
                            
							
							
                        </Swiper>
                       
                      </div>
                      </div>  
				</div>
          </div>
		  </div>
		  </div>
	
			</section >

<script>
	import { one, two, three } from "./section3";
	import 'swiper/swiper-bundle.css'
  import { Swiper} from 'svelte-swiper';
  
  const options = {
	slidesPerView: 1,
      spaceBetween: 15,
      slidesPerGroup: 1,
    pagination: {
      el: '.swiper-pagination',
      clickable: true,
    },
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev',
    },
  };
  export let first = one;
  export let  second = two;
  export let  third = three;
</script>


<style type="text/scss">
  .section5{
	padding: 100px 0 70px 0;
	background-color: #f1f8ff;
	.container{
		display: flex;
				flex-direction: row;
		.wrap{
			position: relative;display: flex;
				flex-direction: row;
			.columns{
				font-size:0; line-height:0; margin: 0 -15px;
				
				
				.column{
					display: inline-block; vertical-align: top;
                  align-items: center;
				 padding-left: 90px;
				  justify-content: center;
					display: flex;
					flex-direction: row;
					.column__wraps{ 
						padding: 0 15px;
						
						.mainTitle{
							margin-bottom: 30px;
							position: relative;
							h2{
								font: 500 30px/42px mont; color: black;
								display: inline-block;
								position: relative;
								a{
									font: 500 30px/42px mont; color: black; text-decoration:none;
									transition: color 250ms ease 0s;
									
								}
								&:hover{
									
									a{
										color:blue;
									}
									&:after{
										background-color:blue;
									}
								}
								&:after{
									position: absolute; content:""; bottom:4px; left:0;
									width: 100%; height: 1px;
									background-color:rgba(gray, 0.5);
								}
							}
							.rss{
								display:inline-block; text-decoration: none;
								margin-left:20px;
								span{
									font-size:20px; color:#ff9a00;
									transition: color 250ms ease 0s;
								}
								&:hover{
									
									span{
										color:blue;
									}
								}
							}
							.btns{
								position: absolute; 
								top: 10px; 
								right:0; left: inherit;
								transform: none;
								z-index: 9;
								min-width: 60px;
								display: flex;
								align-items: center;
								justify-content: space-between;
								.btnArrow {
									position: static;
									width: auto;
									height: auto;
									background: none;
									margin:0; line-height:0;
									cursor: pointer;
									span{
										color:black;
										font-size:24px;
									}
									&.swiper-button-disabled{ display:block; opacity:0.3; }
									&.swiper-button-prev{ 
                    
									}
									&.swiper-button-next{ 
									
									}
								}
							}
						}
						.columnNewsActions{
							padding: 0 20px 50px 20px;
							margin: 0 -20px;
							width: 400px;
							.item{
								
								.wraps{
									padding: 30px 40px;
									box-shadow: 0px 3px 5px 0px rgba(33, 47, 61, 0.06);
									border-radius: 6px;
									background-color:white;
									transition: all 350ms ease 0s;
									a{
										display: block; text-decoration:none;
										.title{
											display: block;
											font: 500 20px/30px mont; color:black;
											margin-bottom:15px; min-height: 60px; max-height: 60px; overflow: hidden;
										}
										.teaser{
											display: block;
											font: 400 14px/24px mont; color:gray;
											min-height:100px; max-height:100px; overflow: hidden;
											margin-bottom: 20px;
										}
										&:hover{
											
											.title{
												color:blue; text-decoration:underline;
											}
										}
									}
									.date{
										display:inline-block; vertical-align: middle;
										font: 400 12px/12px mont; color:gray;
										padding-right: 20px;
									}
									ul{
										display:inline-block; vertical-align: middle;
										font-size:0; line-height:0;
										margin:0 -1px;
										li{
											list-style:none;
											display:inline-block; padding:0 1px;
											a{
												font: 400 12px/12px mont; color:gray; text-decoration:none;
												border-radius:4px;
												background-color:burlywood;
												padding: 8px 10px;
												transition: all 200ms ease 0s;
												&:hover{
													background-color:blue; color:white;
												}
											}
										}
									}
									&:hover{
										box-shadow: 0px 20px 40px 0px rgba(34, 139, 214, 0.15);
									}
								}
							}
						}
					}
				}	
			}
			.mainNewsActions{
				padding: 0 20px 50px 20px;
				margin: 0 -20px;
				.item{
					
					.wraps{
						padding: 30px 40px;
						box-shadow: 0px 3px 5px 0px rgba(33, 47, 61, 0.06);
						border-radius: 6px;
						background-color:white;
						transition: all 350ms ease 0s;
						a{
							display: block; text-decoration:none;
							.title{
								display: block;
								font: 500 20px/30px mont; color:black;
								margin-bottom:15px;
							}
							.teaser{
								display: block;
								font: 400 14px/24px mont; color:gray;
								min-height:100px; max-height:100px; overflow: hidden;
								margin-bottom: 20px;
							}
							&:hover{
								
								.title{
									color:blue; text-decoration:underline;
								}
							}
						}
						.date{
							display:inline-block; vertical-align: middle;
							font: 400 12px/12px mont; color:gray;
							padding-right: 20px;
						}
						ul{
							display:inline-block; vertical-align: middle;
							font-size:0; line-height:0;
							margin:0 -1px;
							li{
								list-style:none;
								display:inline-block; padding:0 1px;
								a{
									font: 400 12px/12px mont; color:gray; text-decoration:none;
									border-radius:4px;
									background-color:blanchedalmond;
									padding: 8px 10px;
									transition: all 200ms ease 0s;
									&:hover{
										background-color:blue; color:white;
									}
								}
							}
						}
						&:hover{
							box-shadow: 0px 20px 40px 0px rgba(34, 139, 214, 0.15);
						}
					}
				}
			}
			.btns{
				position: absolute; 
				top: 45%; 
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
					&.swiper-button-disabled{ display:none; }
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
	&.sectionBusiness{
		
		.container{
			
			.wrap{
			
				.columns{
					
					.column{
						
						.column__wraps{ 
						
							.mainTitle{
							
								h2{
									
									a{
										
										
									}
									&:hover{
										
										a{
											color:blue;
										}
										&:after{
											background-color:blue;
										}
									}
									&:after{
										
									}
								}
								.rss{
								
									span{
									
									}
									&:hover{
										
										span{
											color:blue;
										}
									}
								}
								.btns{
									
									.btnArrow {
									
									}
								}
							}
							.columnNewsActions{
								
								.item{
									
									.wraps{
										
										a{
											
											.title{
												
											}
											.teaser{
												
											}
											&:hover{
												
												.title{
													color:blue; 
												}
											}
										}
										.date{
											
										}
										ul{
											
											li{
											
												a{
													
													&:hover{
														background-color:blue;
													}
												}
											}
										}
										&:hover{
										
										}
									}
								}
							}
						}
					}	
				}
				.mainNewsActions{
					
					.item{
						
						.wraps{
						
							a{
							
								.title{
									
								}
								.teaser{
									
								}
								&:hover{
									
									.title{
										color:blue;
									}
								}
							}
							.date{
								
							}
							ul{
								
								li{
								
									a{
									
										&:hover{
											background-color:blue;
										}
									}
								}
							}
							&:hover{
						
							}
						}
					}
				}
				.btns{
					
					.btnArrow {
						
					}
				}
			}
		}
	}
}

@media only screen and (max-width : 1600px) {
	
	.section5 .container .wrap .btns{ 
		top: 20px;
		max-width: 100px;
		right: 10px;
		left: inherit;
		transform: none;
	}
		.section5 .container .wrap .btns .btnArrow {
			position: static; display:inline-block;
		}
		.section5 .container .wrap .btns .btnArrow span{ font-size:34px; }
		.section5 .container .wrap .btns .btnArrow.swiper-button-disabled{ display: inline-block; }
	
}


@media only screen and (max-width : 1500px) {
	
	.section5 .container .wrap .btns{ right: 70px; }
	
}

@media only screen and (max-width : 1366px) {
	
	.section5 .container .wrap .mainNewsActions .item .wraps .date{ display:block; margin-bottom: 10px; }
	
}

@media only screen and (max-width : 1170px) {
	
	.section5{ overflow: hidden; }
	
	.section5 .container .wrap .mainTitle h2
	.section5 .container .wrap .mainTitle h2{ font-size: 24px; line-height:24px; }
	.section5 .container .wrap .mainTitle h2 a{ font-size: 24px; line-height:24px; }
	.section5 .container .wrap .mainTitle h2:after{ display:none; }
	
	.section5{ padding: 50px 0 20px 0; }
	
	.section5 .container .wrap .columns .column .column__wraps .mainTitle{ margin-bottom:10px; }
	.section5 .container .wrap .columns .column .column__wraps .mainTitle h2 a{ font-size:22px; line-height:22px; }
	.section5 .container .wrap .columns .column .column__wraps .mainTitle .rss span{ font-size:16px; }
	
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps{ padding:20px 20px; }
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps a .title{ font-size:16px; line-height:22px; }
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps a .teaser{ font-size:13px; line-height:22px; }
	
}

@media only screen and (max-width : 992px) {
	
	.section5 .container .wrap .columns{  }
	.section5 .container .wrap .columns .column{ width:50%; }
	.section5 .container .wrap .columns .column:last-child{ width: 100%; }
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions {
		padding: 0 20px 20px 20px;
	}
	
}

@media only screen and (max-width : 640px) {
	
	.section5 .container .wrap .columns .column{ width: 100%; }
	
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps a .teaser {
		line-height: 24px;
	}	
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps .date{ display: block; margin-bottom: 10px; }
	
}
@media only screen and (max-width : 580px) {
	
	.section5 .container .wrap .mainTitle{ padding-right:80px; }
	.section5 .container .wrap .mainTitle .rss{ margin-left:0; margin-top: 10px; }
	.section5 .container .wrap .btns{ top:10px; }
	.section5 .container .wrap .mainTitle h2{ line-height:28px; }
	
}
@media only screen and (max-width : 480px) {
	
	.section5 .container .wrap .mainTitle h2{ font-size:18px; line-height:20px; }
	.section5 .container .wrap .mainTitle h2 a{ font-size:18px; line-height:20px; }
	.section5 .container .wrap .mainTitle .rss{ margin-left:0; }
	.section5 .container .wrap .mainNewsActions .item .wraps{ padding:20px; }
	.section5 .container .wrap .mainNewsActions .item .wraps a .title{ font-size:16px; line-height:20px; }	
	
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps{ padding:20px; }
	.section5 .container .wrap .columns .column .column__wraps .columnNewsActions .item .wraps a .title{ font-size:16px; line-height:20px; }
	
}
</style>