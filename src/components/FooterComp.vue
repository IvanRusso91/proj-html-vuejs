<template>
  <div class="foot">
    <div class="container box-foot">

      <div class="col-uno">
        <h2 class="logo"> <span>nex</span> gen</h2>
        <p>A Functional HTML Template <br> fir Corporate & Business.</p>
        <ul>
          <li><a href="#"><i class="fa-solid fa-phone"></i>+1(305)1234-5678</a></li>
          <li><a href="#"><i class="fa-solid fa-envelope"></i>hello@ecample.com</a></li>
          <li><a href="#"><i class="fa-solid fa-location-dot"></i>Main Avenue, 987</a></li>
        </ul>

        <div class="btn-box">
          <a class="btn" href="#">get in Touch</a>
        </div>
      </div>

      <div class="col-due">
        <h2>About</h2>
        <ul>
          <li v-for="(item, index) in about" :key="`a${index}`"><a href="#"><i :class="item.chevron"></i>{{item.text}}</a></li>
        </ul>
      </div>

      <div class="col-due">
        <h2>Services</h2>
        <ul>
          <li v-for="(obj, index) in services" :key="`b${index}`" ><a href="#"><i :class="obj.chevron"></i>{{obj.text}}</a></li>
        </ul>
      </div>

      <div class="col-due">
        <h2>Support</h2>
        <ul>
          <li v-for="(comp, index) in support" :key="`c${index}`"  ><a href="#"><i :class="comp.chevron"></i>{{comp.text}}</a></li>
        </ul>
      </div>
    </div>

    <div class="fallen">
      <div class="container ir-fallen">
        <p>Enjoy the low price. We are tracking any intention of piracy.</p>
        <p><i class="fa-solid fa-copyright"></i> 2020 NEXGEN is Proudly Powered by <span>Codings</span>.</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name:'FooterComp',
  data(){
    return{
      about:[
        {
          chevron:'fa-solid fa-chevron-right',
          text:'The Company',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Institutional',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Social & Events',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Innovation',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Environment',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Technology',
        },
      ],

      services:[
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Audit & Assurance',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Financial Advisory',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Analytics M&A',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Middle Marketing',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Legal Consulting',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Regulatory Risk',
        },
      ],

      support:[
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Responsibility',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Terms of Use',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'About Cookies',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Privacy Policy',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'Accessibility',
        },
        {
          chevron:'fa-solid fa-chevron-right',
          text:'information',
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';


.foot{
  background-color: rgb(17,17,23);
  .box-foot{
    @include j-sb;
    flex-wrap: wrap;
    padding-top: 130px;
    margin-bottom: 50px;
    .col-uno{
      width: 300px;
      margin-bottom: 50px;
      .logo{
        font-size: 2.0rem;
        text-transform: uppercase;
        color: $pumice-color;
        padding-bottom: 40px;
        span{
          color:$vibrant-color;
          padding: 15px 15px 15px 30px;
          background-color: rgba(3,132,132,0.3);
          border-top-left-radius: 50px;
          border-bottom-left-radius: 50px;
        }
      }
      p{
        color: $pumice-color;
        font-size: 1.1rem;
      }
      .right-p{
        margin-bottom: 30px;
        font-size: 1.1rem;           
        color: $gravel-color;
      }
      ul{
        padding: 0;
        margin-top: 50px;
        li{
          margin-bottom: 30px;
          
          a{
            color: $pumice-color;
            font-size: 1.2rem;
            &:hover{
              color: $bL-color;
            }
            i{
              color: $pumice-color;
              margin-right: 15px;           
            }
          }
        }
      }
      .btn-box{
        margin-top: 50px;
        .btn{       
          @include btn2;
          color: $pumice-color;
          text-transform: uppercase;
          &:hover{
            color: white;
            background-color: $sN-color;
          } 
        }
      }
    }
    .col-due{
      width: 300px;
      margin-bottom: 50px;
      background-color: rgba(188,190,188,0.1);
      border-radius: 20px;
      padding: 40px;
      transition: 1s;
      &:hover{
        transform: translateY(-15px);
      }
      h2{
        color: white;
      }
      ul{
        margin-top: 20px; 
        padding: 0;
        li{
          margin-bottom: 20px;
          
          a{
            color: $pumice-color;
            font-size: 1.1rem;
            &:hover{
              color: $bL-color;
            }
            i{
              margin-right: 15px;
            }
          }
        }   
      }
    }     
  }
  .fallen{
  background-color: rgb(13,13,17);
  height: 100px;
  .ir-fallen{
    @include j-sb;
    p{
      color: $pumice-color;
    margin-top: 40px;

      span{
        color: $bL-color;
      }
    }
  }

  }
}


</style>