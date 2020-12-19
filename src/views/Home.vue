<template>
  <section class="home">
    <GeneralInfo/>
  </section>
</template>

<script>
// @ is an alias to /src
import GeneralInfo from "@/components/GeneralInfo.vue";

export default {
  name: 'Home',
  components: {GeneralInfo}
}
</script>
