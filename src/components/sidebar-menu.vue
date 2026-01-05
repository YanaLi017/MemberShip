<template>
    <div class="sidebar-menu">
        <aside>
            <slot name="student-sidebar">

            </slot>
        </aside>
    </div>
</template>
<style scoped>
.sidebar-menu {
    display: flex;
    flex-direction: column;
    overflow: hidden;
}
</style>