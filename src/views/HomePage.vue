<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Sabastian Longoria',
  slogan: 'Full Time Student and Father',
  avatar:
    'https://api.dicebear.com/10.x/adventurer-neutral/svg?eyesVariant=variant01,variant02,variant03,variant05,variant06,variant07,variant08,variant09,variant10,variant11,variant12,variant13,variant14,variant15,variant16,variant17,variant18,variant19,variant20,variant21,variant22,variant23,variant24,variant25,variant26&mouthVariant=variant01,variant02,variant03,variant04,variant05,variant06,variant07,variant08,variant09,variant11,variant12,variant13,variant14,variant15,variant16,variant17,variant18,variant19,variant20,variant21,variant22,variant23,variant24,variant25,variant26,variant27,variant28,variant29,variant30&backgroundColor=763900,ecad80,9e5622&lipsColor=&seed=Felix',
  links: [
    {
      id: 1,
      title: 'Github',
      url: 'https://github.com/slongo10/',
      icon: 'code',
      description: 'Check out my projects',
    },
    {
      id: 2,
      title: 'Linkedin',
      url: 'https://www.linkedin.com/in/sabstian-longoria-567019174/',
      icon: 'briefcase',
      description: 'Connect with me Professionally',
    },
    {
      id: 3,
      title: 'Expenses-Splitter',
      url: 'https://github.com/slongo10/expense-splitter-vue',
      icon: 'calculator',
      description: 'Split the bill',
    },
  ],
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!--Profile Header-->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20 sm:h-32 sm:w-32"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-white sm:text-3xl">
        {{ profile.name }}
      </h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Link List-->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="link in profile.links"
        :key="link.id"
        :title="link.title"
        :url="link.url"
        :description="link.description"
        :icon="link.icon"
      />
    </div>

    <!-- Navigate to Info -->
    <RouterLink
      to="/info"
      class="mt-8 text-sm text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-green-400 hover:underline"
    >
      About me →</RouterLink
    >
  </main>
</template>
