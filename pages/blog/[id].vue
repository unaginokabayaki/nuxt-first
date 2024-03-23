<template>
    <h1>記事ページです</h1>
    <div>
        <nuxt-img :src="item.image" alt="profile" width="500px"/>
    </div>
    <div>
        {{ item.title }}
        {{ item.date }}
        <ContentDoc />
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