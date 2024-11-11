<script setup lang="ts">
import { SUCCESS } from '../../composables/useNewsletter'
</script>

<template>
  <div class="container mx-auto grid items-center place-items-center h-screen">
    <div class="max-w-4xl text-center  border rounded p-8 shadow-lg">
      <h1 class="text-5xl font-bold py-8">
        Thank you for <span class="text-xp-light-pink">subscribing!</span>
      </h1>
      <p class="text-2xl">
        {{ SUCCESS }}
      </p>
      <NuxtLink
        to="/"
        class="mt-16 text-lg inline-block hover:underline"
      >
        <Icon
          name="heroicons:arrow-left"
          class="me-1"
        /> Return to Homepage
      </NuxtLink>
    </div>
  </div>
</template>

<style>
@keyframes float {
  0% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0); }
}
.animate-float {
  animation: float 5s ease-in-out infinite;
}

@keyframes scroll {
  0% { transform: translateX(0); }
  100% { transform: translateX(-100%); }
}
.emoji-row {
  white-space: nowrap;
}
/* .animate-scroll {
  animation: scroll 15s linear infinite;
} */

@keyframes infinite-scroll {
  0% { transform: translateX(0); }
  100% { transform: translateX(-100%); }
}
.animate-infinite-scroll {
  animation: infinite-scroll 20s linear infinite;
}
.animate-scroll {
  animation: infinite-scroll 25s linear infinite
}

@keyframes infinite-scroll {
          from { transform: translateX(0) }
          to { transform: translateX(-100%) }

}
</style>
