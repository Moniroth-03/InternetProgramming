<script setup>
import Category from './components/Category.vue';
import Promotion from './components/Promotion.vue';
import { ArrowLongRightIcon } from '@heroicons/vue/20/solid';
import img1 from './assets/cat-13 1.png'
import img2 from './assets/cat-11 1.png'
import img3 from './assets/cat-12 1.png'
import img4 from './assets/cat-9 1.png'
import img5 from './assets/cat-3 1.png'
import img6 from './assets/cat-4 1.png'
import img7 from './assets/cat-1 4.png'
import img8 from './assets/cat-15 1.png'
import img9 from './assets/cat-14 1.png'
import img10 from './assets/cat-7 1.png'
import img11 from './assets/Cms-04 1.png'
import img12 from './assets/Cat-01 1.png'
import img13 from './assets/Cms-03 1.png'



const fruits = [
  {
    name: 'Cake & Milk',
    imageUrl: img1,
    description: '3 items',
    bg: "bg-[#F2FCE4]",
  },
  {
    name: 'Peach',
    imageUrl: img2,
    description: '4 items',
    bg: "bg-[#FFFCEB]"
  },
  {
    name: 'Oganic Kiwi',
    imageUrl: img3,
    description: '4 items',
    bg: "bg-[#ECFFEC]"
  },
  {
    name: 'Red Apple',
    imageUrl: img4,
    description: '4 items',
    bg: "bg-[#FEEFEA]"
  },
  {
    name: 'Snack',
    imageUrl: img5,
    description: '4 items',
    bg: "bg-[#FFF3EB]"
  },
  {
    name: 'Black Plum',
    imageUrl: img6,
    description: '4 items',
    bg: "bg-[#FFF3FF]"
  },
  {
    name: 'Vegetables',
    imageUrl: img7,
    description: '4 items',
    bg: "bg-[#F2FCE4]"
  },
  {
    name: 'Headphone',
    imageUrl: img8,
    description: '4 items',
    bg: "bg-[#FFFCEB]"
  },
  {
    name: 'Cake & Milk',
    imageUrl: img9,
    description: '4 items',
    bg: "bg-[#F2FCE4]"
  },
  {
    name: 'Orange',
    imageUrl: img10,
    description: '4 items',
    bg: "bg-[#FFF3FF]"
  },
];

const promotions = [
  {
    name: 'Everyday Fresh & Clean with Our Products',
    imageUrl: img11,
    description: '3 items',
    bg: "bg-[#F0E8D5]",
    button: "Shop Now",
    bgButton :"bg-[#3BB77E]",
    icon: ArrowLongRightIcon, 
  },
  {
    name: 'Make your Breakfast Healthy and Easy',
    imageUrl: 'https://s3-alpha-sig.figma.com/img/2738/f29f/1c4542246febe8c91ddb74ce42b81c5d?Expires=1699833600&Signature=JNM~Pf22QsnaqWM9RZvWG64rjJo-lwfl9CDQ92UKMr6C28gHlbdnOOztzCIiPSRH0g5qkVqbTgGQdrEMyPelGVWQddeCtybMyNUd65D4~cPXAB07xITVuyQVMRet1JACTy8dCeWb8T9iQmnqVt0YR2uHQWVulaiHJnCwld~CzjbFEs1IyFxhYvreRlGm2iD0vuqOAHgHTfEy0EIUnd1CjWkmc8EZtD4X2HlZsQ2~jLP4m~D6OfzE7ep1TEnDlV6DY-dV1rLk2K1XVxF13VbfgrM-Bpo10mw0Dsf2eLV-7UlbFfJhzRPEBW7ZKd23-YWQ-pglVOnpWEJtXuTNrvYUFA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4',
    description: '4 items',
    bg: "bg-[#F3E8E8]",
    button: "Shop Now",
    bgButton :"bg-[#3BB77E]",
    icon: ArrowLongRightIcon,
  },
  {
    name: 'The best Organic Products Online',
    imageUrl: img13,
    description: '4 items',
    bg: "bg-[#E7EAF3]",
    button: "Shop Now",
    bgButton :"bg-[#FDC040]",
    icon: ArrowLongRightIcon, 
  },
];

</script>

<template>
  <section class="flex flex-col gap-12 items-center justify-center h-screen">
    <div className="flex gap-4">
      <Category :class="fruit.bg" v-for="(fruit, index) in fruits" :key="index" :image="fruit.imageUrl" :name="fruit.name" :description="fruit.description" />
    </div>
    <div class="flex justify-center gap-4">
      <Promotion :icon="promotion.icon" :class="promotion.bg+ ` flex justify-center`" v-for="(promotion, index) in promotions" :key="index" :name="promotion.name" :bgButton="promotion.bgButton" :buttonText="promotion.button" :imageUrl="promotion.imageUrl"   />
    </div>
  </section>
</template>
