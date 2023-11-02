<template>
    <div class="h-[170px] w-[130px] rounded-md shadow-md overflow-hidden">
       <img class="h-[120px] w-full" :src="image" :alt="image" />
        <h3 class="text-center font-semibold">{{ name }}</h3>
        <p class="text-center text-xs text-[#ffffff]">{{ description }}</p>
    </div>
</template>

<script>

    export default {
        name: "Category",
        props:[ 
            'image',
            'name',
            'description']
    }
</script>

