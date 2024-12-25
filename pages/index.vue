<script setup lang="ts">
import { ref } from "vue";

const messageCountData = ref([
  /* your data here */
]);
const messageCountLabels = ref([
  /* your labels here */
]);
</script>

<template>
  <div class="relative w-full p-6 bg-[#f8f4fc] font-sarabun overflow-hidden">
    <div class="grid grid-cols-2">
      <div class="flex flex-col gap-4 justify-self-start">
        <div class="flex items-center gap-2">
          <p class="text-[1.5rem] font-medium">ผลสำรวจสถานการณ์คุณธรรม</p>
          <button
            class="px-4 py-0.5 text-sm text-white font-medium bg-[#4977fc] rounded-3xl">
            2567
          </button>
        </div>

        <p class="text-gray-500">โดย: รศ.นพ.สุริยเดว ทรีปาตี</p>

        <div class="flex gap-2 items-center text-[#4977fc]">
          <p class="text-[1.75rem] font-bold">ดัชนี้ชี้วัดคุณธรรม</p>
          <button class="px-4 py-0.5 bg-[#ccebff] rounded-2xl">ทุนชีวิต</button>
        </div>
      </div>

      <div class="mt-6 justify-self-end">
        <p class="flex text-[1.5rem]">
          จำนวนผู้ร่วมประเมิณ&nbsp;
          <span class="relative -top-5 text-[3.25rem] font-medium text-[#4977fc]">
            {{ " 29,000 " }}
          </span>
          &nbsp;คน
        </p>
      </div>
    </div>

    <div class="absolute top-24 w-full flex items-center justify-center">
      <div
        class="w-fit px-5 py-2 flex justify-center items-center bg-white rounded-[4rem] shadow-lg">
        <p class="text-[1.5rem] font-semibold">ภาพรวม :&nbsp;</p>
        <p class="text-[#4977fc] font-semibold">{{ "ประเทศไทย" }}</p>
      </div>
    </div>

    <!-- Grid 3 -->
    <div class="grid grid-cols-3 mt-4">
      <section
        id="left-area"
        class="relative z-50 flex flex-col gap-1.5 w-[400px] h-fit p-3 bg-white rounded-xl">
        <p class="mb-1.5 text-[1.25rem] font-medium">
          ข้อมูลทั่วไปของผู้ร่วมประเมิณ
        </p>

        <div
          class="min-h-[200px] text-[1.125rem] font-medium border rounded-lg p-2">
          เพศผู้ร่วมประเมิณ
        </div>

        <div
          class="min-h-[200px] text-[1.125rem] font-medium border rounded-lg p-2">
          อายุผู้ร่วมประเมิณ
        </div>

        <div
          class="min-h-[200px] text-[1.125rem] font-medium border rounded-lg p-2">
          ภูมิภาคผู้ร่วมประเมิณ
        </div>
      </section>

      <section
        id="map-area"
        class="relative z-20 justify-self-center">
        <ThailandMap />
      </section>

      <section
        id="right-area"
        class="relative z-50 flex flex-col gap-y-3 w-[400px] justify-self-end">
        <div class="min-h-[536px] p-3 bg-white rounded-xl">
          <p class="text-[1.125rem] font-semibold">ดัชนีชี้วัดคุณธรรม</p>

          <!-- <RadarChart /> -->
        </div>

        <div
          class="min-h-[236px] p-3 text-[1.125rem] font-semibold bg-white rounded-xl">
          รายงานสถานการณ์คุณธรรม
        </div>
      </section>
    </div>
  </div>
</template>

<style scoped></style>
