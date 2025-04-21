<script setup>
import { ref } from 'vue'
import logo from '@/assets/logo.jpg'
// 确保路径正确
import HeadPortraitComponent from '@/components/homeViewComponents/HeadPortraitComponent.vue'
import router from "@/router/index.js"
import { ElMessageBox } from 'element-plus'

const showDropdown = ref(false)
const dialogVisible = ref(false)

const handleIconClick = () => {
  dialogVisible.value = true
}

const toggleDropdown = (visible) => {
  showDropdown.value = visible
}
</script>

<template>
  <div id="header">
    <div id="logoContainer">
      <img :src="logo" style="height: 100%;">
    </div>
    <div class="container">
      Store
    </div>
    <div class="container2">
      Collaboration
    </div>
    <div class="container">
      Ecology
    </div>
    <div class="container">
      Support
    </div>

    <div class="icon" @click="handleIconClick">
      <svg t="1744712725541" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6568" width="40" height="50"><path d="M446.112323 177.545051c137.567677 0.219798 252.612525 104.59798 266.162424 241.493333 13.562828 136.895354-78.778182 261.818182-213.617777 289.008485-134.852525 27.203232-268.386263-52.156768-308.945455-183.608889s25.018182-272.252121 151.738182-325.779394A267.235556 267.235556 0 0 1 446.112323 177.545051m0-62.060607c-182.794343 0-330.989899 148.195556-330.989899 330.989899s148.195556 330.989899 330.989899 330.989899 330.989899-148.195556 330.989899-330.989899-148.195556-330.989899-330.989899-330.989899z m431.321212 793.341415a30.849293 30.849293 0 0 1-21.94101-9.102223l-157.220202-157.220202c-11.752727-12.179394-11.584646-31.534545 0.37495-43.50707 11.972525-11.972525 31.327677-12.140606 43.494141-0.37495l157.220202 157.220202a31.036768 31.036768 0 0 1 6.723232 33.810101 31.004444 31.004444 0 0 1-28.651313 19.174142z m0 0" p-id="6569" fill="#707070"></path></svg>
    </div>

    <div class="icon-container">
      <div
          class="icon2"
          @mouseenter="toggleDropdown(true)"
          @mouseleave="toggleDropdown(false)"
      >
        <svg
            t="1744712158302"
            class="clickable-icon"
            viewBox="0 0 1024 1024"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            p-id="4329"
            width="40"
            height="50"
        >
          <path
              d="M466.7 541.2c45.1-36 74.1-91.5 74.1-153.6 0-108.3-88.1-196.5-196.5-196.5s-196.5 88.1-196.5 196.5c0 62.1 29 117.6 74.1 153.6-27.3 13.8-52.6 32.4-74.7 55.3-52.2 54.1-81 125.9-81 202.2 0 19.9 16.1 36 36 36s36-16.1 36-36c0-118.4 92.5-214.6 206.1-214.6s206.1 96.3 206.1 214.6c0 19.9 16.1 36 36 36s36-16.1 36-36c0-76.3-28.8-148.2-81-202.2-22.2-22.9-47.4-41.4-74.7-55.3zM219.8 387.6c0-68.6 55.8-124.5 124.5-124.5S468.7 319 468.7 387.6s-55.8 124.5-124.5 124.5-124.4-55.8-124.4-124.5zM910 192H576.1c-19.9 0-36 16.1-36 36s16.1 36 36 36h310.5v501.5H706.7c-19.9 0-36 16.1-36 36s16.1 36 36 36H910c26.8 0 48.6-21.5 48.6-48V240c0-26.4-21.8-48-48.6-48z"
              p-id="4330"
              fill="#707070"
          ></path>
          <path
              d="M625.6 395.6h184.3c19.9 0 36-16.1 36-36s-16.1-36-36-36H625.6c-19.9 0-36 16.1-36 36s16.1 36 36 36zM845.9 499.7c0-19.9-16.1-36-36-36H625.6c-19.9 0-36 16.1-36 36s16.1 36 36 36h184.3c19.9 0 36-16.2 36-36zM809.9 676c19.9 0 36-16.1 36-36s-16.1-36-36-36H677.4c-19.9 0-36 16.1-36 36s16.1 36 36 36h132.5z"
              p-id="4331"
              fill="#707070"
          ></path>
        </svg>

        <transition name="dropdown">
          <div v-if="showDropdown" class="dropdown-menu">
            <div class="dropdown-item">个人中心</div>
            <div class="dropdown-item">设置</div>
            <div class="dropdown-item">退出登录</div>
          </div>
        </transition>
      </div>
    </div>

    <div class="icon3">
      <svg t="1744712322188" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="5524" width="40" height="50"><path d="M919.68 704H292.48l-160-576H28.8V64h152.32l160 576h525.12l52.16-288H412.8V288h582.4l-75.52 416zM380.8 960a96 96 0 1 1 96-96 96 96 0 0 1-96 96z m0-128a32 32 0 1 0 32 32 32 32 0 0 0-32-32zM796.8 960a96 96 0 1 1 96-96 96 96 0 0 1-96 96z m0-128a32 32 0 1 0 32 32 32 32 0 0 0-32-32z" fill="#707070" p-id="5525"></path><path d="M476.8 416h64v160h-64zM668.8 416h64v160h-64z" fill="#707070" p-id="5526"></path></svg>
    </div>
  </div>
</template>

<style scoped>
#header{
  height: 50px;
  width: 100%;
  display: flex;
  background-color: #F2F2F2;
  border-bottom: 1px solid #b9b9b9;
  align-items: center;
  position: relative;
}

#logoContainer{
  height: 100%;
  width: 250px;
  margin-left:50px;
}

.container{
  height: 20px;
  width: 100px;
  margin-left:60px;
  margin-top: 0px;
}
.container2{
  height: 20px;
  width: 100px;
  margin-left:30px;
  margin-top: 0px;
}

.container:hover{
  color: #3a3939;
}

.icon{
  margin-top:1px ;
  margin-left: 50px;
  cursor: pointer;
}

.icon-container {
  position: relative;
  display: inline-block;
}

.icon2 {
  margin-top:2px;
  margin-left: 60px;
  cursor: pointer;
}

.clickable-icon {
  transition: all 0.3s ease;
}

.clickable-icon:hover {
  opacity: 0.8;
  transform: scale(1.05);
}

.icon3{
  margin-left: 20px;
  margin-top:0px;
  cursor: pointer;
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: white;
  min-width: 160px;
  box-shadow: 0 8px 16px rgba(0,0,0,0.2);
  z-index: 1000;
  border-radius: 4px;
  overflow: hidden;
}

.dropdown-item {
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  color: #333;
  cursor: pointer;
  transition: background-color 0.3s;
}

.dropdown-item:hover {
  background-color: #f5f5f5;
}

.dropdown-enter-active,
.dropdown-leave-active {
  transition: all 0.3s ease;
}

.dropdown-enter-from,
.dropdown-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>