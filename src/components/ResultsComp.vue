<template>
  <div>
    <div class="chess">
      <div class="container ir-res">
        <p class="res">what are we doing</p>
        <h2 class="title-res"><span>Results</span> in Numbers</h2>
        <nav>
          <ul>
            <li><a href="#"><span>128</span> <br> Certifications</a></li>
            <li><a href="#"><span>230</span> <br> Employess</a></li>
            <li><a href="#"><span>517</span> <br> Customers</a></li>
            <li><a href="#"><span>94</span> <br> countries Served</a></li>
          </ul>
        </nav>
      </div>
    </div>

    <div class="box-res">
    <ul class="container">
      <li><a href="#"><img src="../assets/img/logo-4.png" alt=""></a></li>
      <li><a href="#"><img src="../assets/img/logo-5.png" alt=""></a></li>
      <li><a href="#"><img src="../assets/img/logo-1.png" alt=""></a></li>
      <li><a href="#"><img src="../assets/img/logo-2.png" alt=""></a></li>
      <li><a href="#"><img src="../assets/img/logo-3.png" alt=""></a></li>
      <li><a href="#"><img src="../assets/img/logo-4.png" alt=""></a></li>
    </ul>  
    </div>
  </div>
</template>

<script>
export default {
  name:'ResultsComp'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';

.chess{
  height: 600px;
  background-image: url(../assets/img/bg-7.jpg);
  background-size: cover;
  background-position: center;
  .ir-res{
    padding-top: 100px;
    text-align: center;
    margin-top: 200px;
    .res{
      text-transform: uppercase;
      color: $vibrant-color;
      font-weight: bold;    
    }
    .title-res{
      padding: 50px 0;
      font-size: 3rem;
      color: white;
      span{
        padding: 10px 15px;
        background-color: rgba(3,132,132,0.2);
        color: $bL-color;
        border-radius: 5px;
        color: white;
      }  
    }
    nav{
      margin-top: 50px;
      ul{
        display: flex;
          justify-content: space-between;
        li{
          a{
            font-size:2rem;
            font-weight: bolder;
            color: white;
            span{
              color: $bL-color;
              font-size: 3rem;
            }
          }
        }
      }
    }
  }
}
.box-res{
  height: 200px;
  background-color: $shark-color;
  ul{
    display: flex;
    justify-content: space-between;
    padding-top: 80px;
  }
}


</style>