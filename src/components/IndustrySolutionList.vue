<script setup>
import { ref, watchEffect } from 'vue'
import apiSource from '../assets/api-config.json'

const apiUrl = apiSource[0]["url"]

const urlkey = defineProps(['indurl'])

const urlInd = urlkey.indurl
const currentUrl = ref(urlInd)
const data = ref('null')

const API_URL = `${apiUrl}Solution?selectedInd=`
watchEffect(async () => {
  // this effect will run immediately and then
  // re-run whenever currentBranch.value changes
  const url =`${API_URL}${currentUrl.value}`
  console.log("garniiiiiiii"+url)
  data.value = await (await fetch(url)).json()
})
</script>

<template>
  <section class="max-w-[864px] mx-auto mb-[120px]">
    <div class="grid grid-cols-6 gap-[24px]">
      <div
        v-for="i in data"
        :key="i.ID"
        class="rounded-[16px] shadow-lg bg-white col-span-3 md:col-span-2"
      >
        <img
          src="https://source.unsplash.com/random/600x600?sig=1"
          class="w-full rounded-t-[16px]"
        />

        <div class="pt-[35px] pb-[24px]">
          <router-link  to="/"  class="text-center text-[16px] font-medium text-[#2A447F]">
            {{ i.solotion_name }}
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>
