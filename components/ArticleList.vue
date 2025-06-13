<template>
    <CardList :items="items" :title="title" :footer="footer" />
</template>

<script setup lang="ts">
import articles from "../constants/articles";

const title = '煉金筆記精選';
const footer = '持續輸出 3 個月，閱讀量超過 10 萬，分享數接近 6 萬'

const items = articles.map((article) => {
    const desc = `${article.shares} 分享`;
    let className = '';
    if (article.shares > 1000) {
        className = 'text-yellow-400';
    }

    const title = `《${article.title}》`

    return {
        title,
        desc,
        date: article.date,
        className,
    };
});
</script>
