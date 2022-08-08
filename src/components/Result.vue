<template>
  <p>Reaction time: {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 300) {
      this.rank = "Great !";
    } else if (this.score < 400) {
      this.rank = "Good job !";
    } else {
      this.rank = "Try again";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: turquoise;
  font-weight: bold;
}
</style>
