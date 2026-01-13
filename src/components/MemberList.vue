<template>
<div class="main-container">
        <h2>Member List</h2>

        <div class="table">
            <table>
                <tr>
                    <th>Name</th>
                    <th>Student ID</th>
                    <th>Course</th>
                    <th>Year</th>
                    <th>Status</th>
                    <th>Member Fee</th>
                </tr>
                <tr style="background-color: #A8C2C2;">
                    <td>Veronica Zero</td>
                    <td>AU234574949</td>
                    <td>COEDT</td>
                    <td>4TH</td>
                    <td style="color: #AE0000;">Inactive</td>
                    <td style="color: #AE0000;">Unpaid</td>
                </tr>
                <tr style="background-color: #A8C2C2;">
                    <td>Lyka Gomez</td>
                    <td>AU2346464</td>
                    <td>BSIT</td>
                    <td>1st</td>
                    <td style="color: #00AE1A;">Active</td>
                    <td style="color: #00AE1A;">Paid</td>
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
    font-size: 17px;
    padding: 10px;
}
td{
    padding: 10px;
    color: #214444;
    font-weight: 500;

}
</style>