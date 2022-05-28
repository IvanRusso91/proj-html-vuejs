<template>
  <header>
    <div class="box-head container">
      <div class="left ">
        <p><i class="fa-solid fa-clock"></i> Open hourse Mon - Sat - 9:00 - 18:00 </p>
      </div>
      <div class="right container">
       <nav>
         <ul>
            <li><a href="#"><i class="fa-solid fa-phone"></i>
              +1 (305) 1234 - 5678</a>
            </li>
            <li><a href="#"><i class="fa-solid fa-envelope"></i> hello@example.com</a>
            </li>
            <li><a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            </li>
            <li><a href="#"><i class="fa-brands fa-twitter"></i></a>
            </li>
            <li><a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
            </li>
         </ul>
       </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComp',
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars';
@import '../assets/style/mixin';

header{
  background-color: $bSto-color;
  z-index: 4;
  position: relative;
  .box-head{
    @include j-sb;
    height: 60px;
    color: $pumice-color;

    .left{
      width: 50%;
      margin:auto;
    }
    .right{
      display: flex;
      width: 50%;
      justify-content: end;
  
      nav{
        ul{
          li{
            display: inline-block;
            margin-left: 35px;
            a{
              color: $pumice-color;
              &:hover{
                color: $bL-color;
              }
            }
          }
        }
      }

    }
  }
}

</style>