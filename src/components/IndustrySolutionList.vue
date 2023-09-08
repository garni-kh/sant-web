<script setup>

defineProps({

  
  solotions:{


      
    
    }
  }
)

</script>

<template>
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
          <p  class="text-center text-[16px] font-medium text-[#2A447F]">
            {{ i.solotion_name }}
          </p>
        </div>
      </router-link>
    </div>
  </section>
</template>
