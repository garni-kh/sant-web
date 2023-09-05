<script setup>
import { ref, watchEffect } from 'vue'
import apiSource from '../assets/api-config.json'

const apiUrl = apiSource[0]["url"]
const urlkey = defineProps(['indurl'])
const urlInd = urlkey.indurl



const currentUrl = ref(urlInd)
console.log(currentUrl)
const data = ref('null')
console.log(data)
//console.log(this.$route.props.industry )
const API_URL = `${apiUrl}IndNameToText?indName=`
watchEffect(async () => {
  // this effect will run immediately and then
  // re-run whenever currentBranch.value changes
  const url = `${API_URL}${currentUrl.value}`
  console.log("garniiiiiiiiFromDescrpi   "+url)
  data.value = await (await fetch(url)).json()
})
</script>
<template>
  <section class="max-w-[1113px] mx-auto mb-[48px] mt-[42px]">
    <h1 class="text-primary-500 text-[32px] leading-[50px] font-bold text-center mb-[40px]">
      مشاوره و راهکار ها
    </h1>
    <h2 class="text-primary-400 text-[28px] font-bold text-center mb-[40px]">{{ currentUrl }}</h2>
  </section>
  <!-- Page Title:End -->

  <!-- Heading Box:Begin -->
  <section class="max-w-[607px] mx-auto md:px-0 mb-[40px]">
    <div
      class="w-fit h-fit relative mb-[72px] before:contetnt-[''] before:absolute before:flex before:-z-10 before:w-full before:h-full before:bg-[#F7E4C2] before:-translate-x-[23px] before:translate-y-[45px] before:rounded-b-[42px] after:contetnt-[''] after:absolute after:flex after:-z-10 after:top-0 after:w-full after:h-full after:border-[2px] after:border-[#F79633] after:-translate-x-[16px] after:translate-y-[29px] after:rounded-b-[42px]"
    >
      <img
        src="./images/8e792c01c56e5c144c44fa034cc247d1.jpg"
        class="w-full rounded-b-[42px] z-10"
      />
    </div>

    <p
      v-html="data[0][1]"
      class="text-[14px] text-[#403D3D] font-normal leading-[28.525px] px-[20px]"
    ></p>
  </section>
</template>
