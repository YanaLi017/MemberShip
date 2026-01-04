<script setup>

defineProps({
    color: {
        type: String,
        default: '#214444',
    },
    size: {
        type: String,

    }
})

</script>
<template>
    <svg xmlns="http://www.w3.org/2000/svg" :width="size" :height="size" viewBox="0 0 24 24"><path :fill="color" d="M13 9V3h8v6zM3 13V3h8v10zm10 8V11h8v10zM3 21v-6h8v6z"/></svg>
</template>