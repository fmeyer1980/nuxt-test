<template>
    <div :class="['cases', colorTheme]">
        <div class="top" data-aos="text-ani-up" data-aos-anchor-placement="top-bottom" data-aos-once="true">
            <div class="container container--right">
                <div class="width--680">
                    <h2 class="heading h1">Cases</h2>
                    <p class="text--large">Get a leg up on the competition, and learn the newest tools, techniques, and technologies popular in your field.</p>
                </div>
            </div>
        </div>
        <div class="wrapper">
            <div class="container container--right">

                <nuxt-link class="item" data-aos="case-animation" data-aos-once="true" to="/cases/toftild">
                    <div class="image-container" @click="selected = 1" :class="{active:selected == 1}">
                        <div class="img-wrapper">
                            <img class="image" src="@/assets/images/case1.jpg" alt=""/>
                        </div>
                        <div class="overlay toftild"></div>   
                    </div>
                    <div class="content" data-aos="case-text-ani" data-aos-once="true">
                        <span class="sub-heading">Website & webshop</span>
                        <h3 class="heading h3">Toftild</h3>
                    </div>
                </nuxt-link>

                <nuxt-link class="item" data-aos="case-animation" data-aos-once="true" to="/cases/beachtours">
                
                    <div class="image-container" @click="selected = 2" :class="{active:selected == 2}">
                        <div class="img-wrapper">
                            <img class="image" src="@/assets/images/case2.jpg" alt=""/>
                        </div>
                        <div class="overlay beachtours"></div>   
                    </div>
                    <div class="content" data-aos="case-text-ani" data-aos-once="true">
                        <span class="sub-heading">Website</span>
                        <h3 class="heading h3">Beach tours</h3>
                    </div>
                </nuxt-link>

                <nuxt-link class="item" data-aos="case-animation" data-aos-once="true" to="/cases/test">
                    <div class="image-container" @click="selected = 3" :class="{active:selected == 3}">
                        <div class="img-wrapper">
                            <img class="image" src="@/assets/images/case3.jpg" alt=""/>
                        </div>
                        <div class="overlay test-color"></div>   
                    </div>
                    <div class="content" data-aos="case-text-ani" data-aos-once="true">
                        <span class="sub-heading">Dashboard</span>
                        <h3 class="heading h3">LeadscoreApp</h3>
                    </div>
                </nuxt-link>

                <nuxt-link class="item" data-aos="case-animation" data-aos-once="true" to="/cases/limfjords-camping">
                    <div class="image-container" @click="selected = 4" :class="{active:selected == 4}">
                        <div class="img-wrapper">
                            <img class="image" src="@/assets/images/case4.jpg" alt=""/>
                        </div>
                        <div class="overlay limfjords-camping"></div>   
                    </div>
                    <div class="content" data-aos="case-text-ani" data-aos-once="true">
                        <span class="sub-heading">Website</span>
                        <h3 class="heading h3">Limfjords camping</h3>
                    </div>
                </nuxt-link>

                <nuxt-link class="item" data-aos="case-animation" data-aos-once="true" to="/cases/toftild">
                    <div class="image-container" @click="selected = 5" :class="{active:selected == 5}">
                        <div class="img-wrapper">
                            <img class="image" src="@/assets/images/case5.jpg" alt=""/>
                        </div>
                        <div class="overlay leadscoreapp"></div>   
                    </div>
                    <div class="content" data-aos="case-text-ani" data-aos-once="true">
                        <span class="sub-heading">Website & webshop</span>
                        <h3 class="heading h3">Sandbalance</h3>
                    </div>
                </nuxt-link>

                <nuxt-link class="item" data-aos="case-animation" data-aos-once="true" to="/cases/toftild">
                    <div class="image-container" @click="selected = 6" :class="{active:selected == 6}">
                        <div class="img-wrapper">
                            <img class="image" src="@/assets/images/case6.jpg" alt=""/>
                        </div>
                        <div class="overlay leadscoreapp"></div>   
                    </div>
                    <div class="content" data-aos="case-text-ani" data-aos-once="true">
                        <span class="sub-heading">Website</span>
                        <h3 class="heading h3">Online ski</h3>
                    </div>
                </nuxt-link>
            </div>
        </div>
    </div>

</template>

<script>



