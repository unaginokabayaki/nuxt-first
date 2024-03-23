<template>
    <h1>Indexページ</h1>
    <div class="hero">
        <nuxt-img src="/images/index-hero.jpg" alt="profile"/>
        <div class="textContainer">
            <h1>hello</h1>
            <h3>javascript</h3>
        </div>
    </div>
    <div class="container">
        <div class="profile">
            <div>
                <h2>nerd</h2>
                <p>lorem ipsmu</p>
            </div>
            <nuxt-img src="/images/profile.jpg" alt="profile"/>
        </div>
    </div>
    <div class="skills">
        <h2>skills</h2>
        <div class="skillsContainer">
            <div><img src="/images/javascript.svg" alt="js"><span>10 years</span></div>
            <div><img src="/images/javascript.svg" alt="js"></div>
            <div><img src="/images/javascript.svg" alt="js"></div>
            <div><img src="/images/javascript.svg" alt="js"></div>
        </div>
        <div class="ctaButton">
            <NuxtLink to="/contact">Contact</NuxtLink>
        </div>
    </div>
</template>