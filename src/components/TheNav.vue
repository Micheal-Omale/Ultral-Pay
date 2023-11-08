<script setup>
import { ref } from 'vue';

const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  isMobileMenuOpen.value =! isMobileMenuOpen.value;
};


</script>

<template>
  
  <header class="bg-color-primary-light fixed w-[100vw] z-10">
    <nav class="container flex justify-between items-center ">
        <div class="text-color-secondary py-5 font-bold text-3xl">
            <a href="#home">
                <span class="text-color-white">Utra</span>Pay.
            </a>
        </div>
        <div>
            <ul class="hidden lg:flex items-center space-x-6 capitalize">
                <li><a href="#home" class="hover:text-color-secondary ease-in duration-200">Home</a></li>
                <li><a href="#feature" class="hover:text-color-secondary ease-in duration-200">features</a></li>
                <li><a href="#testimonial" class="hover:text-color-secondary ease-in duration-200">testimonials</a></li>
                <li><a href="#blog" class="hover:text-color-secondary ease-in duration-200">blog</a></li>
                <li><a href="#contact" class="hover:text-color-secondary ease-in duration-200">contact</a></li>

                <li><button class="bg-color-secondary px-9 py-3 rounded-md capitalize font-bold hover:opacity-80">Free trial</button></li>
            </ul>
        </div>
<div class="lg:hidden cursor-pointer pr-5" @click="toggleMobileMenu">
      <i class="fa-solid fa-bars"></i>
  </div>


</nav>
    

     <!--Mobile Screen-->
    
     <Transition name="bounce">
      <div class="md:hidden h-[100vh]  bg-color-primary-light bg-transparent" v-if="isMobileMenuOpen">
          <ul class="h-full grid place-items-center pb-14 capitalize" >
              <li><a href="#home" class="text-color-secondary ease-in duration-200 text-2xl">Home</a></li>
              <li><a href="#feature" class="text-color-secondary ease-in duration-200 text-2xl">features</a></li>
              <li><a href="#testimonial" class="text-color-secondary ease-in duration-200 text-2xl">testimonials</a></li>
              <li><a href="#blog" class="text-color-secondary ease-in duration-200 text-2xl">blog</a></li>
              <li><a href="#contact" class="text-color-secondary ease-in duration-200 text-2xl">contact</a></li>

              <li><button class="bg-color-secondary px-9 py-3 rounded-md capitalize font-bold hover:opacity-80">Free trial</button></li>
          </ul>
      </div>
    </Transition>

  

   </header> 
   
</template>

<style scoped>

.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}
</style>