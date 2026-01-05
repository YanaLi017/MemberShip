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

    <div class="student-dashboard">
        <aside class="sidebar-menu">
            
                <img src="@/assets/logo.png" alt="">

                <div class="menu-container" >

                    <div @mouseenter="isHover('white')" @mouseleave="isHoverOut('#214444')" class="menu-item">
                        <dashboard class="icon" :color="color" :size="'40px'"/>
                        <h1 style="">Dashboard</h1>
                    </div>
                    
                    <div @mouseenter="isHover('white')" @mouseleave="isHoverOut('#214444')" class="menu-item">
                        <dashboard class="icon" :color="color" :size="'40px'"/>
                        <h1 style="">Dashboard</h1>
                    </div>
                </div>

          
        </aside>


        <main>
            <div class="dashboard">
                <h1>Student dashboard</h1>
            </div>
        </main>
    </div>
</template>

<style scoped>
* {
    font-family: 'Poppins', sans-serif;
}

.student-dashboard {
    display: flex;
    background-image: url('@/assets/bg .jpg');
    background-size: cover;
    background-position: center;
}

.sidebar-menu {
    width: 500px;
    background-color: rgba(255, 255, 255, 0.5);

}

.menu-container {
    display: flex;
    flex-direction: column;
    margin-top: 50px;
    cursor: pointer;
}

.menu-item {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 10px 20px;
    border-radius: 10px;
    margin-bottom: 20px;
    transition: background-color 0.3s ease;
}

.menu-item h1{
    color: #214444;
    font-size: 20px;
    font-weight: 500;
}

.menu-item:hover{
    background:linear-gradient(135deg, #667eea, #764ba2);
    color: white;
}
main {
    width: 100dvw;
    height: 100dvh;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>