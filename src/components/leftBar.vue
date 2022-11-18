<template>
    <div class="leftBar">
        <div class="section selected" id="home" @click="select('home')">
            <div class="icon"><i class="fa-solid fa-house"></i></div><span >Home</span>
        </div>
        <div class="section" id="short" @click="select('short')">
            <div class="icon"><i class="fa-solid fa-ticket"></i></div><span>Shorts</span>
        </div>
        <div class="section" id="subscriptions" @click="select('subscriptions')">
            <div class="icon"><i class="fa-solid fa-play"></i></div><span>Subscriptions</span>
        </div>
        <hr>
        <div class="section" id="library" @click="select('library')">
            <div class="icon"><i class="fa-solid fa-photo-film"></i></div><span>Library</span>
        </div>
        <div class="section" id="history" @click="select('history')">
            <div class="icon"><i class="fa-solid fa-clock-rotate-left"></i></div><span>History</span>
        </div>
        <div class="section" id="yours" @click="select('yours')">
            <div class="icon"><i class="fa-solid fa-play"></i></div><span>Your videos</span>
        </div>
        <div class="section" id="later" @click="select('later')">
            <div class="icon"><i class="fa-regular fa-clock"></i></div><span>Watch later</span>
        </div>
        <div class="section" id="liked" @click="select('liked')">
            <div class="icon"><i class="fa-regular fa-heart"></i></div><span>Liked videos</span>
        </div>
        <div class="section" id="more" v-if="!show_more" @click="show()">
            <div class="icon"><i class="fa-solid fa-chevron-down"></i></div><span>Show more</span>
        </div>
        <div class="section" id="circuits" v-if="show_more"  @click="select('circuits')">
            <div class="icon"><i class="fa-solid fa-indent"></i></div><span>Circuits</span>
        </div>
        <div class="section" id="curious" v-if="show_more" @click="select('curious')">
            <div class="icon"><i class="fa-solid fa-indent"></i></div><span>Curious</span>
        </div>
        <div class="section" id="less" v-if="show_more" @click="show()">
            <div class="icon"><i class="fa-solid fa-chevron-up"></i></div><span>Show Less</span>
        </div>
        <hr>
        <p>Subscriptions</p>
        <div class="section" id="sub1" @click="select('sub1')">
            <div class="icon"><i class="fa-solid fa-user"></i></div><span>Shark Tank</span>
        </div>
        <div class="section" id="sub2" @click="select('sub2')">
            <div class="icon"><i class="fa-solid fa-user"></i></div><span>Academia Play</span>
        </div>
        <div class="section" id="sub3" @click="select('sub3')">
            <div class="icon"><i class="fa-solid fa-user"></i></div><span>acapellascience</span>
        </div>
        <div class="section" id="sub4" @click="select('sub4')">
            <div class="icon"><i class="fa-solid fa-user"></i></div><span>Aderly Céspedes</span>
        </div>
        <div class="section" id="sub5" @click="select('sub5')">
            <div class="icon"><i class="fa-solid fa-user"></i></div><span>Alan Becker</span>
        </div>
        <div class="section" id="sub6" @click="select('sub6')">
            <div class="icon"><i class="fa-solid fa-user"></i></div><span>Antroporama</span>
        </div>
    </div>
</template>
<script>
export default {
    name: "leftBar",
    data() {
        return {
            show_more: false
        }
    },
    methods: {
        show(){
            if (!this.show_more){
                this.show_more = true
            } else {this.show_more = false}
        },
        select(id){
            document.querySelector(".selected").classList.remove("selected")
            document.getElementById(id).classList.add("selected")
        }
    },
}
</script>
<style scoped>
.selected{
    background-color: rgb(231, 231, 231);
    font-weight: bold;
}
.leftBar{
    height: calc(100%-20px);
    width: 220px;
    overflow: scroll;
    overflow-x: hidden;
    padding: 10px 10px;

}
.section{
    height: 40px;
    width: calc(100%-20px);
    cursor: pointer;
    border-radius: 10px;
    padding-left: 10px;
    display: flex;
    align-items: center;
}
.section:hover{
    background-color: rgb(231, 231, 231);
}
.icon{
    font-size: 20px;
    width: 30px;
    margin-left: 10px;
    text-justify: center;
}
.section>span{
    margin-left: 10px;
    font-size: 15px;
    font-family: "Roboto","Arial",sans-serif;
}
p{
    margin-left: 10px;
    font-size: 17px;
    font-family: "Roboto","Arial",sans-serif;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  /* background: #f1f1f1;  */
  background-color: transparent;
}
 
/* Handle */

::-webkit-scrollbar-thumb {
  background: transparent;   
  border-radius: 5px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: rgb(151, 151, 151); 
}
</style>

