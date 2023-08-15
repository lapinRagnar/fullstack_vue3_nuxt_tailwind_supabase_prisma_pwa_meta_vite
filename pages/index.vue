<template>
  <MainLayout>
    <div id="IndexPage" class="w-full overflow-auto">
      <div class="mx-auto max-w-[500px] overflow-hidden">
        <div id="Posts" class="px-4 max-w-[600px] mx-auto" >
          <div class="text-white" v-if="isPosts" v-for="post in posts" :key="post">
            {{ post }}
          </div>

        </div>
      
      </div>

    </div>
  </MainLayout>

</template>

<script setup>
import MainLayout from '../layouts/MainLayout.vue'

// const user = useSupabaseUser()

let posts = ref([])
let isPosts = ref(true)
let isLoading = ref(false)

onBeforeMount(() => {
  posts.value = [
    {
      name: 'John Doe',
      Image: 'https://placehold.co/100',
      Text: 'ceci est le titre',
      picture: 'https://placehold.co/500'
    }
  ]
})

console.log('post', posts.value);


</script>
