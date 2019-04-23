<template>
  <div class="about">
    <div class="about-box">
        <div class="container container--left">
            <div class="image-ani"></div>
            <div class="image-wrapper">
                <img class="image" src="~assets/images/about-home.jpg" alt="Flemming Meyer"/>
                <a class="contact-btn" href="">Kontakt mig for at høre nærmere <span></span></a>
            </div>
            <div class="content-ani-wrapper">
                <div class="content-ani"></div>
            </div>
            <div class="content">
                <span>Flemming Meyer</span>
                <h1>Webdesigner og udvikler</h1>
                <p>Hej mit navn er Flemming Meyer og jeg er senior designer samt webudvikler. De sidste 10 år har jeg arbejdet for flere forskellige webbureauer hvor jeg primært har arbejde med design og udvikling af hjemmesider til et bredt udvalgt af kunder. Igennem mine mange års erfaring har jeg bygget et bredt udvalg af kompetencer op følgene værktøjer.</p>
            </div>
            <ul class="content__bottom">
                <li><img src="~assets/images/work-sketch.png" alt="" /></li>
                <li><img src="~assets/images/work-invision.png" alt="" /></li>
                <li><img src="~assets/images/work-framer.png" alt="" /></li>
                <li><img src="~assets/images/work-adobe.png" alt="" /></li>
                <li><img src="~assets/images/work-sass.png" alt="" /></li>
                <li><img src="~assets/images/work-gatsby.png" alt="" /></li>
                <li><img src="~assets/images/work-wordpress.png" alt="" /></li>
            </ul>
            <div class="sub-heading"><p>Logonavn er et digitalt bureau med en strategisk tilgang til design, kodning og drift af websites, webapplikationer og shops, der understøtter den bedste</p></div>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'about',
  props: {
    colorTheme: String
  }
}
</script>


<style lang="scss" scoped>
@import '~/assets/css/global.scss';


@keyframes imageAni {
            
    0%{
        transform: translateX(101%);
        animation-timing-function: cubic-bezier(1,0,1,1);
        opacity: 1;
    }

    35%, 55%{
        transform: translateX(0%);
    }

    100%{
        transform: translateX(-101%);
        opacity: 1;
    }
}

@keyframes contenttAni {
            
      0%{
          transform: translateY(-101%);
          animation-timing-function: cubic-bezier(1,0,1,1);
      }

      35%, 55%{
          transform: translateY(0%);
      }

      100%{
          transform: translateY(101%);
      }
  }

  
    

.about{
  --gridd: grid;
  --grid-template-columns: repeat(1, 1fr 50.4rem);

  @media (max-width: $screen-md) {
    --grid-template-columns: repeat(1, 1fr 44rem);
  }

  @media (max-width: $screen-sm) {
    --gridd: block;
  }
  position: relative;
  padding-bottom: $gutter * 1.5;
  z-index: 1;

    &-box{
      position: relative;
      margin-top: -28rem;
      width: 100%;
      display: inline-block;

      /* @media (max-width: $screen-lg) {
        margin-top: -7rem;
      } */

      > div{
        display: var(--gridd);
        grid-template-columns: var(--grid-template-columns);
        grid-template-rows: auto;

        .image-ani{
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            right: 0;
            z-index: 99;
            position: apsolute;
            background-color: var(--primary);
            //animation: imageAni 1.4s cubic-bezier(1,0,1,1) forwards;
            //animation-delay: 2s;
            opacity: 0;
        }

        .image-wrapper{
          grid-column: 1 / 2;
          grid-row: 1 / 2;
          position: relative;
          opacity: 0;
          animation: opacityAni .4s cubic-bezier(1,0,1,1) forwards;
          animation-delay: 2.7s;
          line-height: 0;
          z-index: 1;

          .image{
              width: 100%;
              height: 100%;
              object-fit: cover;
          }

          .contact-btn{
              position: absolute;
              transform: translateY(-50%);
              margin-left: var(--container-padding);
              background-color: lighten($primary, 5%);
              color: $white;
              display: flex;
              width: auto;
              height: 7.5rem;
              align-items: center;
              padding-left: 1.9em;
              transition: background-color 0.2s ease;
              opacity: 0;
              animation: opacityAni .4s cubic-bezier(1,0,1,1) forwards;
              animation-delay: 2.4s;
              z-index: 99;
              font-size: 1.6rem;

              @media (max-width: $screen-sm) {
                  display: none;
              }
              &:hover{
                  background-color: $primary;
              }

              span{
                  width: 8rem;
                  height: 100%;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  margin-left: 1.5em;
                  background: url("../assets/images/arrow-light.svg") no-repeat center $primary;
                  background-size: .6em;
              }
          }
        }

        .content-ani-wrapper{
            grid-column: 2 / 3;
            grid-row: 1 / 4;
            position: relative;
            overflow: hidden;
        }

        .content-ani{
            position: absolute;
            top: 0;
            left: 0;
            background-color: var(--secondary-dark);
            width: 100%;
            height: 100%;
            display: block;
            z-index: 2;
            animation: contenttAni 1.4s cubic-bezier(1,0,1,1) forwards;
            animation-delay: 1.6s;
            transform: translateY(-101%);
        }

        .content{
          grid-column: 2 / 3;
          grid-row: 1 / 2;
          background-color: #DF7744;
          padding: $gutter;
          animation: opacityAni .1s cubic-bezier(1,0,1,1) forwards;
          animation-delay: 2.4s;
          opacity: 0;
          position: relative;

          h1{
              margin-top: 10px;
              font-size: 3.6rem;
              font-weight: 600;
          }
          p{
              font-weight: 300;
                font-size: 1.8rem;
          }

          &__bottom{
              grid-column: 2 / 3;
              grid-row: 3 / 4;
              background-color: lighten(#DF7744, 4%);
              padding: ($gutter - 3) ($gutter - 2rem);
              list-style: none;
              margin: 0;
              display: flex;
              flex-wrap: wrap;
              animation: opacityAni .1s cubic-bezier(1,0,1,1) forwards;
              animation-delay: 2.7s;
              opacity: 0;
              position: relative;

              li{
                  height: 6rem;
                  padding: 0 2.6rem;
                  position: relative;
                  border-bottom: solid 1px;
                  border-color: rgba($black, 0.08);
                  display: flex;
                  align-items: center;

                  &:first-child{
                      img{
                          height: 1.6rem;
                      }
                  }

                  &:nth-child(1), &:nth-child(5){
                      &:after{
                          display: none;
                      }
                  }

                  &:nth-child(n+5){
                      border-bottom: none;
                  }
                  
                  &:after{
                      content: "";
                      height: 40px;
                      width: 1px;
                      background-color: rgba($black, 0.08);
                      position: absolute;
                      left: 0;
                      top: 50%;
                      margin-top: -20px;
                  }

                  img{
                      height: 2.2rem;
                  }
              }
          }
        }
        .sub-heading{
          grid-column: 1 / 2;
          grid-row: 3 / 5;
          padding-left: var(--container-padding);
          padding-right: $gutter;
          
          opacity: 0;
          animation: opacityAni .4s cubic-bezier(1,0,1,1) forwards;
          animation-delay: 2.7s;

          p{
            font-size: 2.8rem;
            @media (max-width: $screen-lg) {
              font-size: 2.3rem;
            }
            font-weight: 300;
            position: relative;
            padding-left: 23px;
            margin-top: $gutter * 2;
            display: block;
            color: $white;

            &:after{
                content: "";
                height: 100%;
                width: 3px;
                background-color: var(--primary);
                position: absolute;
                left: 0;
                top: 0;
            }
          }
        }
    }
  }
}

</style>