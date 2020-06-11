<template>
  <div class="all-container">
    <header>
      <div class="h-container mw1440">
        <div class="logo-box">
          <router-link to="/" class="logo-font uppercase">Sample</router-link>
        </div>

        <nav class="nav-box fs16">
          <router-link to="/" @click.native="clickNavItem(1)" :class="{checked : selectedNavItem == 1 ? true : false}">
            <span>home</span>
          </router-link>
          <router-link to="/about" @click.native="clickNavItem(2)" :class="{checked : selectedNavItem == 2 ? true : false}">
            <span>about us</span>
          </router-link>
          <router-link to="/contact" @click.native="clickNavItem(3)"  :class="{checked : selectedNavItem == 3 ? true : false}">
            <span>contact</span>
          </router-link>
          <router-link to="/portfolio" @click.native="clickNavItem(4)" :class="{checked : selectedNavItem == 4 ? true : false}">
            <span>portfolio</span>
          </router-link>
        </nav>

        <div class="mobile-menu-btn-box">
          <v-app-bar-nav-icon @click="openMobileNav" />
        </div>
      </div>
      <div class="mobile-nav-box" id="mobile-nav-box">
        <div class="group fs16 uppercase" id="group">
          <div class="close-item">
            <button v-ripple @click="closeMobileNav">
              <v-icon>mdi-close</v-icon>
            </button>
          </div>
          <div class="nav-item" v-ripple>
            <a href="/">home</a>
          </div>
          <div class="nav-item" v-ripple>
            <a href="/about">about us</a>
          </div>
          <div class="nav-item" v-ripple>
            <a href="/contact">contact</a>
          </div>
          <div class="nav-item" v-ripple>
            <a href="/portfolio">portfolio</a>
          </div>
        </div>
      </div>
    </header>

    <main>
      <router-view/>
      <button class="top-button" onClick="javascript:window.scrollTo(0,0)" v-ripple>
        <v-icon>mdi-arrow-up</v-icon>
      </button>
    </main>
    
    <footer class="padding-tb-50">
      <div class="f-container mw1440">
        <div class="f-group">
          <div class="f-intro">
            <div class="j-head logo-font">Sample</div>
            <div>
              Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean sit massa cum sociis theme.
            </div>
          </div>
          <div class="f-contact">
            <div class="j-head uppercase">contact</div>
            <div class="address">
              <v-icon>mdi-map-marker</v-icon>
              <div>경기도 시흥시 서울대학로</div>
            </div>
            <div class="mail">
              <v-icon>mdi-email-outline</v-icon>
              <div>sample@gamil.com</div>
            </div>
          </div>
          <div class="f-insta-feed">
            <div class="j-head uppercase">instagram feed</div>
            <div class="img-group">
              <div class="img-box">
                <img src="./assets/footer/01.jpg" alt="">
              </div>
              <div class="img-box">
                <img src="./assets/footer/02.jpg" alt="">
              </div>
              <div class="img-box"> 
                <img src="./assets/footer/03.jpg" alt="">
              </div>
              <div class="img-box"> 
                <img src="./assets/footer/04.jpg" alt="">
              </div>
              <div class="img-box"> 
                <img src="./assets/footer/05.jpg" alt="">
              </div>
              <div class="img-box"> 
                <img src="./assets/footer/06.jpg" alt="">
              </div>
              <div class="img-box"> 
                <img src="./assets/footer/07.jpg" alt="">
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>


<script>
  export default {
    data: () => ({
      selectedNavItem: 1
    }),
    methods: {
      openMobileNav() {
        if(window.innerWidth <= 500){
          document.getElementById("mobile-nav-box").style.width = "100%";
          document.getElementById("group").style.width = "75%";
        } else{
          document.getElementById("mobile-nav-box").style.width = "100%";
          document.getElementById("group").style.width = "50%";
        }
      },
      closeMobileNav() {
        document.getElementById("mobile-nav-box").style.width = "0%";
        document.getElementById("group").style.width = "0%";
      },
      clickNavItem(index) {
        this.selectedNavItem = index;
      }
    }
  }
