<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "@/components/Posts/PostList.vue";
export default {
  components: {
    PostList,
  },
  async asyncData(context) {
    try {
      const data = await new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            loadedPosts: [
              {
                id: "1",
                title: "My Amazing Post",
                previewText: "This is my first post!",
                thumbnail:
                  "https://www.bbva.com/wp-content/uploads/2017/08/innovacion-bbva-100817-1024x551.jpg",
              },
              {
                id: "2",
                title: "Hello there!",
                previewText: "This is my second post!",
                thumbnail:
                  "https://static01.nyt.com/images/2020/01/01/business/01Techfix-print/01Techfix-print-articleLarge.gif?quality=75&auto=webp&disable=upscale",
              },
              {
                id: "3",
                title: "Hi!",
                previewText: "This is my third post!",
                thumbnail:
                  "https://imageio.forbes.com/specials-images/dam/imageserve/930116744/960x0.jpg?format=jpg&width=960",
              },
            ],
          });
        }, 1500);
      });
      return data;
    } catch (e) {
      context.error(new Error());
    }
  },
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
