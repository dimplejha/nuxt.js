<template>
  <div>
    <nuxt-child :video="video"/>
  </div>
</template>

<script>
  export default {
  data() {
    return {
      videos: [
        {
          id: "3",
          name: "DIMPLE",
        },
        {
          id: "5",
          name: "Aaliya",
        },
        {
          id: "7",
          name: "Shital",
        }]
    }
  },

  computed: {
    video() {
      return this.videos.find((v) => v.id == this.$route.params.id);
    }
  }
};
</script>
