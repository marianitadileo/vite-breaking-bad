<script>
export default {
    name: "AppHeader",
    props: {
        title: String
    }
}
</script>

<template>
    <header class="ms_header d-flex">
        <img class="ms_logo" src="../assets/logo-yu-gi-oh.jpg" alt="">
        <h1 class="p-3">{{ title }}</h1>
    </header>
</template>

<style scoped lang="scss">
.ms_header {
    height: 80px;
}

.ms_logo {
    width: 10%;
    padding: 10px;
    text-align: left;
}
</style>