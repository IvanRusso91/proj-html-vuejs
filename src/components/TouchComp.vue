<template>
  <div>
    <div class="container touch">

      <div class="left">
        <p class="tou">send a message</p>
        <h2 class="title-tou">Get in <span>Touch</span></h2>
        <p class="tou-small">We will respond to your message as soon as possible.</p>

        <div class="field">
          <div class="box-field">
            <img src="../assets/img/image_1.png" alt="">
            <input type="text" placeholder="Name">
            <input type="email" placeholder="Email">
            <input type="text" placeholder="phone">
            <select name="More info">
              <option value="">More info</option>
              <option value="">JQuery</option>
              <option value="">Less</option>
              <option value="">Woo Commerce</option>
              <option value="">WordPress</option>
              <option value="">Pingdom</option>

            </select>
            <textarea rows="10" cols="30" placeholder="Message"></textarea>
            <div class="btn-box">
              <a href="#" class="btn">send</a>
            </div>
          </div>


        </div>
      </div>

      <div class="right">
        <h2>Example inc.</h2>
        <p class="right-p">Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
        <p class="right-p">Preasent diam lacus, dapibus sed imperdiet consectetur.</p>
        
        <ul>
          <li><a href="#"><i class="fa-solid fa-phone"></i>+1(305)1234-5678</a></li>
          <li><a href="#"><i class="fa-solid fa-envelope"></i>hello@ecample.com</a></li>
          <li><a href="#"><i class="fa-solid fa-location-dot"></i>Main Avenue, 987</a></li>
        </ul>
        
        <a class="btn-right" href="#">view map</a>  
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'TouchComp'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';


.touch{
  @include j-sb;
  margin-bottom: 130px;
  display: flex;
    flex-wrap: wrap;
  .left{
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    width: 900px;
    .tou{
      text-transform: uppercase;
      color: $vibrant-color;
      font-weight: bold;
      margin-top: 100px;    
    }
    .title-tou{
      padding:30px 0;
      font-size: 3rem;
      color: rgb(0, 0, 0);
      span{
        @include title;   
      }  
    }
    .tou-small{
      color: $gravel-color;
      margin-bottom: 30px;
    }
    .field{
      @include j-sb;
      .box-field{
        img{
          background-repeat: no-repeat;
          position: absolute;
          margin-top: 22px;
          margin-left: 360px;

        }
        input{
          width: 400px;
          margin-right: 30px;
          padding: 20px;
          background-color: $gN-color;
          border-radius: 10px;
          font-size: 1.1rem;
          margin-bottom: 20px;
          
        }
        select{
          width: 400px;
          margin-right: 30px;
          padding: 20px;
          background-color:$gN-color;
          border-radius: 10px;
          font-size: 1.1rem;
        }
        textarea{
          width: 830px;
          margin-right: 30px;
          padding: 20px;
          background-color: $gN-color;
          border-radius: 10px;
          font-size: 1.1rem;
          margin-bottom: 40px;
        }
        .btn-box{
          margin-top: 20px;
          .btn{
            @include btn1;
            text-transform: uppercase;
            &:hover{
              background-color: $vibrant-color;
            }
          }
        }
      } 
    }
  }
  .right{
    width: 350px;
    h2{
      margin-top: 100px;
      margin-bottom: 30px;
    }
    .right-p{
      margin-bottom: 30px;
      font-size: 1.1rem;           
      color: $gravel-color;
    }
    ul{
      padding: 0;
      li{
        margin-bottom: 50px;
        a{
          color: $sN-color;
          font-size: 1.5rem;
          i{
            color: $bL-color;
            background-color: rgba(108,160,160,0.3);
            padding: 10px 11px;
            border-radius: 50%;
            margin-right: 15px;
          }
        }
      }
    }
    .btn-right{
      @include btn2;
      color: $bL-color;
      text-transform: uppercase;
      &:hover{
        color: white;
        background-color: $sN-color;
      } 
    }
  }
}
</style>