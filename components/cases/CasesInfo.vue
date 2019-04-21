<template>
  <div class="case-info">
      <div class="case-info__box">
          <span>Service</span>
          <p>UX/UI, Prototyping</p>
      </div>
      <div class="case-info__box">
          <span>Teknologi</span>
          <p>Invision studio, Gridsome, Vue</p>
      </div>
      <div class="case-info__box">
          <span>Client</span>
          <p>Personal project</p>
      </div>
      <a href="/" class="case-info__box button">
          <span>Website link</span>
          <p>baumundpferdgarten.com</p>
      </a>
</div>
</template>

<script>

export default {


}

</script>

<style lang="scss" scoped>

.case-info{
    position: absolute;
    color: var(--white);
    background-color: var(--secondary-dark);
    display: flex;
    margin-right: var(--container-padding);
    padding-left: var(--container-padding);
    transform: translateY(-50%);
    z-index: 1;
    height: 6rem;
    align-items: center;
    animation: fadeInAni .3s ease-in;
    animation-delay: 1.7s;
    animation-fill-mode: backwards; 
    /* margin-top: -3rem; */

    &__box{
      position: relative;
      flex-grow: 1;
      padding: 0 3rem;
      &:first-child{
        padding-left: 0;
      }
 
      &:first-child:after, &:last-child:after{
        display: none;
      }
      &:after{
          content: "";
          height: 100%;
          width: 1px;
          background-color: var(--white);
          position: absolute;
          left: 0;
          top: 0%;
          opacity: .05;
      }

      span{
        opacity: .4;
        font-size: .75rem;
      }

      p{
        margin: 0;
        font-size: .9rem;
      }
    }

    .button{
      background-color: var(--primary);
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      color: var(--white);
      padding-left: 2rem;
    }
}

</style>