<template>
    <button
        class="button"
        :class="isPrimary ? 'button-state-primary' : 'button-state-secondary'"
        :style="{fontSize: ( isSmallButton ? '14px' : '16px' )}">
        {{ name }}
    </button>
</template>

<script setup>
defineProps(['name', 'isPrimary', 'isSmallButton'])
</script>;

<style lang="scss" scoped>
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

.button-state-primary {
    background: #2591b4;
    color: #ffffff;
}

.button-state-secondary {
    background: linear-gradient(250.73deg,#2dc48d 5.56%,#2bb994 96.08%);
    color: #ffffff;
}
</style>
