<script setup>
import sideBar from '@/components/sidebar-menu.vue';
import dashboard from '@/components/dashboard-icon.vue';
import { ref } from 'vue';

const color = ref('black');

const isHover = (dashcolor) => {
    color.value = dashcolor;
    console.log(color.value);
}
const isHoverOut = (dashcolor) => {
    color.value = dashcolor;
    console.log(color.value);
}

</script>

<template>
    <aside>
        
    </aside>
</template>