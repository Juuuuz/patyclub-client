<template>
  <div>
    <div class="top-edge">
      <p>審核通過</p>
      <br/>
      <button @click="nextStep()">下一步</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    nextStep() {
      this.$parent.goToNextStep("toRelease");
    },
  },
};
</script>
