<script setup>
import { ref } from 'vue'

const Testimonials = [
  {
    message:
      '"This should be used to tell a story and include any testimonials you might have about your product or service for your clients"',
    user: { name: "Markin Nesus", role: "IOS developer", image: "/img/user1.jpg" },
    id: "1",
  },
  {
    message:
      '"I was amazed by how easy it was to manage my finances with [Your Fintech Company]. The user-friendly interface and insightful tools helped me gain better control over my money. It\'s like having a personal financial advisor right at my fingertips!"',
    user: { name: "Vera Ducan", role: "Flutter developer", image: "/img/user2.jpg" },
    id: "2",
  },
  {
    message:
      '"As a tech enthusiast and investor, I\'m thrilled with the cutting-edge tools they offer. The personalized insights and portfolio analysis have truly taken my investment game to the next level. Feel free to use or modify these options according to your website\'s style and branding. If you need further assistance or changes, please let me know!"',
    user: { name: "Michael Chen", role: "Techprenure", image: "/img/user3.jpg" },
    id: "3",
  },
  {
    message:
      '"The platform\'s security measures and expert recommendations have made me feel at ease, even during market fluctuations. Thanks to them, I\'m taking steps towards financial growth with peace of mind"',
    user: { name: "Robert Emily", role: "Cyber Security Expert", image: "/img/user4.jpg" },
    id: "4",
  },
  {
    message:
      '"The user-friendly interface and insightful tools helped me gain better control over my money. It\'s like having a personal financial advisor right at my fingertips"',
    user: { name: "Sarah Johnson", role: "UI/UX developer", image: "/img/user5.jpg" },
    id: "5",
  },
]

const activeReview = ref(Testimonials[2])

const selectReview = (review) => {
    activeReview.value = review
}
</script>

<template>
    <section id="testimonial" class=" py-20 px-20">
      <div class="container">
        <div class="text-center mb-20">
          <h4 class="font-bold text-color-secondary mb-4">User Review</h4>
          <h1 class="title">What Clients Say About Our App After Use It</h1>
        </div>
  
        <div class="mt-8">
          <div class="">
            <ul class="flex items-center justify-center flex-wrap">
              <li v-for="review in Testimonials" :key="review.id">
                <transition name="fade">
                   <img :src="review.user.image"
                     class="h-20 w-20 rounded-full p-1 m-3 cursor-pointer"
                     :class="{activePic: activeReview.id === review.id, inactivePic: activeReview.id !== review.id}"
                     @click="selectReview(review)"
                     />
                </transition>
               
                   
              </li>
              <div show="activeReview" class="flex flex-col gap-3 text-center items-center justify-center max-w-[50rem]">
                <p>{{ activeReview.message }}</p>
                <h4 class="font-bold text-color-secondary mb-1">{{ activeReview.user.name }}</h4>
                <p>{{ activeReview.user.role }}</p>
              </div>
            </ul>
          </div>
        </div>
  
        <!-- Display the selected image information -->
        <div >
          
        </div>
      </div>
    </section>
  </template>

  <style scoped>
  .activePic {
    border: 2px solid #ff7d3b;
    transition: opacity 0.5s;
    opacity: 1;
  }
  
  .inactivePic {
    opacity: 0.5;
  }
  </style>
  
  