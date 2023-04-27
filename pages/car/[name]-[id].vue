<script setup>
const route = useRoute();
const {toTitleCase} = useUtilities();

useHead({
  title: toTitleCase(route.params.name),
});

definePageMeta({
  layout: "costum",
});
</script>

<template>
  <div>
    <CarDetailHero />
    <CarDetailAttributes />
    <CarDetailDescription />
    <CarDetailContact />
  </div>
</template>
