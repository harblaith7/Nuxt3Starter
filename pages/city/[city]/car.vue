<script setup>
const route = useRoute()
useHead({
    title: `All ${route.params.make ? toTitleCase(route.params.make) : 'Cars'} in ${toTitleCase(route.params.city)}`,
})

function toTitleCase(str) {
    return str.replace(
        /\w\S*/g,
        function(txt) {
            return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
        }
    )
}
</script>

<template>
    <div>
      <NavBar />
      <div
        class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5"
      >
        <div class="mt-32 flex">
          <CarSidebar />
  
          <NuxtPage />
        </div>
      </div>
    </div>
  </template>
  