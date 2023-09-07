<script setup>
import IndustryDescrip from '../components/IndustryDescrip.vue'
import IndustrySolutionList from '../components/IndustrySolutionList.vue'
import {  ref,watch } from 'vue'
import apiSource from '../assets/api-config.json'
const apiUrl = apiSource[0]["url"]
console.log( apiUrl)

const urlInd1 =defineProps(['industry'])
const urlInd = urlInd1.industry
console.log( urlInd)
console.log("garni"+ urlInd1)



const API_URL = `${apiUrl}IndNameToText?indName=`


const industeryText = ref(['null'])
async function fetchData() {
  industeryText.value = null
  const res = await fetch(
    `${API_URL}${urlInd}`
  )
  industeryText.value = await res.json()
}

fetchData()



const solotionsList = ref(['null'])

console.log(industeryText)


watch( solotionsList,fetchData)





</script>

<template>
  

  <IndustryDescrip       v-bind:pageDecripation=industeryText[0][1] v-bind:pageTitle=urlInd />
  
  <IndustrySolutionList v-bind:solotions=solotionsList />

</template>
<!--

import IndustrySolutionList from '../components/IndustrySolutionList.vue'
const solotionsList = ref(['null'])
const solotionsList = ref(['null'])
   <IndustrySolutionList v-bind:solotions=solotionsList />
  <IndustrySolutionSection />
-->