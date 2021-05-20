<template>
    <div class="vertical-bar">
      <div class="search-icon">
          <i class="list"><font-awesome-icon :icon="['fas', 'list']"/></i>
          <i><font-awesome-icon :icon="['fas', 'search']"/></i>
      </div>
      <div class="social-icons">
          <i><font-awesome-icon :icon="['fab', 'facebook']"/></i>
          <i><font-awesome-icon :icon="['fab', 'instagram']"/></i>
          <i><font-awesome-icon :icon="['fab', 'twitter']"/></i>
          <i><font-awesome-icon :icon="['fab', 'pinterest']"/></i>
      </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
.vertical-bar{
    height: 100%;
    background: #000;
    position: absolute;
    top: 0;
    left: 0;
}

.search-icon{
    height: 60%;
    width: 80px;
    i{
        margin: 45px 23px;
        display: block;
        color: #fff;
        font-size: 30px;
        cursor: pointer;
    }
}

.social-icons{
    height: 35%;
    width: 80px;
    background: yellow;
    text-align: center;
    padding-top: 27%;
    bottom: 0;
    position: absolute;

    i{
        margin: 15px 23px;
        display: block;
        padding:8px;
        border: 1px solid #000;
        border-radius: 50%;
        cursor: pointer;
    };

}

@media (max-width: 700px) {
    .vertical-bar{
        display: none;
    }

    .list{
        position: absolute;
        right: 20px;
        top: 10px;
    }

}

</style>