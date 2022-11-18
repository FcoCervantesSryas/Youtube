<template>
    <div class="video">
        <div class="media"></div>
        <div class="meta">
            <div class="user">
                <p><i class="fa-solid fa-user"></i></p>
            </div>
            <div class="info">
                <h1 class="title">{{info.title}}</h1>
                <p class="author">{{info.author}}</p>
                <p class="extra">{{info.Kviews}} views · {{info.Ago}} ago</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:"myvideo",
    props:{
        info:{
            type: Object
        }
    }
}
</script>
<style scoped>
.video{
    font-family: "Roboto","Arial",sans-serif;
}
.media{
    height: 60%;
    background-color: grey;
    border-radius: 20px;
    cursor: pointer;
}
.meta{
    height: 40%;
    display: flex;
}
.user{
    height: 100%;
    width: 50px;
    display: flex;
    justify-content: center;
    cursor: pointer;
}
.user>p{
    height: 35px;
    width: 35px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgb(202, 202, 202);
    color: rgb(165, 165, 165);
}
.info{
    height:100%;
    width: 100%;
    display: flex;
    flex-direction: column;
}
.title{
    font-size: 15px;
    margin-top: 20px;
    margin-left: 3px;
    cursor: pointer;
}
.author{
    margin: 0;
    margin-top: auto;
    font-size: 13px;
    cursor: pointer;
}
.extra{
    margin: 0;
    margin-top: 5px;
    margin-bottom: 20px;
    font-size: 12px;

}
</style>