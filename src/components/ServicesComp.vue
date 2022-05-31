<template>
  <div class="service ">
    <div class="box container">
      <div class=" col-left">
        <p class="areas">our business areas</p>
        <h2>Execellence in <span>Services</span></h2>
        <p class="small-t">we are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals. these are some options that you can hire.</p>
      
      </div>

      <div class="col-right container">
        <a href="#"> see all</a>
      </div>

    </div>
    <div class="container box-cards">

      <!--Card ciclate  -->
      
      <div v-for="(card, index) in cards" :key="`i${index}  `"   class="card">
        <div class="up">

          <div>
            <i :class= 'card.icon' class="icon"></i>
          </div>
           
          <dir>
            <i :class= 'card.arr'></i>
          </dir>
           
        </div>

        <div class="down">
          <h3>{{card.title}}</h3>
          <p>{{card.text}}.</p>
        </div>
      </div>    
    </div>
    <div class="bull"></div>
    <div class="bull2"></div>

  </div>
</template>

<script>
export default {
  name:'ServicesComp',

  data(){
    return{
      cards:[
        {
          icon: "fa-solid fa-network-wired",
          arr: 'fa-solid fa-arrow-right',
          title: 'Audio & Assurance',
          text: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.'
        },
        {
          icon: "fa-solid fa-briefcase",
          arr: 'fa-solid fa-arrow-right',
          title: 'Financial Advisory',
          text: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.'
        },
        {
          icon: "fa-solid fa-chart-column",
          arr: 'fa-solid fa-arrow-right',
          title: 'Analytics and M&A',
          text: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.'
        },
        {
          icon: "fa-solid fa-plane",
          arr: 'fa-solid fa-arrow-right',
          title: 'Audio & Assurance',
          text: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.'
        },
        {
          icon: "fa-solid fa-globe",
          arr: 'fa-solid fa-arrow-right',
          title: 'Legal Consulting',
          text: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.'
        },
        {
          icon: "fa-solid fa-inbox",
          arr: 'fa-solid fa-arrow-right',
          title: 'Regulatory Risk',
          text: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';

.service{
  background-color: $gN-color;
  .box{
    @include j-sb;
    .col-left{
      width: 1300px;
      .areas{
        text-transform: uppercase;
        color: $vibrant-color;
        font-weight: bold;
        margin-top: 150px ;
      }
      h2{
        padding: 50px 0;
        font-size: 3rem;
        span{
          @include title
        }
      }
      .small-t{
        font-size: 1.1rem;
        color: $pumice-color;
      }
    }
    .col-right{
      width: 800px;
      display: flex;
      justify-content: end;
      a{
        @include btn1;
        margin-top: 320px;
        text-transform: uppercase;
        &:hover{
          background-color: $vibrant-color;
        }
      }
      
    }  
  }
  .bull{
  @include bull;
  }
  .bull2{
  @include bull;
    margin-top: -65px;
    margin-bottom: -70px;
  }
}
.box-cards{
  padding-top: 50px;
  padding-bottom: 100px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  .card{
    margin-top: 30px;
    width: 420px;
    background-color: white;
    padding: 50px;
    border-radius: 10px;
    transition: 1s;
    
    &:hover{
      transform: translateY(-15px);
      box-shadow: 0px 10px 8px gray
    }
    .up{
      @include j-sb;
      color: $bL-color;
      margin-bottom: 30px;
      .icon{
        font-size: 5rem;
        padding: 20px 0;  
      }
      .fa-arrow-right{
        font-size: 2rem;
        padding: 5px 8px;

        &:hover{
          background-color: $vibrant-color;
          color: white;
          padding: 5px 8px;
          border-radius: 50%;
        }
      }
    }
    .down{
      h3{
        font-size: 2rem;
        margin-bottom: 30px ;
      }
      p{
        font-size: 1.3rem;
        color: $pumice-color;
      }
    }
  }
}



</style>