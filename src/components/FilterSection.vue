<template>
  
    <div class="nav">
      <div class="menu-item" @click="isOpen = !isOpen">
    <a href="#">
      State Association
    </a>
    <svg viewBox="0 0 1030 638" width="10">
      <path d="M1017 68L541 626q-11 12-26 12t-26-12L13 68Q-3 49 6 24.5T39 0h952q24 0 33 24.5t-7 43.5z" fill="#FFF"></path>
    </svg>
    <transition name="fade" appear>
      <div class="sub-menu" v-if="isOpen">
        <div class="menu-item"><a href="#" @click="$emit('refetch-data', '18bad24aaa')" id="18bad24aaa">Georgia High School Association (GHSA)</a></div>
        <div class="menu-item"><a href="#" @click="$emit('refetch-data', '542bc38f95')" id="542bc38f95">University Interscholastic League (UIL)</a></div>
      </div>
    </transition>
  </div>
    </div>
    
  
</template>

<script>
export default {
    name: 'FilterSection',
    
    data () {
        return {
        isOpen: false
        }
    },
    emits: ['refetch-data']
}    
</script>


<style scoped>
.filter-section-wrapper {
    display: flex;
    width: 80%;
    margin: 0 auto;
}
.nav {
width: 80%;
    position: relative;
    top: 44px;
    margin: 1px auto;
    height: 40px;
    display: flex;
    flex-grow: 100;
    justify-content: space-between;
    background-color: transparent;
}
.nav > .menu-item {
    border-radius: 50px;
    width: 240px;
    height: 21px;
    text-align: left;
    border:none !important;
    border-radius: 0;
    box-shadow: none;
    border-bottom: 2px solid #00529b !important;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    padding: 10px 0 !important;
}
a{
  font-family: 'Montserrat', sans-serif;
}
.nav .menu-item {
    position: relative;
    border: 1px solid #00529b;
    padding: 10px;
}
.nav a {
    color: #fff;
    text-decoration: none;
    opacity: 1;
    z-index: 100;
}
.nav .menu-item svg {
    width: 10px;
    margin-left: 10px;
}
.nav .menu-item .sub-menu {
    position: relative;
    background-color: transparent;
    top: 20px;
    left: 120px;
    transform: translateX(-50%);
    width: 250px;
    text-align: center;
}
.nav .sub-menu .menu-item {
    background-color: #09121a;
    padding: 19.5px 0;
}

.nav .sub-menu .menu-item:hover {
    background-color: #fff;
}

.nav .sub-menu .menu-item:last-child {
    border-radius: 0 0 15px 15px;
}

.nav .sub-menu .menu-item:hover a{
    color: #09121a;
}

.fade-enter-active,
.fade-leave-active {
  transition: all .5s ease-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}

</style>