<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
export default {
  fetch(context) {
    if (context.store.state.loadedPosts.length > 0) {
      return null
    }

  },
  created(){
    this.$store.dispatch('setPosts', this.loadedPosts)
  },
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts
    }
  }
};
</script>

<style>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
