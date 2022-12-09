<template>
  <section class="post-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      title="Hello there!"
      previewText="This is my first post."
      thumbnail="https://www.bbva.com/wp-content/uploads/2017/08/innovacion-bbva-100817-1024x551.jpg"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      title="Hello there, the second time!"
      previewText="This is my second post."
      thumbnail="https://static01.nyt.com/images/2020/01/01/business/01Techfix-print/01Techfix-print-articleLarge.gif?quality=75&auto=webp&disable=upscale"
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      title="Hi!"
      previewText="This is my third post."
      thumbnail="https://imageio.forbes.com/specials-images/dam/imageserve/930116744/960x0.jpg?format=jpg&width=960"
    />
  </section>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview.vue";
export default {
  components: {
    PostPreview,
  },
  props: {
    isAdmin: Boolean,
    default: false,
  },
};
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
