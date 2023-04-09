<template>
  <div>
    <TheHeader />
    <slot />
    <div class="wave">
        <img class="wave__image" src="@/assets/images/footer-wave.svg" alt="Footer Wave">
    </div>
    <TheFooter/>
  </div>
</template>

<style lang="scss" scoped>
.wave {
    &__image {
        width: 100%;
    }
}
</style>