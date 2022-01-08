<template>
  
  <div class="black-bg" v-if="openModal == true">
    <div class="white-bg">
      <h4></h4>
      <p>상세내용</p>
      <button @click="openModal = false">닫기</button>
    </div>
  </div>
  
  <div class="menu">
    <a v-for="header in menus" :key="header">{{header}}</a>
  </div>
  
  <div>
    <img alt="" :src="원룸정보[0].image">
    <h4 @click="openModal = true" >{{원룸정보[0].title}}</h4>
    <p>{{원룸정보[0].price}}</p>
    <button @click="신고수[0]++">허위매물신고</button> 
    <span>신고수 :{{신고수[0]}}</span>
  </div>
  <img alt="" src="./assets/room1.jpg">
  <div>
    <h4 @click="openModal = true">{{ products[1] }}</h4>
    <p>200만원</p>
    <button @click="신고수[1]++">허위매물신고</button> 
    <span>신고수 :{{신고수[1]}}</span>
  </div>
  <img alt="" src="./assets/room2.jpg">
    <div>
    <h4 @click="openModal = true">{{ products[2] }}</h4>
    <p>100만원</p>
    <button @click="신고수[2]++">허위매물신고</button> 
    <span>신고수 :{{신고수[2]}}</span>
  </div>

</template>

<script>
import contents from './assets/room.js';


export default {
  name: 'App',
  data(){
    return{
      원룸정보 : contents,
      신고수 : [0,0,0],
      menus : ['Home', 'Products', 'About'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      openModal : false,
    }
  },
  methods : {
    increase(){
      this.신고수 ++ ;
    },
    increase1(){
      this.신고수1 ++ ;
    },
    increase2(){
      this.신고수2 ++ ;
    }
  },
  components: {
  }
}
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%; height: 100%;
  background: rgb(0,0,0,0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%; 
  background: white;
  border-radius: 8px;
  padding: 20px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 20px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}

  img {
    width: 100%;
    margin-top: 40px;
  }
</style>
