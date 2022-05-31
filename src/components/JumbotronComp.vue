<template>
<div>
  <div class="jumbo">
    <div class="container box-jumbo">
      <div class="c-left">
        <img src="../assets/img/logo.png" alt="">
      </div>
      <div class="c-right">
        <nav>
          <ul>
            <li  v-for="(item, index) in menu" :key="`a-${index}`"><a href="#">{{item.name}}</a></li>
            <li><a class="btn">get in touch</a></li>
          </ul>
        </nav>
      </div>
    </div>
    <div class="jumbo-text">
      <h1>Ready <span>Team</span></h1>
      <p>No matter what your company needs, we will be <br> ready to assist you in the best possible way.</p>
      <a class="btn-left" href="#">get in touch</a>
      <a class="btn-right" href="#"> read more</a>
    </div>
    
    <div class="right-box">
      <div class="box"></div>
      <div class="box-active"></div>
      <div class="box"></div>
    </div>
    
  </div>
</div> 
</template>

<script>
export default {
  name: 'JumbotronComp',

  data(){
    return{
      menu:[
        {
          href: '#',
          name: 'home',
        },
        {
          href: '#',
          name: 'services',
        },
        {
          href: '#',
          name: 'about',
        },
        {
          href: '#',
          name: 'projects',
        },
        {
          href: '#',
          name: 'results',
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';

 .jumbo{
  height: calc(100vh - 60px);
  background-image: url(../assets/img/bg-parallax.PNG);
  background-size: cover;
  background-position: center;
   .box-jumbo{
     @include j-sb;
     .c-left{
       img{
         width: 160px;
         padding-top: 20px;
       }
     }
     .c-right{
       display: flex;
       padding-top: 35px;
       justify-content: end;
       nav{
         ul{
           li{
             display: inline-block;
             margin-left: 20px;
             cursor: default;
             a{
               color: $shark-color;
               text-transform: uppercase; 
               font-weight: bold;
              
               &:hover{
                 color: $bL-color;
               }   
             }
             .btn{
               @include btn1;           
               &:hover{
                 color: white;
                 background-color: $vibrant-color;
               }
             }
           }
         }
       }
     }
   }

   .jumbo-text{
     text-align: center;
     margin-top: 300px;
     h1{
       font-size: 5rem;
       margin-bottom: 25px;
       span{
         @include title 
        }
      }
     p{
       font-size: 1.3rem;
       color: $pumice-color;
       margin-bottom: 60px;
     }
     .btn-left{
       @include btn1;
       margin-right: 20px;
       text-transform: uppercase;
       &:hover{
         background-color: $vibrant-color;
       }
     }
     .btn-right{
       @include btn2;
       text-transform: uppercase;
       &:hover{
         color: white;
         background-color: $sN-color;
       } 
     }
   }
   .right-box{
     padding: 20px;
     float: right;
     width: 50px;
     margin-top: - 230px;
     .box{
       padding: 15px 5px;
       border: 1px solid $bL-color;
       margin-bottom: 10px;
       border-radius: 10px;
     }
     .box-active{
       padding: 15px 5px;
       border: 1px solid $bL-color;
       background-color: $bL-color;
       margin-bottom: 10px;
       border-radius: 10px;
     }
   }
 
 }

</style>