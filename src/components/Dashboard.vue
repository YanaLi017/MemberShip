<script setup>
    import dateTime from '@/components/Date&time.vue';
    import weather from '@/components/Weather.vue';
</script>

<template>
    <!-- Main content area -->
    <div class="content">

        <!-- Events -->
        <div class="school-events">
            <h3>Upcoming Events</h3>
            <div class="incoming-event"> <span>Robothinks 🤖🧠</span>
                <p>Webinar Lecture</p>
                <p style="font-size: 10px; margin-top: auto;">Jan 5, 2026 || 10am - 5pm</p>
            </div>
            <div class="other-events">
                <div class="events"> <span>Ces Webinar</span>
                    <p>Computer Month</p>
                    <p style="font-size: 9px; margin-top: auto;">Jan 23, 2026 || 10am - 5pm</p>
                </div>
                <div class="events"> <span>Typing Race</span>
                    <p>All year level</p>
                    <p style="font-size: 9px; margin-top: auto;">Feb 6, 2026 || 10am - 5pm</p>
                </div>
                <div class="events"> <span>Design a Page</span>
                    <p>Environmental Website Contest</p>
                    <p style="font-size: 9px; margin-top: auto;">Jan 5, 2026 || 10am - 5pm</p>
                </div>
            </div>
        </div>

        <!-- My Clubs -->
        <div class="my-clubs">
            <div class="header-club">
                <h3>My Clubs</h3> <span>View All>></span>
            </div>
            <div style="width: 100%; height: 100%; gap: 20px; display: flex; flex-direction: column;">
                <div class="clubs-list">
                    <h3>CES - Computer Explorer Society</h3> <span>Active Member</span>
                </div>
                <div class="clubs-list">
                    <h3>Tourist Club</h3>
                </div>
            </div>
        </div>
    </div>


    <div class="lower-section">
        <!-- DateTime & Weather -->
        <div class="date-time">
            <div>
                <dateTime />
            </div>
            <div>
                <weather />
            </div>
        </div>

        <!-- announcement -->
        <div class="announcement">
            <h3>Club Announcement</h3>

            <div class="announcement-content">
                <h4>Rewenal of Membership - CES</h4>
                <ul class="announcement-list">
                    <li>Dealine: March 14, 2026</li>
                    <li>Membership Fee: &#8369;20.00</li>
                    <li>Payment Method: Cash or Online</li>
                </ul>
                <p>Note: Don't miss out on upcoming workshops, networking events, and project opportunities.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
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

.lower-section {
    width: 95%;
    height: 30%;
    margin-top: 20px;
    border-radius: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.date-time {
    width: 50%;
    height: 100%;
    background-color: rgba(255, 255, 255, 0.14);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    border: solid 2px rgba(255, 255, 255, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 40px;
}

.announcement {
    width: 40%;
    height: 100%;
    background-color: rgba(255, 255, 255, 0.14);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    border: solid 2px rgba(255, 255, 255, 0.5);
    display: flex;
    flex-direction: column;
    padding: 10px;
}

.announcement h3 {
    text-align: center;
    color: #fff;
    font-weight: 500;
}

.announcement-content {
    width: 100%;
    height: auto;
    background-color: #DBE4E4;
    border-radius: 10px;
    border: solid 2px rgba(255, 255, 255, 1);
    display: flex;
    flex-direction: column;
    padding: 5px;
}

.announcement-content h4 {
    color: #214444;
    font-weight: 600;
}

.announcement-list li {
    color: #214444;
    font-weight: 400;
    font-size: 12px;
    margin-left: 15px;
    list-style-type: disc;
}

.announcement-content p {
    color: #214444;
    font-weight: 300;
    font-size: 12px;
    margin-top: 10px;
}
</style>