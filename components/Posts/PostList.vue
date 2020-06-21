<template>
  <section class="posts-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      thumbnail="https://images.idgesg.net/images/article/2019/05/cso_best_security_software_best_ideas_best_technology_lightbulb_on_horizon_of_circuit_board_landscape_with_abstract_digital_connective_technology_atmosphere_ideas_innovation_creativity_by_peshkov_gettyimages-965785212_3x2_2400x1600-100797318-large.jpg"
      title="Hello there!"
      previewText="This is my first post"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      thumbnail="https://images.idgesg.net/images/article/2019/05/cso_best_security_software_best_ideas_best_technology_lightbulb_on_horizon_of_circuit_board_landscape_with_abstract_digital_connective_technology_atmosphere_ideas_innovation_creativity_by_peshkov_gettyimages-965785212_3x2_2400x1600-100797318-large.jpg"
      title="Hello there- the second time!"
      previewText="This is my second post"
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      thumbnail="https://images.idgesg.net/images/article/2019/05/cso_best_security_software_best_ideas_best_technology_lightbulb_on_horizon_of_circuit_board_landscape_with_abstract_digital_connective_technology_atmosphere_ideas_innovation_creativity_by_peshkov_gettyimages-965785212_3x2_2400x1600-100797318-large.jpg"
      title="Hello there- the third time!"
      previewText="This is my third post"
    />
  </section>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview";
export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      required: false
    }
  }
};
</script>

<style scoped>
.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
