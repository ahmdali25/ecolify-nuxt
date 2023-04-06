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
                        <NuxtLink to="/getInTouch" class="button button-state-secondary">Get In Touch</NuxtLink>
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

.button {
    display: inline-block;
    font-weight: 400;
    font-size: 14px;
    color: #212529;
    height: 46px;
    width: 128px;
    padding: 10px 18px;
    border-radius: 6px;
    border: none;
    text-align: center;
    vertical-align: middle;
}

a {
    text-decoration: none;
}

.button-state-secondary {
    background: linear-gradient(250.73deg,#2dc48d 5.56%,#2bb994 96.08%);
    color: #ffffff;
}
</style>