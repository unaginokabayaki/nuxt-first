<template>
    <h1>記事ページです</h1>
    <div class="hero">
        <nuxt-img :src="item.image" alt="profile" width="500px"/>
    </div>
    <div class="wrapper">
       <div class="container">
        <h1>{{ item.title }}</h1>
        <p>{{ item.date }}</p>
        <ContentDoc />
       </div>
    </div>
</template>

<script setup>
const { data: item } = await useAsyncData(useRoute().path, () => 
    queryContent(useRoute().path).findOne()
)

// useAsyncDataの名前は重複してはいけない
// const { data: item } = await useAsyncData("/blog/blog-1", () => 
//     queryContent(/blog/blog-1).findOne()
// )

console.log(useRoute().path)
</script>