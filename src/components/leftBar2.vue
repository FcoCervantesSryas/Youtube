<template>
    <div class="leftBar2">
        <div class="section selected" id="home" @click="select('home')">
            <div class="icon"><i class="fa-solid fa-house"></i></div><span>Home</span>
        </div>
        <div class="section" id="short" @click="select('short')">
            <div class="icon"><i class="fa-solid fa-ticket"></i></div><span>Shorts</span>
        </div>
        <div class="section" id="subscriptions" @click="select('subscriptions')">
            <div class="icon"><i class="fa-solid fa-play"></i></div><span>Subscriptions</span>
        </div>
        <div class="section" id="library" @click="select('library')">
            <div class="icon"><i class="fa-solid fa-photo-film"></i></div><span>Library</span>
        </div>
    </div>
</template>
<script>
export default {
    name: "lefBar2",
    methods: {
        select(id){
            document.querySelector(".selected").classList.remove("selected")
            document.getElementById(id).classList.add("selected")
        }
    }
}
</script>
<style scoped>
.leftBar2{
    display: flex;
    flex-direction: column;
    width: 72px;
    height: 100%;
    align-items: center;
}
.section{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0;
    background-color: transparent;
    height: 75px;
    justify-content: center;
    border-radius: 10px;
}
.section:hover{
    background-color: rgb(231, 231, 231);
}
span{
    font-size: 10px;
    font-family: "Roboto","Arial",sans-serif;
    margin: 5px 0px;
}
i{
    font-size: 20px;
}
</style>