</script>


<style lang="scss">
/* 전체 배경: b2b2b2, opacity-title: bebebe, footer: 999; white-font-hover: e5e5e5, btn: #777 */

/* default setting */
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Montserrat', 'Nanum Gothic'; word-break:break-all; }
  html, body{ font-size: 10px; }
  a{ display: inline-block; text-decoration: none; color: inherit; }
  button{ background-color: transparent; border: none; cursor: pointer; }
  button:focus{ outline: none; }
  img{ display: block; }

  .mw1440{ max-width: 1440px; margin: 0 auto; padding-left: 40px; padding-right: 40px; }
  .fs16{ font-size: 16px; }
  .fs14{ font-size: 14px; }

  .j-head-opacity{ font-size: 120px; text-transform: uppercase; font-weight: bold; color: #bebebe; }
  .j-head{ font-size: 24px; margin-bottom: 24px; }
  .j-title{ font-size: 20px; margin-bottom: 20px; text-transform: uppercase; }
  .j-text{ font-size: 16px; }
  .logo-font{ font-family: 'Delius Swash Caps', cursive; }
  .padding-50{ padding: 50px; }
  .padding-tb-50{ padding-top: 50px; padding-bottom: 50px; }
  .padding-lr-50{ padding-left: 50px; padding-right: 50px; }
  .uppercase{ text-transform: uppercase; }


  .all-container{ overflow: hidden; }

/* header */
  header{
    height: 100px;
    .logo-box{
      height: inherit;
      a{
        height: 100%;
        line-height: 90px;
        color: #fff;
        font-size: 50px;
      }
    }
    .nav-box{
      color: #fff;
      text-transform: uppercase;
      a{
        height: 100%;
        line-height: 100px;
        margin-right: 20px;
        padding: 0 10px;
        position: relative;
      }
      a:last-child{ margin-right: 0; }
      span{
        opacity: .8;
      }
      span:before{
        content: "";
        width: calc(100% - 20px);
        border-top: 3px solid #1BB850;
        border-bottom: 3px solid #1BB850;
        opacity: 0;
        transition: all 0.35s ease;
        -webkit-transition: all 0.35s ease;
        position: absolute;
        top: 50%;
        bottom: 50%;
        left: 10px;
      }
      a:hover{
        color: #fff;
        font-weight: bold;
        transition: all 0.2s ease;
      }
      .checked{
        color: #fff;
        font-weight: bold;
      }
      a:hover span:before, .checked span:before{
        opacity: 1;
        top: 32%;
        bottom: 32%;
      }
      
    }
  }
  .h-container{
    height: inherit;
    display: flex;
    justify-content: space-between;
    position: relative;
  }
  .mobile-menu-btn-box{
    display: none;
    .v-btn--icon.v-size--default{
      color: #1BB850;
      width: 40px;
      height: 40px;
      margin: 20px 0;
      .v-icon{
        color: #fff;
        width: 30px;
        height: 30px;
        font-size: 30px;
      }
    }
    .v-btn--icon.v-size--default:hover{ background-color: rgba(27, 184, 80, .2); }
  }
  .mobile-nav-box{
    background-color: rgba(0, 0, 0, .8);
    width: 0;
    height: 100vh;
    overflow: hidden;
    position: fixed;
    top: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    z-index: 999;
    .group{
      background-color: #fff;
      width: 0%;
      height: 100%;
      margin-left: auto;
      transition: .5s;
    }
    .close-item{
      padding: 20px 40px;
      text-align: right;
      button{
        color: #1BB850;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        i{ color: #000; }
      }
      button:hover{
        background-color: rgba(27, 184, 80, .2);
        transition: .2s;
      }
    }
    .nav-item{
      margin: 10px;
      border-radius: 5px;
      padding: 20px 40px;
      color: #1bb850;
      text-align: center;
      cursor: pointer;
      a{ color: #000; }
    }
    .nav-item:hover{ background-color: rgba(27, 184, 80, .2); }
  }


/* main */
  main{ display: flex; justify-content: center; }
  .top-button{
    background-color: rgb(119, 119, 119);
    width: 36px;
    height: 36px;
    border-radius: 50%;
    position: fixed;
    bottom: 40px;
    right: 40px;
    .v-icon{ color: #fff !important; }
  }


/* footer */
  footer{
    background-color: #999;
    color: #fff;
    font-size: 14px;
    margin-top: auto;
  }
  .f-group{
    margin: 0 -10px;
    display: flex;
    flex-wrap: wrap;
  }
  .f-intro{
    width: 25%;
    padding: 0 10px;
    img{
      height: 30px;
    }
  }
  .f-contact{
    width: 25%;
    padding: 0 10px;
    .address{
      margin-bottom: 16px;
      display: flex;
    }
    .mail{ display: flex; }
    .theme--light.v-icon{ color: #fff; margin-right: 14px; }
  }
  .f-insta-feed{
    width: 50%;
    padding: 0 10px;
    .img-group{
      margin: 0 -5px;
      display: flex;
    }
    .img-box{
      width: 14.28571%;
      padding: 0 5px;
      img{ width: 100%; }
    }
  }


/* 반응형 */
  @media (max-width: 1080px) {
    .j-head-opacity{ font-size: 100px;}
    header{
      height: 80px;
      .nav-box{ display: none; }
      .mobile-menu-btn-box{ display: block; margin-right: -10px; }

      .mobile-nav-box{ display: block; }
    }

    .f-intro{ width: 30%; }

    .f-contact{ width: 30%; }

    .f-insta-feed{ width: 40%; }
  }

  @media (max-width: 768px) {
    /* default setting */
      .j-head-opacity{ font-size: 70px;}
      .j-head{ font-size: 22px; margin-bottom: 20px; }
      .j-title{ font-size: 18px; margin-bottom: 16px; }
      .j-text{ font-size: 14px; }
      .fs16{ font-size: 14px; }
      .fs14{ font-size: 12px; }

      .padding-50{ padding: 30px 0; }
      .padding-tb-50{ padding-top: 30px; padding-bottom: 30px; }
      .padding-lr-50{ padding-left: 30px; padding-right: 30px; }


    .f-intro{ width: 50%; margin-bottom: 30px; }
    .f-contact{ width: 50%; margin-bottom: 30px; }
    .f-insta-feed{ width: 100%; }
  }

  @media (max-width: 500px) {
    /* default setting */
      .mw1440{ padding-left: 20px; padding-right: 20px; }
      .j-head-opacity{ font-size: 50px;}
      .j-head{  margin-bottom: 16px; }
      .j-title{ margin-bottom: 12px; }
      .j-text{ font-size: 12px; }
      .fs16{ font-size: 12px; }
      .fs14{ font-size: 10px; }

      .padding-50{ padding: 20px; }
      .padding-tb-50{ padding-top: 20px; padding-bottom: 20px; }
      .padding-lr-50{ padding-left: 20px; padding-right: 20px; }

    header{
      height: 60px;
      .logo-box{
        a{
          line-height: 60px;
          font-size: 30px;
        }
      }
    }
    .mobile-menu-btn-box{
      .v-btn--icon.v-size--default{
        margin: 10px 0;
        .v-icon{ font-size: 24px; }
      }
    }
    .mobile-nav-box{
      .close-item{ padding: 10px; }
    }

    .f-intro{ width: 100%; margin-bottom: 30px; }
    .f-contact{ width: 100%; margin-bottom: 30px;
      .address{ margin-bottom: 10px; }
    }
    .f-insta-feed{ width: 100%; }
  }


</style>
