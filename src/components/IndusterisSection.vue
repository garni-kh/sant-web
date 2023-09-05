<script setup>
import { ref } from 'vue'

const data = ref([])

async function fetchData() {
  const res = await fetch(`http://185.227.111.193:8000/Industries`)
  data.value = await res.json()
}
fetchData()
</script>
<template>
  <section class="max-w-[1102px] mx-auto py-[60px]">
    <p class="w-full text-center text-primary-500 font-bold text-[32px] leading-[50px] mb-[80px]">
      مشاوره و راهکارها
    </p>
    <div class="bg-gradiantsant rounded-[24px] px-[69px] md:px-0 py-[95px]">
      <div class="max-w-[742px] mx-auto">
        <p class="text-[16px] leading-[32px] font-normal text-justify text-[#403D3D] mb-[12px]">
          لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک
          است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی
          تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. کتابهای زیادی
          در شصت و سه درصد گذشته، حال و آینده شناخت فراوان جامعه و متخصصان را می طلبد تا با نرم
          افزارها شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی و فرهنگ پیشرو در
          زبان فارسی ایجاد کرد. در این صورت می ت00000
        </p>

        <div
          class="flex flex-col md:flex-row items-center justify-center space-y-[24px] md:space-y-0 md:space-x-[10px] md:space-x-reverse mx-auto"
        >
          <router-link
            v-for="i in data"
            :key="i.id"
            :to="{ name: 'industryName', params: { industry: i.Name } }"
            class="px-[50px] py-[12px] bg-santGreen rounded-[16px] text-[18] font-bold text-white"
          >
            {{ i.Name }}
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>
