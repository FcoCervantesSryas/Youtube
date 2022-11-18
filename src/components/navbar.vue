<template>
    <div class="nav">
        <div class="threelines circle" @click="toogleText()"><i class="fa-solid fa-bars"></i></div>
        <img src="https://www.gstatic.com/youtube/img/branding/youtubelogo/svg/youtubelogo.svg" alt="YouTube" >
        <input class="search_bar" type="text" placeholder="Search">
        <div class="search_button"><pre>  <i class="fa-solid fa-magnifying-glass"></i></pre></div>
        <div class="mic circle"><i class="fa-solid fa-microphone"></i></div>
        <div class="create circle"><i class="fa-solid fa-square-plus"></i></div>
        <div class="notification circle"><i class="fa-regular fa-bell"></i></div>
        <div class="perfil circle"><i class="fa-solid fa-user"></i></div>
    </div>
</template>
<script>
export default {
    name: "navbar",
    methods: {
        toogleText(){
            // console.log(text)
            this.$emit('toggleText')
        }
    }
}
</script>

<style scoped>
.nav {
    /* border: solid black 1px; */
    height: 56px;
    width: 100%;
    display: flex;
    align-items: center;
    padding: 0;
    margin: 0;
    font-size: 20px;
}
.circle{
    height: 40px;
    width: 40px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.circle:hover{
    background-color: #a0a0a0;
    cursor: pointer;
}
.threelines{
    margin: 0 10px;
}
input{
    height: 35px;
    border-radius: 20px 0px 0px 20px;
    border: solid rgb(206, 206, 206) 0.8px;
    margin-left: 15%;
    width: 30% ;
    padding-left: 20px;
    font-size: 20px;
    outline-color: blue;
}
.search_button{
    height: 37px;
    width: 80px;
    border-radius: 0px 20px 20px 0px;
    background-color: #F0F0F0;
    border: solid rgb(206, 206, 206) 0.8px;
    display: flex;
    align-items: center;
    cursor: pointer;
}
.search_button:hover{
    background-color: #e0e0e0;
}
img{
    height: 35%;
}
.mic{
    margin-left: 10px;
    background-color: rgb(238, 238, 238);
}
.create{
    margin-left: 20%;
}
.notification{
    margin: auto
}
.perfil{
    margin-right: 10px;
}
</style>