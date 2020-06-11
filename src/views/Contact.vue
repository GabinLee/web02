<template>
  <div class="contact mw1440 padding-tb-50">
    <div class="main-img-box">
      <div class="img-box"></div>
    </div>

    <div class="contact padding-50">
      <div class="j-head-opacity">contact</div>
      <div class="group">
        <div class="info-box">
          <div class="j-head uppercase">sample</div>
          <div class="j-text">
            <v-icon>mdi-map-marker</v-icon>
            <div class="info-contents">경기도 시흥시 서울대학로</div>
          </div>
          <div class="j-text">
            <v-icon>mdi-phone</v-icon>
            <div class="info-contents">010-0000-0000</div>
          </div>
          <div class="j-text">
            <v-icon>mdi-email</v-icon>
            <div class="info-contents">sample@gamil.com</div>
          </div>
        </div>

        <div class="question-box fs16">
          <textarea name="your-message" aria-required="true" placeholder="Message"></textarea>

          <div class="input-box">
            <input type="text" name="first-name" value="" placeholder="Your name">

            <input type="text" name="first-name" value="" placeholder="Your email">
          </div>

          <button class="uppercase fs14">send</button>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.main-img-box{
  .img-box{
    height: 50vh;
    background-image: url(../assets/contact-main-img.jpg);
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
  }
}
.contact{
  color: #fff;
  .group{
    display: flex;
    justify-content: space-between;
  }
  .info-box{
    width: 50%;
    margin-top: -34px;
    padding: 0 50px 0 90px;
    .j-text{
      margin-bottom: 16px;
      display: flex;
      .v-icon{
        color: #fff;
        margin-right: 20px;
      }
    }
  }

  .question-box{
    width: 50%;
    margin-top: -34px;
    textarea{
      width: 100%;
      height: 200px;
      background-color: #bebebe;
      margin-bottom: 20px;
      padding: 14px 10px;
      transition: .2s;
    }
    .input-box{ margin: 0 -10px 20px; }
    input{
      background-color: #bebebe;
      width: calc(50% - 20px);
      margin: 0 10px;
      padding: 14px 10px;
    }
    textarea::placeholder, input::placeholder{ color: #fff; }
    textarea:focus::placeholder, input:focus::placeholder{ color: #000; }
    textarea:focus, input:focus{ outline: none; color: #000; }
    button{
      background-color: #777;
      color: #fff;
      padding: 14px 24px;
    }
    button:hover{
      opacity: .8;
    }
  }
}


/* 반응형 */
  @media (max-width: 1080px) {
    .contact{
      .info-box{
        margin-top: -28px;
        padding: 0 50px 0 10px;
      }
      .question-box{ margin-top: -28px; }
    }
  }

  @media (max-width: 768px) {
    .contact{
      .group{ flex-direction: column; }
      .info-box{
        width: 100%;
        margin-top: -20px;
        margin-bottom: 30px;
        padding: 0 50px 0 10px;
      }
      .question-box{
        width: 100%;
        margin-top: -20px;
      }
    }
  }

  @media (max-width: 500px) {
    .contact{
      .group{ flex-direction: column; }
      .info-box{
        width: 100%;
        margin-top: -16px;
        margin-bottom: 30px;
        padding: 0 50px 0 10px;
      }
      .question-box{
        width: 100%;
        margin-top: -16px;
      }
    }
  }

</style>