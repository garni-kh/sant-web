<script>
import apiSource from '../assets/api-config.json'
const apiUrl = apiSource[0]['url']
const API_URL = `${apiUrl}IndNameToText?indName=`
const API_URL1 = `${apiUrl}Solution?selectedInd=`
export default {
  data() {
    return {
      loading: false,
      industeryText: null,
      error: null,
      solotions:null,
      error1:null,
      loading1:null,
    }
  },
  created() {
    // watch the params of the route to fetch the data again
    this.$watch(
      () => this.$route.params,
      () => {
        this.fetchData()
      },
      // fetch the data when the view is created and the data is
      // already being observed
      { immediate: true },
  
    )
    this.fetchData2()
  },
  methods: {
    async fetchData() {
      this.error = this.industeryText = null
      this.loading = true

      try {
        // Replace `API_URL` with your actual API endpoint
        const res = await fetch(`${API_URL}${this.$route.params.industry}`)
    

        if (!res.ok) {
          throw new Error(`Request failed with status: ${res.status}`)
        }

        this.industeryText = await res.json()
        this.loading = false
        
      } catch (err) {
        console.error('An error occurred:', err)
        this.loading = false
        this.error = err.toString()
      }

      this.fetchData2()
    },


    async fetchData2() {
      this.error1 = this.solotions = null
      this.loading1 = true

      try {
        // Replace `API_URL` with your actual API endpoint
        const res = await fetch(`${API_URL1}${this.industeryText.Name}`)
    

        if (!res.ok) {
          throw new Error(`Request failed with status: ${res.status}`)
        }

        this.solotions = await res.json()
        this.loading1 = false
      } catch (err) {
        console.error('An error occurred:', err)
        this.loading1 = false
        this.error1 = err.toString()
      }

      
    }


    
  }
}



</script>
<template>
  <section class="max-w-[1113px] mx-auto mb-[48px] mt-[42px]">
    <h1 class="text-primary-500 text-[32px] leading-[50px] font-bold text-center mb-[40px]">
      مشاوره و راهکارها
    </h1>
    <h2 class="text-primary-400 text-[28px] font-bold text-center mb-[40px]">
      {{ industeryText.Name }}
    </h2>
  </section>
  <!-- Page Title:End -->

  <!-- Heading Box:Begin -->
  <section class="max-w-[607px] mx-auto md:px-0 mb-[40px]">
    <div
      class="w-fit h-fit relative mb-[72px] before:contetnt-[''] before:absolute before:flex before:-z-10 before:w-full before:h-full before:bg-[#F7E4C2] before:-translate-x-[23px] before:translate-y-[45px] before:rounded-b-[42px] after:contetnt-[''] after:absolute after:flex after:-z-10 after:top-0 after:w-full after:h-full after:border-[2px] after:border-[#F79633] after:-translate-x-[16px] after:translate-y-[29px] after:rounded-b-[42px]"
    >
      <div v-if="loading" class="loading">Loading...</div>

      <div v-if="error" class="error">{{ error }}</div>
      <img
        src="https://source.unsplash.com/random/600x600?sig=1"
        class="w-full rounded-b-[42px] z-10"
      />
    </div>

    <p
      v-html=industeryText.testlong
      class="text-[14px] text-[#403D3D] font-normal leading-[28.525px] px-[20px]"
    ></p>
  </section>
  <section class="max-w-[864px] mx-auto mb-[120px]">
    <div class="grid grid-cols-6 gap-[24px]">
      
      <router-link
        v-for="i in solotions"
        :key="i.ID"
        :to="{ name: 'solotion.name', params: { solution: i.solotion_name } }"
        class="rounded-[16px] shadow-lg bg-white col-span-3 md:col-span-2"
      >
        <img
          src="https://source.unsplash.com/random/600x600?sig=1"
          class="w-full rounded-t-[16px]"
        />

        <div class="pt-[35px] pb-[24px]">
          <p class="text-center text-[16px] font-medium text-[#2A447F]">
            {{ i.solotion_name }}
          </p>
        </div>
      </router-link>
    </div>
  </section>

</template>
