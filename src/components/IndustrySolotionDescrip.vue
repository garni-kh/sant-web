<script>
import apiSource from '../assets/api-config.json'
const apiUrl = apiSource[0]['url']
const API_URL = `${apiUrl}SolotionNameToText/`
const neededDash = '/'

export default {
  data() {
    return {
      loading: false,
      SolotionNameToText: null,
      error: null
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
      { immediate: true }
    )
  },
  methods: {
    async fetchData() {
      this.error = this.SolotionNameToText = null
      this.loading = true

      try {
        // Replace `API_URL` with your actual API endpoint
        const res = await fetch(
          `${API_URL}${this.$route.params.solution}${neededDash}${this.$route.params.industry}`
        )

        if (!res.ok) {
          throw new Error(`Request failed with status: ${res.status}`)
        }

        this.SolotionNameToText = await res.json()
        this.loading = false
      } catch (err) {
        console.error('An error occurred:', err)
        this.loading = false
        this.error = err.toString()
      }
    }
  }
}
</script>

<template>
  <!-- Page Title:Begin -->
  <section class="max-w-[1113px] mx-auto mb-[120px] mt-[42px]">
    <h1 class="text-primary-500 text-[32px] leading-[50px] font-bold text-center mb-[40px]">
      مشاوره و راهکار ها
    </h1>
    <h2 class="text-primary-400 text-[28px] font-bold text-center mb-[40px]">
      {{ SolotionNameToText.solotion_name }}
    </h2>
  </section>
  <!-- Page Title:End -->

  <!-- Heading Box:Begin -->
  <section class="max-w-[928px] mx-auto md:px-0 mb-[120px]">
    <div class="grid grid-cols-2 gap-x-[66px] items-center">
      <div class="col-span-2 md:col-span-1">
        <div
          class="w-fit h-fit relative mb-[72px] scale-75 md:scale-100 before:contetnt-[''] before:absolute before:flex before:-z-10 before:w-full before:h-full before:bg-[#F7E4C2] before:-translate-x-[23px] before:translate-y-[45px] before:rounded-b-[42px] after:contetnt-[''] after:absolute after:flex after:-z-10 after:top-0 after:w-full after:h-full after:border-[2px] after:border-[#F79633] after:-translate-x-[16px] after:translate-y-[29px] after:rounded-b-[42px]"
        >
          <img
            src="https://source.unsplash.com/random/600x600?sig=1"
            class="w-full rounded-b-[42px] z-10"
          />
        </div>
      </div>
      <div class="col-span-2 md:col-span-1">
        <p
          v-html="SolotionNameToText.text"
          class="text-[14px] text-[#403D3D] font-normal leading-[28.525px] px-[20px] text-justify"
        ></p>
      </div>
    </div>
  </section>
</template>
