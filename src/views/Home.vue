<template>
  <div class="home">
    <div class="home-icon">
      <Heart />
      <span>Default</span>
    </div>
    <div class="home-icon">
      <Twitter color="#1da1f2" />
      <span>Change Color</span>
    </div>
    <div class="home-icon">
      <Sun width="32" height="32" />
      <span>Change Size</span>
    </div>
    <div class="home-icon">
      <Moon class="moon-icon" />
      <span>Add Class</span>
    </div>
    <div class="home-icon">
      <Loading class="loading-icon" />
      <span>Add Animation</span>
    </div>
  </div>
</template>

<script>
import Heart from '@/icons/heart.svg'
import Twitter from '@/icons/twitter.svg'
import Sun from '@/icons/sun.svg'
import Moon from '@/icons/moon.svg'
import Loading from '@/icons/loading.svg'

export default {
  name: 'Home',
  components: { Heart, Twitter, Sun, Moon, Loading }
}
</script>

<style scoped>
.home {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  max-width: 100%;
  flex-wrap: wrap;
}
.home-icon {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  margin: 2rem;
  height: 84px;
}
span {
  margin-top: 0.75rem;
}
.moon-icon {
  opacity: 0.25;
  cursor: pointer;
  transition: 0.3s;
}
.moon-icon:hover {
  opacity: 1;
}
.loading-icon {
  animation: rotate 0.75s linear infinite;
}
@keyframes rotate {
  to {
    transform: rotate(360deg);
  }
}
</style>
