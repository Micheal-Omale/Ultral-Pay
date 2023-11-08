<template>
    <section id="home" class="relative pt-[10rem] pb-[15rem] md:py-[10rem]">
      <div class="blob"></div>
      <div class="blob2"></div>
      <div class="container">
        <div class="flex flex-col items-center z-20 md:flex-row">
          <div class="text-center mb-12 md:text-left md:w-1/2 md:pr-10">
            <h1 class="title pb-2">Awesome App For Your Financial.</h1>
            <p class="leading-relaxed mb-10">This should be used to tell a story and let your users know a little more about the app and its use, how it can benefit them.</p>
            <button class="btn">Download App</button>
          </div>
  
          <div class="hero_bg md:w-1/2 absolute top-[55%] left-[80%] py-[10rem] md:py-10">
            <img class="md:w-[80%] w-full" src="/img/hero3.png" alt="">
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <style scoped>
  .hero_bg img {
    animation: float 4s ease-in-out infinite;
  }
  
  @keyframes float {
    0% {
      transform: translate(-50%, -46%);
    }
    50% {
      transform: translate(-50%, -54%);
    }
    100% {
      transform: translate(-50%, -46%);
    }
  }
  
  @media (max-width: 640px) {
    .hero_bg {
      top: 60%; /* Adjust the vertical position for mobile */
      left: 50%; /* Center horizontally on mobile */
    }
  }
  </style>
  