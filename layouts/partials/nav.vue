<template>
  <header>
      <div class="logo-wrapper">
        <nuxt-link class="logo" to="/"><img src="@/assets/images/logo.png" alt="" /></nuxt-link>
      </div>
      <nav class="nav">
        <ul class="main-menu">
          <li><nuxt-link to="/" exact>Forside</nuxt-link></li>
          <li><nuxt-link to="/service">Service</nuxt-link></li>
          <li><nuxt-link to="/cases">Cases</nuxt-link></li>
          <li><nuxt-link to="/about">Om os</nuxt-link></li>
          <li><nuxt-link to="/kontact">Kontakt</nuxt-link></li>
        </ul>
      </nav>
      <div class="contact">
        <li><a href="">E: mail@konform.com</a></li>
        <li><a href="">T: 33 11 05 11</a></li>
      </div>
  </header>
</template>

<script>

export default {

}
</script>


<style lang="scss">
@import '~/assets/css/global.scss';

header.dark{
  color: $black;

  .logo-wrapper{
    background-color: $lightGrayDark;
  }

}


[class*="cases-"]{

  header{
    color: #fff;
    transition: .2s;
    transition-delay: .4s;

    .logo-wrapper{
      background-color: #eee;
      transition: .2s;
      transition-delay: .4s;
    }

    .main-menu{

      li{
        
        .nuxt-link-exact-active, .nuxt-link-active{
          transition: .2s;
          transition-delay: .4s;
        }
      }
    }
  }

  .contact{
    transition: .2s;
    transition-delay: .4s;

    li{

      &:after{
        background-color: rgba($white, 0.05);
        transition: .2s;
        transition-delay: .4s;
      }
      &:last-child{
        color: rgba($white, 0.7);
        transition: .2s;
        transition-delay: .4s;
      }
    }
  }
  
}

.cases{

  header{
    color: #111;
    

    .logo-wrapper{
      background-color: #333;
    }


    .main-menu{

      li{
          position: relative;

          &:after{
              background-color: rgba($black, 0.05);
          }
      }
    }

    .contact{

    li{

      &:after{
        background-color: rgba($black, 0.05);
      }
      &:last-child{
        padding-right: 0;
        color: rgba($black, 0.7);
      }

      a{
        height: 100%;
        display: flex;
        align-items: center;
        color: inherit;
      }
      
    }
    }



  }
}

header{
  position: absolute;
  width: 100%;
  height: 5rem;
  display: flex;
  font-size: 0.9em;
  z-index: 101;
  color: var(--white);

.logo-wrapper{
    background-color: #eee;
    padding-left: 2.8rem;
    padding-right: 2.8rem;
    width: 18rem;
    display: flex;
    align-items: center;

    .logo{
      height: 1.4em;
      display: block;


      img{
        height: 100%;
      }

    }

  }

    .main-menu{
      display: flex;
      height: 100%;
      @extend .listStyleNone;
      
      li{
          position: relative;

          &:after{
              content: "";
              height: 40px;
              width: 1px;
              background-color: rgba($white, 0.05);
              position: absolute;
              top: 50%;
              right: 0;
              margin-top: -20px;
          }

          &:last-child:after{
              display: none;
          }

          a{
              color: inherit;
              padding: 0 1.8em;
              display: block;
              background-color: transparent;
              height: 100%;
              display: flex;
              align-items: center;
          }

          .nuxt-link-exact-active, .nuxt-link-active{
              
              color: var(--white);
              background-color: var(--primary);
              /* animation: header-links .3s ease-in forwards;

              @keyframes header-links{
                0%{
                  background-color: transparent;
                }
                100%{
                  background-color: var(--primary);
                }
              } */

          }

      }
  }
  .contact{
    display: flex;
    @extend .listStyleNone;
    margin-left: auto;
    padding-right: 2.8rem;
    color: var(--primary);

    li{
      position: relative;
      padding: 0 1.8em;
      &:after{
        content: "";
        height: 40px;
        width: 1px;
        background-color: rgba($white, 0.05);
        position: absolute;
        top: 50%;
        right: 0;
        margin-top: -20px;
      }
      &:last-child{
        padding-right: 0;
        color: rgba($white, 0.5);

        &:after{
          display: none;
        }

      }

      a{
        height: 100%;
        display: flex;
        align-items: center;
        color: inherit;
      }
      
    }

    @media (max-width: $screen-lg) {
     flex-direction: column;
      justify-content: center;
      align-items: flex-end;

      li{
        padding: 0;
          &:after{
          display: none;
        }
      }
    }
  }
}

</style>

