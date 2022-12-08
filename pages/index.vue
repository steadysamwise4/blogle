<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news!</h1>
    </section>
    <section class="featured-posts">
      <PostPreview
        id="1"
        title="Hello there!"
        previewText="This is my first post."
        thumbnail="https://www.bbva.com/wp-content/uploads/2017/08/innovacion-bbva-100817-1024x551.jpg"
      />
      <PostPreview
        id="2"
        title="Hello there, the second time!"
        previewText="This is my second post."
        thumbnail="https://static01.nyt.com/images/2020/01/01/business/01Techfix-print/01Techfix-print-articleLarge.gif?quality=75&auto=webp&disable=upscale"
      />
      <PostPreview
        id="3"
        title="Hi!"
        previewText="This is my third post."
        thumbnail="https://imageio.forbes.com/specials-images/dam/imageserve/930116744/960x0.jpg?format=jpg&width=960"
      />
      <!-- <nuxt-link :to="'/posts/' + 2" class="post-preview">
        <article>
          <div
            class="post-thumbnail"
            style="
              background-image: url('https://static01.nyt.com/images/2020/01/01/business/01Techfix-print/01Techfix-print-articleLarge.gif?quality=75&auto=webp&disable=upscale');
            "
          ></div>
          <div class="post-content">
            <h1>Post Title 2</h1>
            <p>Preview Text 2</p>
          </div>
        </article>
      </nuxt-link> -->
    </section>
  </div>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview";
export default {
  name: "IndexPage",
  components: {
    PostPreview,
  },
};
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url("~assets/images/main-page-background.jpg");
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
