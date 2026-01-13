<template>

    <div class="main-container">
        <h2>My Participation</h2>

        <div class="table">
            <table>
                <tr>
                    <th>Event Name</th>
                    <th>Date</th>
                    <th>Type</th>
                    <th>Status</th>
                </tr>
                <tr style="background-color: #A8C2C2;">
                    <td>RoboThinks Webinar</td>
                    <td>January 5, 2026</td>
                    <td>Webinar</td>
                    <td style="color: #00AE1A;">Attended</td>
                </tr>
                <tr>
                    <td>CES Webinar Computer Month</td>
                    <td>January 23, 2026</td>
                    <td>Webinar</td>
                    <td style="color: #DEA40F;">On-going</td>
                </tr>
                <tr style="background-color: #A8C2C2;">
                    <td>Typing Race All Year Level</td>
                    <td>February 6, 2026</td>
                    <td>Contest</td>
                    <td style="color: #DEA40F;">On-going</td>
                </tr>
            </table>
        </div>
    </div>

</template>
<style scoped> 
*{
    font-family: 'Poppins', sans-serif;
}
.main-container {
    background-color: rgba(255, 255, 255, 0.14);
    backdrop-filter: blur(10px);
    margin-top: 40px;
    width: 95%;
    height: 75.5%;
    border-radius: 20px;
    border: solid 2px rgba(255, 255, 255, 0.5);
    padding: 30px;
}
h2 {
    font-weight: 600;
    color: #ffffff;
}
table{
    width: 100%;
    border-collapse: collapse;
    background-color: #DBE4E4;
}
th{
    text-align: left;
    font-size: 20px;
    color: #214444;
    font-weight: 600;
    padding: 10px;
}

tr{
    height: 50px;
    font-size: 15px;
    padding: 10px;
}
td{
    padding: 10px;
    color: #214444;
    font-weight: 500;

}
</style>