<template>

    <div class="myclub-section">
        <h2>My Clubs</h2>

        <div class="clubs-container">
            <div class="clubs">
                <h3 style="width: 50%;">Computer Explorer <br>Society (CES)</h3>
                <div style="display: flex; gap: 10rem; position: absolute; bottom: 10px;">
                    <button id="digital-id">View Digital ID</button>
                    <span>Active Member</span>
                </div>
            </div>
            <div class="clubs">
                <h3 style="width: 50%;">Basketball Club</h3>
                <div style="display: flex; gap: 10rem; position: absolute; bottom: 10px;">
                    <button id="digital-id">View Digital ID</button>
                    <span>Active Member</span>
                </div>
            </div>
            <div class="clubs">
                <h3 style="width: 50%;">ICCT Cisco Student <br> Organization (ICSO)</h3>
                <div style="display: flex; gap: 10rem; position: absolute; bottom: 10px;">
                    <button id="digital-id">View Digital ID</button>
                    <span>Active Member</span>
                </div>
            </div>
        </div>

        <button id="addClub">Add New Club +</button>
    </div>
</template>

<style scoped>

*{
    font-family: 'Poppins', sans-serif;
}
.myclub-section {
    position: relative;
    margin-top: 40px;
    width: 95%;
    height: 75.5%;
    background-color: rgba(255, 255, 255, 0.14);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    border: solid 2px rgba(255, 255, 255, 0.5);
    display: flex;
    flex-direction: column;
    padding: 20px;
}

h2 {
    font-weight: 600;
    color: #ffffff;
}

#addClub {
    position: absolute;
    bottom: 10px;
    right: 10px;
}

.clubs-container {
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 30%;
}

.clubs {
    width: 30%;
    height: 100%;
    background-color: #DBE4E4;
    backdrop-filter: blur(10px);
    border-radius: 20px;
    border: solid 2px rgba(255, 255, 255, 1);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

h3 {
    background-color: #A5CFCF;
    width: auto;
    height: 50%;
    padding: 5px;
    border-radius: 5px;
    color: #214444;
    font-weight: 600;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
}

#digital-id{
    background-color: #214444;
    color: #ffffff;
    padding: 2px 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 12px;
}
span{
    font-size: 13px;
    background-color: #00AE1A;
    color: #ffffff;
    padding: 1px 10px;
    border-radius: 50px;
}
#addClub{
    background-color: #D9E1E1;
    color: #214444;
    padding: 10px 15px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    font-size: 15px;
    font-weight: 700;
    border: solid 2px rgba(255,255,255, 1);
}
</style>