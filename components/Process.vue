<template>
    <div class="process">
        <div class="container container--right">
            <div class="step" data-aos="text-ani-up" data-aos-once="true">
                <img src="../assets/images/process-step-2.png" alt=""/>
                <h3 class="heading h4">1. User experience</h3>
                <p>Digital design and development is at the core of what we do. Web platforms, e-commerce shops, front-end development.</p>
            </div>
            <div class="step" data-aos="text-ani-up" data-aos-delay="200" data-aos-once="true">
                <img src="../assets/images/process-step-2.png" alt=""/>
                <h3 class="heading h4">2. Visual design</h3>
                <p>Design and development core of what we do. Web platforms, front-end development, brand logos, creative direction.</p>
            </div>
            <div class="step" data-aos="text-ani-up" data-aos-delay="400" data-aos-once="true">
                <img src="../assets/images/process-step-2.png" alt=""/>
                <h3 class="heading h4">3. Webudvikling & cms</h3>
                <p>Is at the core of what we do. Web platforms, e-commerce shops, front-end development, brand logos.</p>
            </div>
        </div>
    </div>
</template>

<script>

export default {
  name: 'process',
  props: {
    colorTheme: String
  }
}
</script>


<style lang="scss" scoped>
@import '~/assets/css/global.scss';

.process{
    background-size: cover;
    color: $white;
    padding: ($gutter * 1.5) var(--container-padding) ($gutter * 1.5) 0;
    background-color: lighten($tertiary, .3);

     > div{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        grid-column-gap: $gutter * 2;

        .step{
            position: relative;

            &:first-child:after{
                display: none;
            }
            &:after{
                content: "";
                height: 100%;
                width: 1px;
                background-color: rgba($white, 0.05);
                position: absolute;
                left: -$gutter;
                top: 0;
            }

            img{
                height: 27px;
            }

            .heading{
                margin-top: 0.6rem;
            }

            p{
                opacity: 0.7;
            }
        }
     }
}

</style>