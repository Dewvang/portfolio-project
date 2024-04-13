<template>
    <hr class="hr-1" />
    <div class="exp" id="exp">
        <div class="exp-content-wrap">
            <h1>Experiences</h1>
            <div class="exp-content">
                <div class="exp-content-img-bg">
                    <div class="exp-content-img">
                        <LottieAnimation :animationData="animationData" :loop="true" class="lottie-animation" />
                    </div>
                </div>
                <div class="exp-content-text-box">
                    <div class="exp-content-text">
                        <h4>Mar 2023 - Presen</h4>
                        <h2>Electrical engineer, Freelance</h2>
                        <p>Narawadee Property Company Limited</p>
                    </div>
                    <div class="exp-content-text">
                        <h4>October 2021 - February 2023</h4>
                        <h2>Electrical engineer</h2>
                        <p>Sangchai Lighting Company Limited</p>
                    </div>
                    <div class="exp-content-text">
                        <h4>May 2016 - August 2016</h4>
                        <h2>Trainee engineer</h2>
                        <p>The Electricity Generating Public Company Limited</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { LottieAnimation } from 'lottie-web-vue';

export default {
    components: {
        LottieAnimation,
    },
    data() {
        return {
            animationData: require('@/assets/Animation1.json'),
        };
    },
};
</script>

<style scoped>
.exp {
    color: white;
    display: flex;
    padding-top: 50px;
    padding-bottom: 100px;
    background-image: url('/src/assets/section.svg');
    background-size: 120%;
    background-position: top;
    background-repeat: no-repeat;
}

.exp-content-wrap {
    display: flex;
    flex-direction: column;
    width: 100%;
}

.exp-content {
    margin-top: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.exp-content-text{
    transition: transform 0.3s ease;
    cursor: pointer;
}

.exp-content-text:hover {
    transform: scale(1.1);
}

.exp-content-wrap h1 {
    font-size: 2rem;
    text-align: center;
    text-shadow: 0 0 50px #a445b2;
}

.exp-content-img-bg {
    background-image: linear-gradient(45deg, #3023ae 0%, #ff0099);
    background-blend-mode: multiply;
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    animation: borderAnimation 50s infinite alternate;
}

.exp-content-img {
    animation: moveUpDown 2s infinite alternate;
}

@keyframes borderAnimation {

    0%,
    100% {
        border-radius: 40% 60% 60% 40% / 40% 60% 60% 40%;
    }

    10% {
        border-radius: 60% 40% 30% 70% / 40% 70% 30% 60%;
    }

    20% {
        border-radius: 80% 20% 50% 50% / 50% 30% 70% 50%;
    }

    30% {
        border-radius: 50% 50% 50% 50% / 40% 50% 50% 40%;
    }

    40% {
        border-radius: 50% 50% 80% 20% / 80% 50% 50% 20%;
    }

    50% {
        border-radius: 100%;
    }

    60% {
        border-radius: 60% 40% 50% 50% / 70% 70% 30% 30%;
    }

    70% {
        border-radius: 50% 50% 50% 50% / 30% 30% 70% 70%;
    }

    80% {
        border-radius: 50% 50% 50% 50% / 30% 70% 70% 30%;
    }

    90% {
        border-radius: 30% 70% 30% 70% / 30% 70% 30% 70%;
    }
}

@keyframes moveUpDown {
    0% {
        transform: translateY(0);
    }

    100% {
        transform: translateY(-20px);
    }
}

.exp-content-text-box {
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.exp-content-text {
    margin-top: 28px;
    width: 100%;
    height: 90%;
    border: solid 1px;
    border-radius: 10px;
    padding: 30px;
    border-color: #a445b2;
    box-shadow: 0 0 10px #a445b2;
    background: linear-gradient(180deg,
            rgb(21, 23, 47) 0%,
            rgba(16, 17, 37, 1) 100%);
}

.lottie-animation {
    width: 400px;
    height: auto;
}

@media (max-width: 569px) {
    .exp-content {
        display: flex;
        flex-direction: column;
    }

    .lottie-animation {
        width: 300px;
        height: auto;
    }

    .exp-content-text-box {
        width: 100%;
        margin-top: 25px;
    }

    .exp-content-text h2 {
        font-size: 1.3rem;
    }

    .exp-content-text p {
        font-size: 0.8rem;
    }
}

@media (min-width: 570px) and (max-width: 1100px) {
    .exp-content {
        display: flex;
        flex-direction: column;
    }


    .exp-content-text-box {
        width: 100%;
        margin-top: 25px;
    }

    .exp-content-text h2 {
        font-size: 1.3rem;
    }

    .exp-content-text p {
        font-size: 0.8rem;
    }
}

@media (min-width: 1101px) {}
</style>
