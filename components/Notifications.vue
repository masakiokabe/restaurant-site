<template>
    <div class="notifications">
        <div class="contents">
            <small>Subscribe My Channel and never miss any new videos </small>
            <p><a href="">PREV</a><a href="">NEXT</a></p>
        </div>
        <div class="notification-img">
            <img src="../assets/img/youtube-subscribe.jpeg"/>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
.notifications{
    display: flex;
    width: 400px;
    position: absolute;
    right: 0;
    bottom: 0;
    background: yellow;
    align-items: center;
}
.notification-img{
    flex-basis: 50%;
    img{
        width: 100%;
        cursor: pointer;
    }
}

.contents{
    flex-basis: 50%;
    padding: 10px;

    a{
        text-decoration: none;
        color: #000;
        font-size: 13px;
        margin: 0 10px;
    }

    p{
        text-align: right;
        margin-top: 10px;
    }
}

@media (max-width: 700px) {
    .notifications{
        width: 100%;
    }
}

</style>