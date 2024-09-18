<header>
  <h2>Статьи</h2>
</header>
<main>
  <article class="post" v-for="post in posts" :key="post.id">
    <h3>{{ post.title }}</h3>
    <ul>
      <li v-for="tag  in post.tags" :key="tag.id">{{ tag }}</li>
    </ul>
    <a href="#">Читать подробнее</a>
  </article>
</main>
</template>

<script setup lang="ts">
const dataTwice = await $fetch('https://dummyjson.com/posts')
const posts = dataTwice.posts;

</script>

<style scoped>
main {
display: flex;
gap: 10px;
flex-wrap: wrap;
}
li:hover {
text-decoration: underline;
cursor: pointer;
}
.post {
background-color: brown;
color: aliceblue;
padding: 10px;
width: 280px;
}
.post  a{
font-size: 18px;
color: wheat;
}
</style>