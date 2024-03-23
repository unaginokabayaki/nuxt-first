<template>
    <div class="wrapper">
        <div class="container">
            <h1>Blog</h1>
            <div v-for="item in data" :key="item.id" class="blogCard">
                <div class="textsContainer">
                    <h3>{{ item.title }}</h3>
                    <p>{{ item.excerpt }}</p>
                    <p>{{ item.date }}</p>
                    <NuxtLink :to="item._path">ReadMore</NuxtLink>
                </div>
                <div class="blogImg">
                    <nuxt-img :src="item.image" alt="profile" width="500px" format="webp"/>
                </div>
                <hr>
            </div>
        </div>
    </div>
</template>

<script setup>
const { data } = await useAsyncData("blogQuery", () => 
    queryContent("/blog").sort({id: -1}).find()
)
</script>
