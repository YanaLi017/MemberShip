<template>
    <div class="main-container">
        <h1 class="h1-text">Club Activity Report</h1>
        <div class="reports">
            <div class="summary">
                <h2 class="h2-text">Recent Activity Log</h2>
                <div class="table">
            <table>
                <tr>
                    <th>Date</th>
                    <th>Event Name</th>
                    <th>Type</th>
                    <th>Attendee</th>
                    <th>Status</th>
                </tr>
                <tr style="background-color: #A8C2C2;">
                    <td>Jan. 15, 2026</td>
                    <td>AU234574949</td>
                    <td>COEDT</td>
                    <td>4TH</td>
                    <td style="color: #AE0000;">Inactive</td>
                    
                </tr>
                <tr style="background-color: #A8C2C2;">
                    <td>Lyka Gomez</td>
                    <td>AU2346464</td>
                    <td>BSIT</td>
                    <td>1st</td>
                    <td style="color: #00AE1A;">Active</td>
                   
                </tr>
            </table>
                </div>
            </div>
            <div class="todo">
                <h2 class="h2-text">To do to</h2>
            </div>
        </div>
    
        
    </div>

</template>

<style scoped>
*{
    font-family: 'Poppins', sans-serif;
}
.main-container {
    width: 95%;
    height: 75.5%;
    margin-top: 30px;
    
}

.h1-text {
    color: #ffffff;
    font-weight: 600;
    font-size: 24px;
}

.h2-text {
    color: #ffffff;
    font-size: 23px;
    margin-left: 20px;
    margin-top: 10px;
    text-align: center;
}

.reports {
    width: 100%;
    height: 90%;
    display: flex;
    justify-content: space-between;
}

.summary {
    margin-top: 20px;
    width: 47.5%;
    height: 100%;
    background-color: rgba(219, 228, 228,0.2);
    backdrop-filter: blur(10px);
    color: black;
    border-radius: 20px;
    border: solid 2px #ffffff;
}

table{
    width: 100%;
    border-collapse: collapse;
    background-color: #DBE4E4;
}
th{
    text-align: left;
    font-size: 15px;
    color: #214444;
    font-weight: 600;
    padding: 10px;
   
}

tr{
    height: 30px;
    font-size: 15px;
    padding: 20px;
}
td{
    padding: 10px;
    color: #214444;
    font-weight: 500;

}

.todo {
    margin-top: 20px;
    width: 47.5%;
    height: 100%;
    background-color: rgba(219, 228, 228,0.2);
    backdrop-filter: blur(10px);
    color: black;
    border-radius: 20px;
    border: solid 2px #ffffff;
}
</style>
