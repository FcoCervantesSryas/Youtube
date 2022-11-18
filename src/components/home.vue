<template>
    <div class="home">
        <div class="tags">
            <div class="tag">All</div>
            <div class="tag">Mixes</div>
            <div class="tag">Gaming</div>
            <div class="tag">Podcast</div>
            <div class="tag">Quantum Mechanics</div>
            <div class="tag">Numbers</div>
            <div class="tag">Media theories</div>
            <div class="tag">Computers</div>
            <div class="tag">AI</div>
            <div class="tag">Computer Programming</div>
        </div>
        <div class="videos">
            <myvideo class="video" t="video" v-for="video in info" :info="video"/>
            <myvideo class="video" t="video" v-for="video in info" :info="video"/>
        </div>
    </div>
</template>
<script>
import videos from "../videos.json";
import myvideo from "./myvideo.vue"
export default {
    name:"home",
    components:{
        myvideo
    },
    data() {
        return {
            info: videos
        }
    }
}
</script>
<style scoped>
.home{
    height: 100%;
    width:100%;
    overflow: scroll;

}
.tags{
    display: flex;
    height: 56px;
    align-items: center;
    margin-left: 40px;
}
.tag{
    height: 60%;
    background-color: rgb(231, 231, 231);
    display: flex;
    align-items: center;
    padding: 0px 10px;
    border-radius: 8px;
    font-size: 14px;
    font-family: "Roboto","Arial",sans-serif;
    cursor: pointer;
    margin: 0px 10px;
}
.videos{
    width: calc(100%-20px);
    display: flex;
    flex-wrap: wrap;
    margin-right: 20px;
    margin-left: 20px;
    justify-content: space-between;
}
.video{
    height: 260px;
    width: 260px;
    /* background-color: blue; */
    margin: 10px 0;
}
</style>