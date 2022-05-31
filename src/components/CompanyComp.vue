<template>
  <div>
    <div class="box">
      <div class="company">
        <div class="ir-text">

          <p class="comp">about the network</p>
          <h2 class="title-comp"> <span>The</span> Company</h2>
          <p class="small-t">For 12 years we hae been providing audit and warranty, financial <br> advice, risk advice, taxws and related services to select clients</p>

          <div class="box-card">
            <div class="card">

              <h2 class="text-card"><i class="fa-solid fa-award"></i> Tradition </h2>
              <p class="small-t">Lorem ipsum dolor sit amet, consectetur    adipisicing elit.
              </p>

            </div>

            <div class="card">

              <h2 class="text-card"><i class="fa-solid fa-lock"></i> Security </h2>
              <p class="small-t">Lorem ipsum dolor sit amet, consectetur    adipisicing elit.
              </p>

            </div>

            <div class="card">

              <h2 class="text-card"><i class="fa-solid fa-pen-to-square"></i> Certificate </h2>
              <p class="small-t">Lorem ipsum dolor sit amet, consectetur    adipisicing elit.
              </p>

            </div>

            <div class="card">

              <h2 class="text-card"><i class="fa-solid fa-graduation-cap"></i> Expertise </h2>
              <p class="small-t">Lorem ipsum dolor sit amet, consectetur    adipisicing elit.
              </p>

            </div>
          </div>

          <div class="btn">
            <a class="left-btn" href="#">get in toach</a>
            <a class="right-btn" href="#">read more</a>
          </div>

        </div>
      </div>

      <div class="sfondo"></div>
      
    </div>
    <div class="bull"></div>
    <div class="bull2"></div>
  </div>
</template>

<script>
export default {
  name:'CompanyComp'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';

.box{
  @include j-sb;
  .company{
    width: 50%;
    background-color: $shark-color;
    padding-bottom: 150px;
    .ir-text{
      height: 100%;
      width: 70%;
      margin-left: 285px;
      .comp{
        text-transform: uppercase;
        color: $vibrant-color;
        font-weight: bold;
        margin-top: 100px ;
      }
      .title-comp{
        padding: 50px 0;
        font-size: 3rem;
        color: white;
        span{
          background-color: rgba(3,132,132,0.2);
          padding: 10px 15px;
          border-radius: 5px;
          color: white;
        }
      }
      .small-t{
        font-size: 1.1rem;
        color: $pumice-color;
      }
      .box-card{
        padding-top: 20px;
        padding-bottom: 100px;
        display: flex;
        flex-wrap: wrap;
        .card{
          margin-top: 50px;
          width: 300px;

          .text-card{
            color: white;
            padding-bottom: 30px;
            font-size: 2rem;
            i{
              color: $vibrant-color;
            }
          }
        } 
      }
      .btn{
        text-transform: uppercase;
        .left-btn{
          @include btn1;
          margin-right: 40px;
          &:hover{
            background-color: $vibrant-color;
          }
        }
        .right-btn{
          @include btn3;
          &:hover{
            color: white;
            background-color: $sN-color;
          }
        }
      }  
    }
  }
  .sfondo{
    width: 50%;
    background-image: url(../assets/img/about-4.jpg);
    background-position: center;
    background-size: cover;
  }
}
.bull{
  @include bull;
  margin-top: -65px;
}
.bull2{
  @include bull;
  margin-top: -65px; 
}
</style>