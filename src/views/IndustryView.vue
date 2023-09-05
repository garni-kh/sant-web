<script setup>
import IndustryDescrip from '../components/IndustryDescrip.vue';
import  IndustrySolutionList from '../components/IndustrySolutionList.vue'
import IndustrySolutionSection from '../components/IndustrySolutionSection.vue'

const urlkey = defineProps(['industry'])

const urlInd = urlkey.industry
</script>

<template>
    <IndustryDescrip :indurl="urlInd" />
    <IndustrySolutionList  :indurl="urlInd"/>
    <IndustrySolutionSection />
</template>
