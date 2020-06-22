<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "@/components/Posts/PostList";

export default {
  components: { PostList },
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          loadedPosts: [
            {
              id: "1",
              title: "First Post",
              previewText: "This is our first post",
              thumbnail:
                "https://images.idgesg.net/images/article/2019/05/cso_best_security_software_best_ideas_best_technology_lightbulb_on_horizon_of_circuit_board_landscape_with_abstract_digital_connective_technology_atmosphere_ideas_innovation_creativity_by_peshkov_gettyimages-965785212_3x2_2400x1600-100797318-large.jpg"
            },
            {
              id: "2",
              title: "Second Post",
              previewText: "This is our second post",
              thumbnail:
                "https://images.idgesg.net/images/article/2019/05/cso_best_security_software_best_ideas_best_technology_lightbulb_on_horizon_of_circuit_board_landscape_with_abstract_digital_connective_technology_atmosphere_ideas_innovation_creativity_by_peshkov_gettyimages-965785212_3x2_2400x1600-100797318-large.jpg"
            }
          ]
        });
      }, 1500);
    }).then(data => {
      return data
    }).catch(e => {
      context.error(new Error())
    });
  },
  created(){
    this.$store.dispatch('setPosts', this.loadedPosts)
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
