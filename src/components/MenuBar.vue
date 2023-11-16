<template>
    <nav>
        <h1 v-text="title"></h1>
        <div class="display flex justify-between">
            <p style="font-weight: bold;">All</p>
            <p>Milks & Dairies</p>
            <p>Coffes & Teas</p>
            <p>Pet Foods</p>
            <p>Meats</p>
            <p>Vegetables</p>
            <p>Fruits</p>
        </div>
    </nav>
</template>

<script>
    export default{
        props: {
            title: String,
    }
}
</script>
<style>
    nav {
        display:flex;
        margin:1rem 0;
    }
    h1{
        color: black;
        font-size: 32px;
    }
    .menu {
        display:flex;
        gap:2rem;
        font-size: 16px;
    }
</style>