<template>
    <div class="content">
        <div class="settings-page">
            <div class="settings-card">
                <h3>Club Officer Roster</h3>
                <div class="form-group">
                    <label>Club Name:</label>
                    <input type="text" value="Computer Essential Society" readonly>
                </div>
                <div class="form-group">
                    <label>President:</label>
                    <input type="text" value="Francine Orange" readonly />
                </div>
                <div class="form-group">
                    <label>V- President:</label>
                    <input type="text" value="Allie Roy Sanchez" readonly />
                </div>
                <div class="form-group">
                    <label>Secretary:</label>
                    <input type="text" value="Allie Roy Sanchez" readonly />
                </div>
                <div class="btn-container right">
                    <button class="btn-dark">Edit Roster</button>
                </div>
            </div>

            <div class="settings-card">
                <h3>Login Credentials</h3>
                <div class="form-group">
                    <label>Club ID</label>
                    <input type="text" value="CES2023" readonly />
                </div>
                <div class="form-group">
                    <label>Password</label>
                    <input type="password" value="123456">
                </div>
                <div class="form-group">
                    <label>New Club ID</label>
                    <input type="text" value="CES2026" readonly />
                </div>
                <div class="form-group">
                    <label>New Password</label>
                    <input type="password" value="123456">
                </div>
                <div class="btn-container center">
                    <button class="btn-teal">Save Changes</button>
                    <button class="btn-grey">Discard</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.content {
    width: 95%;
    height: 76%;
    margin-top: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.settings-card {
    width: 95%;
    height: 74%;
    background-color: rgb(33, 68, 68, 0.4);
    backdrop-filter: blur(10px);
    margin-top: 40px;
    border-radius: 20px;
    border: solid 2px rgba(255, 255, 255, 0.5);
    padding: 30px;
    display: flex;
}

</style>