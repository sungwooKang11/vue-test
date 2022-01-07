<template>
  <div class="menu">
    <a v-for="header in menus" :key="header">{{header}}</a>
 
  </div>
  
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h4>{{ products[0] }}</h4>
    <p>500만원</p>
    <button @click="increase">허위매물신고</button> <span>신고수 :{{신고수}}</span>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>200만원</p>
    <button @click="increase1">허위매물신고</button> <span>신고수 :{{신고수1}}</span>
  </div>
    <div>
    <h4>{{ products[2] }}</h4>
    <p>100만원</p>
    <button @click="increase2">허위매물신고</button> <span>신고수 :{{신고수2}}</span>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      menus : ['Home', 'Products', 'About'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      신고수 : '0',
      신고수1 : '0',
      신고수2 : '0',
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
</style>
