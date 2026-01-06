<script setup>
import dashboard from '@/components/Dashboard.vue';
import MyClubs from '@/components/MyClubs.vue';
import DigitalID from '@/components/DigitalID.vue';
import MyParticipation from '@/components/MyParticipation.vue';

import { ref } from 'vue';

const hovered = ref(false);

const component1 = ref(true);
const component2 = ref(false);
const component3 = ref(false);
const component4 = ref(false);

const nav = (mode) => {
    switch (mode) {
        case ('dashboard'):
            component1.value = true;
            component2.value = false;
            component3.value = false;
            component4.value = false;
            console.log('dashboard')
            break;
        case ('myClubs'):
            component1.value = false;
            component2.value = true;
            component3.value = false;
            component4.value = false;
            console.log('myClubs')
            break;
        case ('participation'):
            component1.value = false;
            component2.value = false;
            component3.value = true;
            component4.value = false;
            console.log('participation')
            break;
        case ('id'):
            component1.value = false;
            component2.value = false;
            component3.value = false;
            component4.value = true;
            console.log('id')
            break;
    }
}
</script>
<template>


    <main>
        <div class="sidebar-container">

            <img src="@/assets/logo.png" alt="Logo">

            <div class="sidebar-menu">

                <div class="menu-item" @mouseenter="hovered = 0" @mouseleave="hovered = null"
                    :style="{ color: hovered === 0 ? '#214444' : '#ffffff' }" @click="nav('dashboard')">
                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24"
                        fill="currentColor">
                        <path d="M13 9V3h8v6zM3 13V3h8v10zm10 8V11h8v10zM3 21v-6h8v6z" />
                    </svg>
                    <span>Dashboard</span>
                </div>

                <div class="menu-item" @mouseenter="hovered = 1" @mouseleave="hovered = null"
                    :style="{ color: hovered === 1 ? '#214444' : '#ffffff' }" @click="nav('myClubs')">
                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24"
                        fill="currentColor">
                        <path
                            d="M12 11.385q-1.237 0-2.119-.882T9 8.385t.881-2.12T12 5.386t2.119.88t.881 2.12t-.881 2.118t-2.119.882m-7 7.23V16.97q0-.619.36-1.158q.361-.54.97-.838q1.416-.679 2.834-1.018q1.417-.34 2.836-.34t2.837.34t2.832 1.018q.61.298.97.838q.361.539.361 1.158v1.646z" />
                    </svg>
                    <span>My Clubs</span>
                </div>

                <div class="menu-item" @mouseenter="hovered = 2" @mouseleave="hovered = null"
                    :style="{ color: hovered === 2 ? '#214444' : '#ffffff' }" @click="nav('participation')">
                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 640 640"
                        fill="currentColor">Font Awesome Free v7.1.0 by @fontawesome -
                        https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2026 Fonticons,
                        Inc.-->
                        <path
                            d="M104 112C90.7 112 80 122.7 80 136L80 184C80 197.3 90.7 208 104 208L152 208C165.3 208 176 197.3 176 184L176 136C176 122.7 165.3 112 152 112L104 112zM256 128C238.3 128 224 142.3 224 160C224 177.7 238.3 192 256 192L544 192C561.7 192 576 177.7 576 160C576 142.3 561.7 128 544 128L256 128zM256 288C238.3 288 224 302.3 224 320C224 337.7 238.3 352 256 352L544 352C561.7 352 576 337.7 576 320C576 302.3 561.7 288 544 288L256 288zM256 448C238.3 448 224 462.3 224 480C224 497.7 238.3 512 256 512L544 512C561.7 512 576 497.7 576 480C576 462.3 561.7 448 544 448L256 448zM80 296L80 344C80 357.3 90.7 368 104 368L152 368C165.3 368 176 357.3 176 344L176 296C176 282.7 165.3 272 152 272L104 272C90.7 272 80 282.7 80 296zM104 432C90.7 432 80 442.7 80 456L80 504C80 517.3 90.7 528 104 528L152 528C165.3 528 176 517.3 176 504L176 456C176 442.7 165.3 432 152 432L104 432z" />
                    </svg>
                    <span>My Participations</span>
                </div>

                <div class="menu-item" @mouseenter="hovered = 3" @mouseleave="hovered = null"
                    :style="{ color: hovered === 3 ? '#214444' : '#ffffff' }" @click="nav('id')">
                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24"
                        fill="currentColor">
                        <path
                            d="M14.154 12.462h4.077v-1h-4.077zm0-2.77h4.077v-1h-4.077zm-8.385 5.616h6.616v-.166q0-.875-.88-1.355t-2.428-.48t-2.429.48t-.879 1.355zm3.308-3.616q.633 0 1.066-.433q.434-.434.434-1.067t-.434-1.066t-1.066-.434t-1.066.434t-.434 1.066t.434 1.067t1.066.433M4.616 19q-.691 0-1.153-.462T3 17.384V6.616q0-.691.463-1.153T4.615 5h14.77q.69 0 1.152.463T21 6.616v10.769q0 .69-.463 1.153T19.385 19z" />
                    </svg>
                    <span>My Digital ID</span>
                </div>

                <div class="menu-item" @mouseenter="hovered = 4" @mouseleave="hovered = null"
                    :style="{ color: hovered === 4 ? '#214444' : '#ffffff' }">

                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 640 640"
                        fill="currentColor">Font Awesome Free v7.1.0 by @fontawesome -
                        https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2026 Fonticons,
                        Inc.-->
                        <path
                            d="M569 337C578.4 327.6 578.4 312.4 569 303.1L425 159C418.1 152.1 407.8 150.1 398.8 153.8C389.8 157.5 384 166.3 384 176L384 256L272 256C245.5 256 224 277.5 224 304L224 336C224 362.5 245.5 384 272 384L384 384L384 464C384 473.7 389.8 482.5 398.8 486.2C407.8 489.9 418.1 487.9 425 481L569 337zM224 160C241.7 160 256 145.7 256 128C256 110.3 241.7 96 224 96L160 96C107 96 64 139 64 192L64 448C64 501 107 544 160 544L224 544C241.7 544 256 529.7 256 512C256 494.3 241.7 480 224 480L160 480C142.3 480 128 465.7 128 448L128 192C128 174.3 142.3 160 160 160L224 160z" />
                    </svg>
                    <span>Logout</span>
                </div>
            </div>
        </div>

        <div class="main">

            <!-- Header section with search bar and user info -->
            <div class="header">

                <input type="text" name="" id="" placeholder="Search" />
                <div style="display: flex; gap: 50px; align-items: center;">
                    <h1>Welcome back, Student!</h1> <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60"
                        viewBox="0 0 640 640" fill="#214444">Font Awesome Free v7.1.0 by @fontawesome -
                        https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2026
                        Fonticons,
                        Inc.-->
                        <path
                            d="M470.5 463.6C451.4 416.9 405.5 384 352 384L288 384C234.5 384 188.6 416.9 169.5 463.6C133.9 426.3 112 375.7 112 320C112 205.1 205.1 112 320 112C434.9 112 528 205.1 528 320C528 375.7 506.1 426.2 470.5 463.6zM430.4 496.3C398.4 516.4 360.6 528 320 528C279.4 528 241.6 516.4 209.5 496.3C216.8 459.6 249.2 432 288 432L352 432C390.8 432 423.2 459.6 430.5 496.3zM320 576C461.4 576 576 461.4 576 320C576 178.6 461.4 64 320 64C178.6 64 64 178.6 64 320C64 461.4 178.6 576 320 576zM320 304C297.9 304 280 286.1 280 264C280 241.9 297.9 224 320 224C342.1 224 360 241.9 360 264C360 286.1 342.1 304 320 304zM232 264C232 312.6 271.4 352 320 352C368.6 352 408 312.6 408 264C408 215.4 368.6 176 320 176C271.4 176 232 215.4 232 264z" />
                    </svg>
                </div>
            </div>

            <dashboard v-if="component1" />
            <MyClubs v-if="component2" />
            <DigitalID v-if="component4" />
            <MyParticipation v-if="component3" />
        </div>
    </main>

