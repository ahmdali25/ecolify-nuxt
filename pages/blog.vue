<template>
    <div class="container">
        <section class="row justify-content-center banner">
            <img class="img-banner" src="../assets/images/logoBlog.png" alt="Banner Image">
            <ul class="row mt-5">
                <li class="col-2 text-center list">Eco-Acts</li>
                <li class="col-2 text-center list">Eco-News</li>
                <li class="col-2 text-center list">Eco-Project</li>
                <li class="col-2 text-center list">Eco-Edu</li>
                <li class="col-2 text-center list">Eco-Tips</li>
                <li class="col-2 text-center list">Eco-Feature</li>
            </ul>
        </section>
        <section class="row">
            <h1 class="section-title">Artikel Pilihan</h1>
        </section>
        <section class="row">
            <div class="card-group">
                <div class="col-sm-12 col-md-8 col-lg-8">
                    <article class="card-article">
                        <img class="card-img mb-1" :src="blog.data[0].image" :alt="blog.data[0].name">
                        <NuxtLink class="mt-2 mb-1">
                            <img src="@/assets/images/category-icon.svg" alt="Category Icon" class="category-icon">
                            <span class="card-article__category">{{ blog.data[0].category }}</span>
                        </NuxtLink>
                        <p class="card-article__title">{{ blog.data[0].name }}</p>
                        <p class="card-article__desc">{{ blog.data[0].description }}</p>
                        <p class="card-article__author">{{ formatDate(blog.data[0].date) }} / {{ blog.data[0].author }}</p>
                    </article>
                </div>
                <div class="col-sm-12 col-md-4 col-lg-4">
                    <article class="card-article">
                        <img class="card-img mb-1" :src="blog.data[1].image" :alt="blog.data[1].name">
                        <NuxtLink class="mt-2 mb-1">
                            <img src="@/assets/images/category-icon.svg" alt="Category Icon" class="category-icon">
                            <span class="card-article__category">{{ blog.data[0].category }}</span>
                        </NuxtLink>
                        <p class="card-article__title">{{ blog.data[1].name }}</p>
                        <p class="card-article__desc">{{ blog.data[1].description }}</p>
                        <p class="card-article__author">{{ formatDate(blog.data[1].date) }} / {{ blog.data[1].author }}</p>
                    </article>
                </div>
            </div>
        </section>
        <section class="row">
            <div v-for="data in blog.data" :key="data.id" class="col-4">
                <article class="card-article">
                    <img class="card-article__image mb-1" :src="data.image" :alt="data.name">
                    <NuxtLink class="mt-2 mb-1">
                        <img src="@/assets/images/category-icon.svg" alt="Category Icon" class="category-icon">
                        <span class="card-article__category">{{ data.category }}</span>
                    </NuxtLink>
                    <p class="card-article__title">{{ data.name }}</p>
                    <p class="card-article__desc">{{ data.description }}</p>
                    <p class="card-article__author">{{ formatDate(data.date) }} / {{ data.author }}</p>
                </article>
            </div>
        </section>
        <section class="row justify-content-center mt-5 mb-5">
            <BaseButton :isPrimary="false" :isSmallButton="false" name="Lanjut Baca" />
        </section>
    </div>
</template>

<script setup>
const { data: blog } = await useFetch("https://mocki.io/v1/8b2bbd1e-8c0a-4ee6-bd9b-135fee8c7280");

function formatDate(date) {
    const dateFormatted = new Date(date).toLocaleString('id-ID',{day: 'numeric',month: 'short',year:'numeric'});
    return dateFormatted;
}
</script>

<style lang="scss" scoped>
.banner {
    padding: 100px 0;
}

.img-banner {
    width: 514px;
}

.section-title {
    font-size: 48px;
    font-weight: 700;
    margin-left: 30px;
}

.list {
    list-style: none;
    font-size: 12.8px;
}

.category-icon {
    height: 20px;
    color: #67c0de;
    margin-right: 10px;
}

.card-article {
    display: flex;
    flex-direction: column;
    padding: 1.25rem;
    
    p {
        font-size: 14px;
        line-height: 1.6;
    }

    &__image {
        height: 246px;
        object-fit: cover;
        border-radius: 3px;
    }

    &__category {
        color: #67C0DE;
        font-weight: 600;
    }

    &__title {
        color: #212322;
        font-weight: 900;
        height: 40px;
    }

    &__desc {
        color: #767A78;
        height: 80px;
    }

    &__author {
        color: #767A78;
    }
}

.card-img {
    height: 300px;
    object-fit: cover;
    border-radius: 3px;
}
</style>