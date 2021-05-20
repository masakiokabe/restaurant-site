<template>
  <div class="hero">
    <Navbar/>
    
    <div class="banner-title">
       <h1>Food <span>Doesn't have<br/> a religion.</span> It is a religion</h1>
       <button type="button" class="btn">EXPLORE</button>
    </div>

    <Notifications />
  </div>
</template>

<script>
import Navbar from '../components/Navbar';
import Notifications from '../components/Notifications';
//import Vertical from '../components/Vertical-bar';

export default {
  components:{
   Navbar,
   Notifications,
   //Vertical,
  }
}
</script>

<style lang="scss" scoped>
.hero{
  height: 100vh;
  background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.6)), url("../assets/img/burger1.jpg") no-repeat fixed;
  background-size: cover;
}

.banner-title{
  margin: 80px 130px;
  color: #fff;
  h1{
    font-size: 64px;
    margin-bottom: 30px;
  }
  span{
    color: yellow;
  }
}

.btn{
      padding: 10px 20px;
      border: 0;
      background: yellow;
      font-weight: bold;
      cursor: pointer;
      //float: right;
  }

@media (max-width: 700px) {
    .banner-title{
        margin: 80px 40px;

        h1{
          font-size: 50px;
        }
    }
}  

</style>