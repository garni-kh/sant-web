<script>
import apiSource from '../assets/api-config.json'
const apiUrl = apiSource[0]['url']
const API_URL = `${apiUrl}Solution?selectedInd=`

export default {
  data() {
    return {
      loading: false,
      solotions: null,
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
      this.error = this.solotions = null
      this.loading = true

      try {
        // Replace `API_URL` with your actual API endpoint
        const res = await fetch(`${API_URL}${this.$route.params.industry}`)

        if (!res.ok) {
          throw new Error(`Request failed with status: ${res.status}`)
        }

        this.solotions = await res.json()
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
  <section class="max-w-[864px] mx-auto mb-[120px]">
    <div class="grid grid-cols-6 gap-[24px]">
      <div v-if="loading" class="loading">Loading...</div>

      <div v-if="error" class="error">{{ error }}</div>
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
