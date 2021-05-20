<template>
    <div class="nav-bar">
        <div class="nav-logo">
            <img src="../assets/img/restaurant-logo.png" />
        </div>
        <div class="nav-links " id="nav-links" :class="close ? 'closeClass' : 'openClass'">
            <div class="close icons" @click="clickMe">
                <i><font-awesome-icon :icon="['fas', 'times']"/></i>
            </div>
            <ul>
                <a href="#"><li>HOME</li></a>
                <a hreif="#"><li>ABOUT</li></a>
                <a href="#"><li>RECIPE</li></a>
            </ul>
            <button type="button" class="btn">SIGN UP</button>
        </div> 
        <div class="responsive icons" @click="close = !close">
            <i ><font-awesome-icon :icon="['fas', 'bars']"/></i>
        </div>
    </div>
</template>
<script>
export default{
    data:{
        close: true,
    },

    methods:{
        clickMe(){
            console.log("you click!", this.close)
        }
    }
}    
</script>
<style lang="scss" scoped>
    .nav-bar{
        display: flex;
        padding: 40px 120px; 
        img{
            width: 135px;

        }
    }

    .nav-links{
        flex: 1;
        ul{
          margin-left: 50px;
          display: inline; 
          li{
              list-style: none;
              display: inline-block;
              padding: 8px 25px;
              &::after{
                  content: '';
                  width: 0%;
                  height: 2px;
                  background: yellow;
                  display: block;
                  margin: auto;
                  transition: .5s;
              }
              &:hover::after{
                  width: 100%;
              }
          }
          a{
              color: #fff;
              text-decoration: none;
              font-size: 13px;
          }

        }
    }

    .icons{
        display: none;
        //visibility: hidden;
    }
    
    .btn{
        padding: 10px 20px;
        border: 0;
        background: yellow;
        font-weight: bold;
        cursor: pointer;
        float: right;
    }

    .responsive{
        display: hidden;
    }

    .close{
        display: hidden;
    }

 @media (max-width: 700px) {
    .nav-bar{
        padding: 10px 30px;
    }

    .responsive{
        display: visble;
        position: absolute;
        right: 20px;
        top: 10px;

        i{
            display: block;
            color: #fff;
            margin: 10px 25px;
            font-size: 35px;
            cursor: pointer;
        }
    }

    .close{
        display: visble;
        float: none;
         i{
            display: block;
            color: #ffff;
            margin: 10px 25px;
            font-size: 35px;
            cursor: pointer;
        }
    }

    .nav-links{
        height: 100vh;
        width: 200px;
        background: #000;
        position: absolute;
        top: 0;
        right: 0px; 
        /* ↓by icon click
        right: -200px;
        */
        text-align: left;
        z-index: 2;

        a{
            display: block;
        }

        .btn{
            float: none;
            margin-left: 25px;
            margin-top: 10px;
        }
    }

    .icons{
        display: block;
        //visibility: visible;
    }

    .closeClass{  
        right: -200px;
    }

    .openClass{
        right: 0;
    }
}   
</style>