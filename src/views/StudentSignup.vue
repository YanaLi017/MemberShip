<template>
    <main>
        <div class="card">
            <div>
                <img src="@/assets/logo.png" alt="Logo">
            </div>
            <div class="title">
                <h1>Create Your Account</h1>
            </div>
            <div class="form">
                <input type="text" placeholder="Full Name">
                <input type="text">
            </div>
        </div>
    </main>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

main {
    background-image: url('@/assets/bg .jpg');
    width: 100dvw;
    height: 100dvh;
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
}
.card {
    width: 50rem;
    height: 40rem;
    background-color: rgba(255, 255, 255, 0.4);
    backdrop-filter: blur(5px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 20px;
}
.title h1{
    font-size: 30px;
    font-weight: 600;
    color: #214444;
}
.form{
    display: flex;
    gap: 100px;
    margin-top: 30px;
}
input{
    width: 200px;
    height: 40px;
    border-radius: 10px;
    border: none;
    padding: 10px;
    font-size: 16px;
}
</style>