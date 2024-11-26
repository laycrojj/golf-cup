<script setup lang="ts">
const results = [
  { name: "South Cave", win: "JJ", year: "2023" },
  { name: "Kilnwick Percy", win: "JJ", year: "2023" },
  { name: "Kilnwick Percy", win: "OD", year: "2024" },
  { name: "Rufford Park", win: "OD", year: "2024" },
  { name: "Atherstone", win: "JJ", year: "2024" }
]

</script>

<template>
  <main class="min-h-screen flex">
    <!-- Left Window -->
    <div class="panelling md:flex-1"></div>
    <!-- Chalkboard Div -->
    <div class="md:flex-none md:w-[768px] w-full text-slate-200 font-display chalkboard relative">
      <!-- Logo -->
      <div class="px-20 py-10">
        <img alt="Vue logo" src="@/assets/cup_logo.svg" class=" w-3/5 m-auto" />
      </div>

      <!-- Border -->
      <div class=" absolute border-b-4 border-r-4 left-1 top-2 rounded-br-full w-12 h-12"></div>
      <div class=" absolute border-b-4 border-l-4 right-1 top-2 rounded-bl-full w-12 h-12"></div>
      <div class="px-12 absolute top-0 left-0 w-full">
        <div class="relative h-4 top-2 border-t-4 w-full"></div>
      </div>

      <div class="pointer-events-none px-1 pt-12 pb-16 absolute top-0 left-0 w-full h-full">
        <div class="relative h-full top-2 border-x-4 w-full"></div>
      </div>

      <div class=" absolute border-t-4 border-r-4 left-1 bottom-2 rounded-tr-full w-12 h-12"></div>
      <div class=" absolute border-t-4 border-l-4 right-1 bottom-2 rounded-tl-full w-12 h-12"></div>
      <div class="px-12 absolute bottom-0 left-0 w-full">
        <div class="relative h-4 top-2 border-t-4 w-full"></div>
      </div>



      <!-- Screws -->
      <img class="absolute left-2 top-2" src="@/assets/screw.png" height="20" width="20">
      <img class="absolute right-2 top-2" src="@/assets/screw.png" height="20" width="20">
      <img class="absolute left-2 bottom-2" src="@/assets/screw.png" height="20" width="20">
      <img class="absolute right-2 bottom-2" src="@/assets/screw.png" height="20" width="20">
      <!-- Overlay -->
      <!-- <div class="overlay absolute left-0 top-0 mix-blend-darken w-full h-full"></div> -->
      <!-- Names -->
      <div class="m-auto flex justify-around pt-10 text-2xl text-center font-semibold">
        <h2>Jack & Jack</h2>
        <h2>Dave & Owen</h2>
      </div>
      <!-- Big Score -->
      <div class="py-4 border-b-2 border-white mx-10">
        <p class="text-center font-bold text-5xl">3 - 2</p>
      </div>
      <!-- Results -->
      <div class="py-6">
        <div v-for="match in results">

          <div class="flex justify-around pt-10">
            <div class="text-2xl font-bold">{{ match.win == "JJ" ? "W" : "L" }}</div>
            <div>{{ match.name }}</div>
            <div class="text-2xl font-bold">{{ match.win == "JJ" ? "L" : "W" }}</div>
          </div>

          <div class="text-center text-sm font-bold">{{ match.year }}</div>

        </div>
      </div>


    </div>
    <!-- Right Window -->
    <div class="md:flex-1 panellingRight"></div>
  </main>
</template>
