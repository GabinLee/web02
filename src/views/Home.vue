<template>
  <div class="home mw1440 padding-tb-50">
    <div class="main-img-box">
      <div class="img-box">
        <div class="bg-opacity">
          <div class="logo logo-font">Sample</div>
        </div>
      </div>
    </div>
    <div class="service padding-50">
      <div class="j-head-opacity">service</div>
      <div class="group">
        <div class="box">
          <v-icon>mdi-cellphone-iphone</v-icon>
          <div class="text-box">
            <div class="j-title">sample</div>
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. </div>
            <a href="/about" class="a-box fs16 uppercase">more
              <v-icon>mdi-chevron-right</v-icon>
            </a>
          </div>
        </div>
        <div class="box">
          <v-icon>mdi-laptop-mac</v-icon>
          <div class="text-box">
            <div class="j-title">sample</div>
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry.</div>
            <a href="/about" class="a-box fs16 uppercase">more
              <v-icon>mdi-chevron-right</v-icon>
            </a>
          </div>
        </div>
        <div class="box">
          <v-icon>mdi-monitor-cellphone</v-icon>
          <div class="text-box">
            <div class="j-title">sample</div>
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry.</div>
            <a href="/about" class="a-box fs16 uppercase">more
              <v-icon>mdi-chevron-right</v-icon>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="img-group padding-tb-50">
      <div class="group">
        <div class="box">
          <img src="../assets/portfolio/01.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/02.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/03.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/04.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/05.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/06.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/07.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/08.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
      </div>
    </div>
    <div class="history padding-50">
      <div class="j-head-opacity">history</div>
      <div class="group">
        <div class="text-box">
          <div class="j-head">
            <span class="uppercase">sample</span>
          </div>
          <div class="contents j-text">
            <div class="year">
              <strong>2020</strong>
              <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
            </div>
            <div class="year">
              <strong>2019</strong>
              <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
            </div>
            <div class="year">
              <strong>2018</strong>
              <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
            </div>
            <div class="year">
              <strong>2017</strong>
              <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
            </div>
          </div>
        </div>
        <div class="img-box">
          <img src="../assets/history-img.jpg" alt="">
        </div>
      </div>
    </div>
  </div>
</template>


<script>
  export default {
  }
</script>


<style lang="scss" scoped>
.main-img-box{
  position: relative;
  .img-box{
    height: 50vh;
    background: url(../assets/home-main-img.jpg) no-repeat bottom center / cover;
    .bg-opacity{
      background-color: rgba(0, 0, 0, .2);
      height: 100%;
      padding-top: 100px;
      font-size: 100px;
      font-weight: bold;
      color: #fff;
      text-align: center;
    }
  }
}

.service{
  .group{
    margin: -50px -20px 0 -20px;
    color: #fff;
    display: flex;
    flex-wrap: wrap;
  }
  .box{
    width: 33.33333%;
    margin-bottom: 20px;
    padding: 20px;
    display: flex;
  }
  .box:last-child{ margin-bottom: 0; }
  .v-icon{
    width: 80px;
    height: 80px;
    margin-right: 20px;
    font-size: 80px;
    color: #fff;
  }
  .text-box{
    .j-text{ line-height: 1.5; margin-bottom: 30px; }
    .a-box{
      width: 100px;
      height: 24px;
      font-weight: bold;
      display: flex;
      align-items: center;
      justify-content: space-between;
      transition: .2s;
      .v-icon{
        width: auto;
        height: auto;
        margin-right: 0;
        font-size: 20px;
      
      }
    }
    .a-box:hover{ color: #e5e5e5; }
    .a-box:hover .v-icon{ color: #e5e5e5; }
  }
}

.img-group{
  .group{
    margin-left: -10px;
    margin-right: -10px;
    display: flex;
    flex-wrap: wrap;
    .box{
      background-color: #f7f7f7;
      width: calc(25% - 20px);
      margin: 0 10px 30px 10px;
      padding: 20px;
      text-align: center;
      img{
        width: 100%;
        margin-bottom: 20px;
      }
    }
  }
}

.history{
  .group{
    color: #fff;
    display: flex;
    justify-content: space-between;
    .text-box{
      width: 60%;
      margin-top: -34px;
      padding-right: 50px;
      .contents{
        .year{
          margin-bottom: 16px;
          display: flex;
          justify-content: space-between;
          strong{ font-size: 20px; }
          p{ width: calc(100% - 70px); }
        }
      }
    }
    .img-box{
      width: 40%;
      margin-top: -64px;
      img{
        width: 100%;
      }
    }
  }
}



/* 반응형 */
  @media (max-width: 1080px) {
    .service{
      .box{ width: 50%; }
    }
    .history{
      .group{
        .img-box{ margin-top: -30px; }
      }
    }
  }

  @media (max-width: 768px) {
    .main-img-box{
      .img-box{
        .bg-opacity{
          font-size: 80px;
        }
      }
    }
    .service{
      .group{ margin: -36px -20px 0 -20px; }
      .box{ width: 100%; }
      .v-icon{
        width: 60px;
        height: 60px;
        font-size: 60px;
      }
      .text-box{ .j-text{ margin-bottom: 20px; } }
    }
    .img-group{
      .group{
        .box{
          width: calc(33.33333% - 20px);
        }
      }
    }
    .history{
      .group{
        flex-direction: column-reverse;
        .text-box{
          width: 100%;
          margin: 0;
          padding-right: 0;
        }
        .img-box{
          width: 100%;
          margin-top: -10px;
          margin-bottom: 30px;
          img{ width: 50%; margin: 0 auto; }
        }
      }
    }


  }

  @media (max-width: 500px) {
    .main-img-box{
      .img-box{
        .bg-opacity{
          font-size: 50px;
        }
      }
    }
    .img-group{
      .group{
        .box{
          width: calc(50% - 20px);
          padding: 15px;
        }
      }
    }
    .service{
      .group{ margin: -36px 0 0 0; }
      .box{ width: 100%; margin-bottom: 0; padding: 30px 0; }
      .v-icon{
        width: 40px;
        height: 40px;
        font-size: 40px;
      }
      .text-box{ .j-text{ margin-bottom: 20px; } }
    }
    .history{
      .group{
        flex-direction: column-reverse;
        .text-box{
          margin: 0;
          width: 100%;
        }
        .img-box{
          width: 100%;
          margin-top: -10px;
          img{ width: 50%; margin: 0 auto; }
        }
      }
    }
  }
</style>