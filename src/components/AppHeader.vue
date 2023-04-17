<script>
export default {
    name: "AppHeader",
    props: {
        title: String
    }
}
</script>

<template>
    <header>
        <h1 class="p-4">{{ title }}</h1>
    </header>
</template>

<style scoped lang="scss">
header {
    background-color: lightblue;
    height: 100px;
    width: 100%;
}
</style>