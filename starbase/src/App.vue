<template>
    <div id="app">
        <h3>{{ title }}</h3>
        <div class="row">
            <Character v-for="(id, index) in initial_ids" v-bind:id="id" v-bind:key="index" />
        </div>
    </div>
</template>

<script>
import Character from "./Components/Character.vue";
export default {
  name: "app",
  data() {
    return {
      title: "Generate your team",
      initial_ids: [1, 13, 14]
    };
  },
  components: {
    Character
  }
};
</script>
