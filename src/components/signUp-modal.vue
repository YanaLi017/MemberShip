<script setup>
import { useRouter } from 'vue-router';

const emit = defineEmits([
    "close"
])
const router = useRouter();

const homeView = () => {
  emit("close")
};
const studentSignUp = () => {
  router.push({ name: 'studentsignup' });
};
const clubSignUp = () => {
  router.push({ name: 'clubsignup' });
};
</script>
<template>

        <div class="modal-contianer" @click.self="homeView">
            <div class="modal">
                <div>
                    <img src="@/assets/close.png" @click="homeView" alt="" id="close">
                </div>
                <div class="modal-logo">
                    <img src="@/assets/membership-icon.png" alt="modal-logo">
                </div>

                <div class="modal-option">
                    <button id="modal-button" @click="studentSignUp">I'm a Student</button>
                    <button id="modal-button" @click="clubSignUp">I'm a Club Admin</button>
                </div>
            </div>
        </div>

</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    font-family: 'Poppins', sans-serif;
}


.modal-contianer {
    background-color: rgba(0, 0, 0, 35%);
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100dvw;
    height: 100dvh;
    z-index: 2;
    backdrop-filter: blur(3px);

}

.modal {
    background-color: rgba(225, 225, 225, 1);
    width: 600px;
    height: 300px;
    border-radius: 15px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
}

.modal-logo img {
    width: 150px;
}

.modal-option {
    display: flex;
    gap: 40px;
}

#modal-button {
    width: 180px;
    height: 60px;
    border-radius: 10px;
    border: none;
    background-color: #214444;
    color: white;
    font-size: 18px;
    cursor: pointer;
    padding: 10px;
    font-weight: 500;
    box-shadow: -6px 8px 3px rgba(0, 0, 0, 0.3);
}

#modal-button:hover {
    background-color: #8CADA9;
    color: #214444;

}

#close{
    width: 15px;
    cursor: pointer;
    position: absolute;
    top: 0;
    right: 0;
    margin: 15px;

}
</style>