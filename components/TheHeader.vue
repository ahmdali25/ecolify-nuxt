<template>
    <nav class="navbar navbar-expand-lg shadow">
        <div class="container">
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarText">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item" v-for="list in lists" :key="list.id">
                        <NuxtLink :to="list.path" class="nav-link">{{ list.name }}</NuxtLink>
                    </li>
                </ul>
            </div>
            <div class="ml-auto">
                <ul class="navbar-nav d-flex flex-row justify-content-between align-items-center">
                    <li class="nav-item me-2">
                        <img class="img-flag" src="@/assets/images/eng.png" alt="Icon Flag">
                    </li>
                    <li class="nav-item">
                        <NuxtLink to="/getInTouch">
                            <BaseButton :isPrimary="false" :isSmallButton="true" name="Get In Touch" />
                        </NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script setup>
const lists = ref([
    { id: 1, name: "Home", path: "/" },
    { id: 2, name: "Blog", path: "/blog" },
    { id: 3, name: "Why?", path: "why" },
    { id: 4, name: "Service", path: "/service" },
    { id: 5, name: "Location", path: "/location" }
])
</script>

<style lang="scss" scoped>
.navbar-nav {
    .nav-item {
        .img-flag {
            border-radius: 50%;
            height: 30px;
            border: 2px solid #2dc48d
        }
    }
}
</style>