export default {
  name: 'cases',
  data() {
     return{
        selected: undefined
     } 
    
  },
  props: {
    colorTheme: String
  }
  
}
</script>


<style lang="scss" scoped>
@import '~/assets/css/global.scss';

[data-aos="case-animation"] {
  opacity: 0;
  transition-property: transform, opacity;

  &.aos-animate {
    opacity: 1;
  }

}

[data-aos="case-text-ani"] {
    opacity: 0;
    transform: translate3d(30px,0,0);
    transition: .2s cubic-bezier(1,0,1,1);
        
    &.aos-animate {
        opacity: 1;
        transform: translate3d(0px,0,0);
    }
}

.cases.home{
    .top{
        padding: ($gutter * 2) 0 ($gutter * 4.5);
    }
}

.cases{
    background-color: $white;

      .top{
        background-color: $lightGrayLight;
        padding: ($gutter * 5) 0 ($gutter * 4.5);

      .heading{
          margin-top: 0;
          margin-bottom: 0;
          font-weight: 400;
          position: relative;
          padding-left: 0.35em;
          line-height: 1em;
          &:after{
              content: "";
              height: 0.8em;
              width: 5px;
              background-color: var(--primary);
              position: absolute;
              left: 0;
              top: 0;
              margin-top: .05em;
          }
      }

      .text{
          max-width: 30rem;
          opacity: 0.7;
      }
  }

  .wrapper{
      margin-top: -18rem;

      > div{
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      position: relative;

      @media (max-width: $screen-sm) {
        grid-template-columns: repeat(2, 1fr);
      }

      .item{
          color: $text-color;

          
          &:nth-child(1), &:nth-child(4){
              .image-container{
                .image{
                    transition-delay: .4s;
                }
                .overlay{
                    transition-delay: 0s;
                }
              }
          }
          &:nth-child(2), &:nth-child(5){
              .image-container{
                .image{
                    transition-delay: .6s;
                }
                .overlay{
                    transition-delay: .2s;
                }
              }
          }
          &:nth-child(3), &:nth-child(6){
              .image-container{
                .image{
                    transition-delay: .8s;
                }
                .overlay{
                    transition-delay: .4s;
                }
              }
          }
        .image-container{
            
            display: grid;

            .img-wrapper{
                overflow: hidden;
                width: 100%;
                height: 100%;
                grid-row-start: 1;
                grid-column-start: 1;
                padding-top: calc(591.44 / 727.34 * 100%);
                position: relative;
            }

            .image{
                position: absolute;
                z-index: 2;
                object-fit: cover;
                width: 100%;
                height: 100%;
                opacity: 0;
                transition: opacity 0.1s ease-out;
                transform: scale3d(1.075,1.075,1);
                transition: 0.2s ease-in-out;
                top: 0;
                left: 0;
    
            }

            .overlay{
                width: 100%;
                height: 100%;
                background-color: var(--primary);
                max-height: 0;
                transition: max-height .3s cubic-bezier(1,0,1,1);
                grid-row-start: 1;
                grid-column-start: 1;
                position: relative;
            }
        }

        .content{
            padding: 2rem 0 6rem;

            .heading{
                margin-top: 0.2em;
                margin-bottom: 0;
                font-weight: 400;
                position: relative;
                padding-left: 0.4em;
                line-height: 1em;
                font-size: 2.6rem;
                &:after{
                    content: "";
                    height: 0.8em;
                    width: 3px;
                    background-color: var(--primary);
                    position: absolute;
                    left: 0;
                    top: 0;
                    margin-top: 0.1em;
                }
            }

            .sub-heading{
                opacity: 0.7;
                font-size: 1.3rem;
                margin-bottom: .5em;
                display: block;
            }
        }

        /* &:hover{
            .image-container{
                .image{
                    opacity: .1 !important;
                    transition-delay: 0s;
                }
            }

        } */

      }

      .active{

          .img-wrapper{

            .image{
                z-index: -1 !important;
            }
          }
          .overlay{
            animation: caseOverlayAni 1s ease forwards;
            z-index: 98;
        }
      }

    [data-aos="case-animation"] {
          
        &.aos-animate {
            .image-container{

                    .image{
                        opacity: 1;
                        transform: scale3d(1,1,1);
                    }

                    .overlay{
                        max-height: 100%;
                    }
            }
        }
    }


  }

}
    
}

</style>