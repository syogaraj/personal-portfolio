<template>
  <div class="home">
    <GeneralInfo/>
  </div>
</template>

<script>
// @ is an alias to /src
import GeneralInfo from "@/components/GeneralInfo.vue";

export default {
  name: 'Home',
  components: {GeneralInfo}
}
</script>
