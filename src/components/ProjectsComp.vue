<template>
  <div>
    <div class="container ir-box">
      <p class="pro">we do more for everyone</p>
      <h2 class="title-pro">Actions & <span>Projects</span></h2>
      <nav>
        <ul>
          <li><a href="#">All</a></li>
          <li><a href="#">institutional</a></li>
          <li><a href="#">socila</a></li>
          <li><a href="#">events</a></li>
          <li><a href="#">innovation</a></li>
          <li><a href="#">environment</a></li>
          <li><a href="#">technology</a></li>
        </ul>
      </nav>

      <div class="box-cards">
      <div v-for="(item, index) in books" :key="`i${index}  `"   class="card" id="c-up">
        
        <div class="up">

          <dir>
            <i :class= 'item.arr'></i>
          </dir>
           
        </div>

        <div class="down">
          <h2>{{item.text}}.</h2>
          <p>{{item.down}}</p>
        </div>
      </div>    
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'ProjectsComp',
  data(){
    return{
      books:[
        {
          arr:'fa-solid fa-arrow-right',
          image:'../assets/img/project-1.jpg',
          text: 'Accademic professional program in social media',
          down: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.',
        },
        {
          arr:'fa-solid fa-arrow-right',
          image:'../assets/img/project-2.jpg',
          text: "President's speech at the annual meeting",
          down: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.',
        },
        {
          arr:'fa-solid fa-arrow-right',
          image:'../assets/img/project-3.jpg',
          text: 'International business trip in Shanghai',
          down: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.',
        },
        {
          arr:'fa-solid fa-arrow-right',
          image:'../assets/img/project-4.jpg',
          text: 'technology workshop with education theme',
          down: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.',
        },
        {
          arr:'fa-solid fa-arrow-right',
          image:'../assets/img/project-5.jpg',
          text: 'Donation of clothed and food to the partner NGO',
          down: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.',
        },
        {
          arr:'fa-solid fa-arrow-right',
          image:'../assets/img/project-6.jpg',
          text: 'Confratenrnization of the procurement team',
          down: 'Lorem ipsum dolor sit amet consectetur     adipisicing elit.',
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';


.ir-box{
  text-align: center;
  margin-top: 200px;
  .pro{
    text-transform: uppercase;
    color: $vibrant-color;
    font-weight: bold;    
  }
  .title-pro{
    padding: 50px 0;
    font-size: 3rem;
    span{
      @include title
    }  
  }
  nav{
    ul{
      li{
        display: inline-block;
        margin-left: 40px;
        a{
          text-transform: uppercase;
          color: $gravel-color;
          font-weight: bold;
          &:hover{
            cursor: pointer;
            color: $bL-color;
          }
        }
      }
    }
  }


  .box-cards{
    padding-top: 50px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    #c-up:hover .fa-arrow-right{
      display: block;
    }
    #c-up:hover p{
      display: block;
    }  
    .card{
      width: calc(100% / 3 - 20px);
      padding: 50px;
      border-radius: 10px;
      height: 400px;
      margin-top: 20px;
      background-color: blue;
      transition: 1s; 
      &:hover{
        transform: translateY(-15px);
        box-shadow: 0px 10px 8px gray;
      }
      
      .up{
        color: $bL-color;
        margin-bottom: 30px;
        
        .icon{
          font-size: 5rem;
          padding: 20px 0;  
        }
        .fa-arrow-right{
          font-size: 2rem;
          padding: 5px 8px;
          margin-left: 240px;
          display: none;
          &:hover{
            background-color: $vibrant-color;
            color: white;
            padding: 5px 8px;
            border-radius: 50%;
          }
        }
      }
      .down{
        margin-top: 170px;
        h2{
          font-size: 1.5rem;
          margin-bottom: 10px ;
          color: white;
        }
        p{
          font-size: 1.3rem;
          color: $pumice-color;
          display: none;
        }
      }
    }
  }

}
</style>