</template>

<style scoped>
/* Sidebar CSS */
.sidebar-container {
    width: 300px;
    height: 90vh;
    background-color: rgba(255, 255, 255, 0.14);
    backdrop-filter: blur(10px);
    box-sizing: border-box;
    border-radius: 20px;
    margin-left: 10px;
}

img {
    width: 100%;
    padding: 20px;
    margin-top: 30px;
}

.sidebar-menu {
    display: flex;
    flex-direction: column;
    margin-top: 30px;
}

.menu-item {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-top: 30px;
    cursor: pointer;
    font-size: 20px;
    transition: color 0.5s;
    width: 100%;
    padding: 5px 30px;
}

.menu-item:hover {
    background-color: rgba(255, 255, 255, 0.14);
}

/* Main Container CSS */
main {
    background-image: url('@/assets/bg .jpg');
    width: 100dvw;
    height: 100dvh;
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    gap: 20px;
}

.main {
    width: calc(100% - 350px);
    height: 100vh;
}

.header {
    width: 95%;
    height: 10%;
    margin-top: 45px;
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 1);
    border-bottom: 1px solid rgba(255, 255, 255, 0.12);
    border: solid 2px #214444;
    border-radius: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 40px;

}

.header input {
    width: 40%;
    height: 30px;
    border-radius: 10px;
    border: solid 2px rgba(0, 0, 0, 0.3);
    font-size: 15px;
    padding: 10px;
    outline: var('#214444');
}

.header h1 {
    font-size: 30px;
    font-weight: 600;
    color: #214444;
}
</style>
