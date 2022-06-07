<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 60) {
      this.rank = "OP Fast!";
    } else if (this.score < 1500) {
      this.rank = "slower than snail mail!";
    } else {
      this.rank = "Too slow!! Try again";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>