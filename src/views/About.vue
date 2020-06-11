<template>
  <div class="about mw1440 padding-tb-50">
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
        <div class="box box-first">
          <div class="text-box">
            <div class="j-head uppercase">sample</div>
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</div>
          </div>
          <div class="img-box">
            <img src="../assets/about/01.jpg" alt="">
          </div>
        </div>

        <div class="box box-second">
          <div class="img-box">
            <img src="../assets/about/02.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-head uppercase">sample</div>
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</div>
          </div>
        </div>

        <div class="box">
          <div class="text-box">
            <div class="j-head uppercase">sample</div>
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</div>
          </div>
          <div class="img-box">
            <img src="../assets/about/03.jpg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  .main-img-box{
    position: relative;
    .img-box{
      height: 50vh;
      background-image: url(../assets/about-main-img.jpg);
      background-repeat: no-repeat;
      background-position: center top;
      background-size: cover;
      .bg-opacity{
        background-color: rgba(0, 0, 0, .5);
        height: 100%;
        font-size: 100px;
        font-weight: bold;
        color: #fff;
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
  }

  .service{
    .box{
      color: #fff;
      display: flex;
      justify-content: space-between;
      .text-box{
        width: 60%;
        padding-right: 50px;
        line-height: 1.5;
      }
      .img-box{
        width: 40%;
        img{ width: 100%; }
      }
    }
    .box-first{
      .text-box{
        margin-top: -34px;
      }
      .img-box{
        margin-top: -70px;
      }
    }
    .box-second{
      margin: 30px 0;
      .text-box{
        padding-left: 50px;
        padding-right: 0;
      }
    }
  }


/* 반응형 */
  @media (max-width: 1080px) {
    .service{
      .box-first{
        .img-box{ margin-top: 0; }
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
      .box{
        flex-direction: column-reverse;
        .text-box{
          width: 100%;
          padding-right: 0;
        }
        .img-box{
          width: 100%;
          margin-bottom: 30px;
          img{ width: 80%; margin: 0 auto; }
        }
      }
      .box-first{ .text-box{ margin-top: 0px; } }
      .box-second{
        flex-direction: column;
        margin: 30px 0;
        .text-box{ padding-left: 0; }
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
  }
</style>