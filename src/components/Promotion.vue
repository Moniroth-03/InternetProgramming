<script>
import Button from './Button.vue';

export default {
  name: "Promotion",
  props: {
    name: String,
    bgButton: String,
    imageUrl: String,
    buttonText: String,
    icon: Object, 
  },
  components: { Button },
}
</script>

<template>
  <div class="flex justify-center h-[220px] items-center w-[470px]  rounded-md shadow-md overflow-hidden relative">
    <div class="flex flex-col m-auto flex-1 px-4 gap-4">
      <div class="flex items-center">
        <h3>{{ name }}</h3>
      </div>
      <Button :background="bgButton" :text="buttonText" :iconComponent="icon" />
    </div>

    <div class=" h-full w-1/2">
      <img class="h-full w-full object-contain -right-20 bottom-0" :src="imageUrl" :alt="name" />
    </div>
  </div>
</template>
