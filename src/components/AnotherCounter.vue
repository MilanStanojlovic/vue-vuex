<template>
  <div>
    <button class="btn btn-primary" @click="asyncIncrement({by: 50, duration: 500})">Increment</button>
    <button class="btn btn-primary" @click="asyncDecrement({by: 50, duration: 500})">Decrement</button>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  methods: {
    ...mapActions(["asyncIncrement", "asyncDecrement"])
  }
  //mapActions creates these methods
  // increment(value) {
  //   this.$store.dispatch("increment", value);
  // }
};
</script>