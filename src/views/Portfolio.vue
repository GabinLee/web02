<template>
  <div class="portfolio mw1440 padding-tb-50">
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
        <div class="box">
          <img src="../assets/portfolio/09.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/10.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/11.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
        <div class="box">
          <img src="../assets/portfolio/12.jpg" alt="">
          <div class="j-title">sample</div>
          <div class="j-text">You can change this text.</div>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
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


/* 반응형 */
  @media (max-width: 1080px) {
  }

  @media (max-width: 768px) {
    .img-group{
      .group{
        .box{
          width: calc(33.33333% - 20px);
        }
      }
    }
  }

  @media (max-width: 500px) {
    .img-group{
      .group{
        .box{
          width: calc(50% - 20px);
          padding: 15px;
        }
      }
    }
  }

</style>