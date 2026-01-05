<script setup>
import sideBar from '@/components/SideBar.vue';
</script>

<template>
    <main>
        <sideBar />
        <div class="main">

            <!-- Header section with search bar and user info -->
            <div class="header">
                <input type="text" name="" id="" placeholder="Search" />
                <h1>Welcome back, Student!</h1>
                <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 640 640" fill="#214444">Font
                    Awesome Free v7.1.0 by @fontawesome -
                    https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2026 Fonticons,
                    Inc.-->
                    <path
                        d="M470.5 463.6C451.4 416.9 405.5 384 352 384L288 384C234.5 384 188.6 416.9 169.5 463.6C133.9 426.3 112 375.7 112 320C112 205.1 205.1 112 320 112C434.9 112 528 205.1 528 320C528 375.7 506.1 426.2 470.5 463.6zM430.4 496.3C398.4 516.4 360.6 528 320 528C279.4 528 241.6 516.4 209.5 496.3C216.8 459.6 249.2 432 288 432L352 432C390.8 432 423.2 459.6 430.5 496.3zM320 576C461.4 576 576 461.4 576 320C576 178.6 461.4 64 320 64C178.6 64 64 178.6 64 320C64 461.4 178.6 576 320 576zM320 304C297.9 304 280 286.1 280 264C280 241.9 297.9 224 320 224C342.1 224 360 241.9 360 264C360 286.1 342.1 304 320 304zM232 264C232 312.6 271.4 352 320 352C368.6 352 408 312.6 408 264C408 215.4 368.6 176 320 176C271.4 176 232 215.4 232 264z" />
                </svg>
            </div>

            <!-- Main content area -->
            <div class="content">

                <!-- Events -->
                <div class="school-events">
                    <h3>Upcoming Events</h3>

                    <div class="incoming-event">
                        <span>Robothinks 🤖🧠</span>
                        <p>Webinar Lecture</p>
                        <p style="font-size: 10px; margin-top: auto;">Jan 5, 2026 || 10am - 5pm</p>
                    </div>


                    <div class="other-events">

                        <div class="events">
                            <span>Ces Webinar</span>
                            <p>Computer Month</p>
                            <p style="font-size: 9px; margin-top: auto;">Jan 23, 2026 || 10am - 5pm</p>
                        </div>

                        <div class="events">
                            <span>Typing Race</span>
                            <p>All year level</p>
                            <p style="font-size: 9px; margin-top: auto;">Feb 6, 2026 || 10am - 5pm</p>
                        </div>

                        <div class="events">
                            <span>Design a Page</span>
                            <p>Environmental Website Contest</p>
                            <p style="font-size: 9px; margin-top: auto;">Jan 5, 2026 || 10am - 5pm</p>
                        </div>
                    </div>
                </div>

                <!-- My Clubs -->
                <div class="my-clubs">

                    <div class="header-club">
                        <h3>My Clubs</h3>
                        <span>View All>></span>
                    </div>

                    <div style="width: 100%; height: 100%;  gap: 20px; display: flex; flex-direction: column;">
                        <div class="clubs-list">
                            <h3>CES - Computer Explorer Society</h3>
                            <span>Active Member</span>
                        </div>

                        <div class="clubs-list">
                            <h3>Tourist Club</h3>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>


<style scoped>
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
    height: 15%;
    margin-top: 35px;
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 1);
    border-bottom: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 20px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding-left: 40px;
    gap: 30px;
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

.content {
    width: 95%;
    height: 40%;
    margin-top: 20px;
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 0.14);
    border-radius: 20px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    border: solid 2px rgba(255, 255, 255, 0.5);
}

.school-events {
    width: 55%;
    height: 100%;
    margin-left: 20px;
    display: flex;
    flex-direction: column;
}

.school-events h3 {
    color: #fff;
    font-weight: 500;
}

.incoming-event {
    width: 100%;
    height: 40%;
    background-color: #DBE4E4;
    border-radius: 10px;
    border: solid 2px rgba(255, 255, 255, 1);
    display: flex;
    flex-direction: column;
    padding: 10px 20px;
}

.incoming-event:hover {
    background-color: #c4d0d0;
    translate: 5px -5px;
    cursor: pointer;
}

.incoming-event span {
    color: #214444;
    font-weight: 600;
    text-transform: uppercase;
}

.incoming-event p {
    color: #214444;
    font-weight: 300;
    font-size: 13px;
    margin-left: 10px;
}

.other-events {
    width: 100%;
    height: 45%;
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    gap: 10px;
}

.events {
    background-color: #DBE4E4;
    border-radius: 10px;
    border: solid 2px rgba(255, 255, 255, 1);
    width: 30%;
    height: 100%;
    color: #214444;
    display: flex;
    flex-direction: column;
    padding: 5px 10px;
}

.events:hover {
    background-color: #c4d0d0;
    translate: 5px -5px;
    cursor: pointer;
}

.events span {
    color: #214444;
    font-weight: 600;
    text-transform: uppercase;
    font-size: 13px;

}

.events p {
    color: #214444;
    font-weight: 300;
    font-size: 12px;
    margin-left: 10px;
}

.my-clubs {
    width: 55%;
    height: 95%;
    margin: -10px 10px 5px 20px;
    display: flex;
    flex-direction: column;
}

.my-clubs h3,
span {
    color: #fff;
    font-weight: 500;
}

.header-club {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 10px;
}

.clubs-list {
    position: relative;
    width: 100%;
    height: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 10px;
    border-radius: 10px;
    background-color: #DBE4E4;
    border: solid 2px rgba(255, 255, 255, 1);
    padding: 10px;
}

.clubs-list:hover {
    background-color: #c4d0d0;
    translate: 5px -5px;
    cursor: pointer;
}

.clubs-list h3 {
    color: #214444;
    font-weight: 600;
}

.clubs-list span {
    color: #214444;
    font-weight: 400;
    font-size: 10px;
    bottom: 3px;
    right: 3px;
    position: absolute;
    background-color: #00AE1A;
    border-radius: 50px;
    padding: 1px 5px;
}
</style>