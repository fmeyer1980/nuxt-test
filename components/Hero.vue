<template>
  <div class="hero" :class="page">
      <div class="bg-image" :style="{backgroundImage: 'url(' + imagUrl + ')', opacity: opacity}"></div>
        <div class="container container--right">
            <h1>
            <span class="heading">{{ title }}
                <span class="ani"></span>
            </span>
            </h1>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
const IMG_PATH = "/images/";

export default {
  name: 'hero',
  props: {
    page: String, 
    title: String,
    text: String,
    image: String,
    opacity: String
  },
  computed: { 
    imagUrl: function(){
      return `${IMG_PATH}${this.image}`;
    }
  },
}

</script>

<style lang="scss" scoped>
@import '~/assets/css/breakpoints.scss';

.hero.home{
    height: 76rem;

    .bg-image{
        animation-delay: 3.2s;
    }

    .container{
        transform: translateY(-9rem);
    }
}

.hero{
    height: 72.5rem;
    background-color: transparent;
    color: var(--white);
    padding-top: 0;
    position: relative;
    //padding-right: var(--container-padding);
    display: flex;

    .bg-image{
        width: 100%;
        height: 100%;
        background-size: cover;
        background-blend-mode: multiply;
        position: absolute;
        top: 0;
        left: 0;
        background-color: var(--secondary);
        opacity: 0;
        animation: opacityAni .3s ease-in forwards;
        animation-delay: 2s;
    }

   .container{
        position: relative;
        z-index: 1;
        align-self: center;
    }

    h1{
        margin-top: 0;
        margin-bottom: 0.1em;
        display: inline-block;
        font-size: 7rem;
        line-height: 0;

        .heading{
            animation: heroHeadingAni 1.4s forwards;
            animation-delay: .3s;
            animation-fill-mode: backwards;
            padding-left: 0.35em;
            font-weight: 300;
            overflow: hidden;
            display: inline-block;
            position: relative;
            line-height: 1.2em;

            &:after{
                content: "";
                height: 0.8em;
                width: 5px;
                background-color: currentColor;
                position: absolute;
                left: 0;
                top: 0;
                margin-top: 0.1em;
                animation: heroHeadingAfterAni 1.4s forwards;
            }


            .ani{
                width: 100%;
                height: 100%;
                position: absolute;
                top: 0;
                left: 0;
                z-index: 1;
                animation: slideInFromLeft 1.2s cubic-bezier(0,0,0,1) forwards;
                animation-delay: .3s;
            }
        }
    }
    
    p{
        margin-top: 0;
        font-size: 2.2rem;
        font-weight: 300;
        max-width: 70%;
        opacity: 0;
        animation: textFadeIn 1.2s cubic-bezier(0,0,0,1) forwards;
        animation-delay: 1.4s;
    }
}

</style>