<template>
    <hr class="hr-1" />
    <div class="education" id="education">
        <div class="education-content-wrap">
            <h1>Education</h1>
            <div class="education-content">
                <div class="education-content-text-box">
                    <div class="education-content-text">
                        <h4>2014 - 2019</h4>
                        <h2>Thammasat University</h2>
                        <p>Industrial Electrical Engineering</p>
                    </div>
                    <div class="education-content-text">
                        <h4>2007 - 2013</h4>
                        <h2>Satit Valaya Alongkorn Rajabhat University</h2>
                        <p>Scienc-Math</p>
                    </div>
                </div>
                <div class="education-content-img-bg">
                    <div class="education-content-img">
                        <LottieAnimation :animationData="animationData" :loop="true" class="lottie-animation" />
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
            animationData: require('@/assets/study.json'),
        };
    },
};
</script>

<style scoped>
.education {
    color: white;
    display: flex;
    padding-top: 50px;
    padding-bottom: 100px;
    background-image: url('/src/assets/section.svg');
    background-size: 120%; 
    background-position: top; 
    background-repeat: no-repeat; 
}

.education-content-wrap {
    display: flex;
    flex-direction: column;
    width: 100%;
}

.education-content {
    margin-top: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.education-content-text{
    transition: transform 0.3s ease;
    cursor: pointer;
}

.education-content-text:hover {
    transform: scale(1.1);
}

.education-content-wrap h1 {
    font-size: 2rem;
    text-align: center;
    text-shadow: 0 0 50px #a445b2;
}

.education-content-img-bg {
    background-image: linear-gradient(45deg, #3023ae 0%, #ff0099);
    background-blend-mode: multiply;
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    animation: borderAnimation 50s infinite alternate;
}

.education-content-img {
    animation: moveUpDown 2s infinite alternate;
}

@keyframes borderAnimation {

0%, 100% {
    border-radius: 40% 60% 60% 40% / 40% 60% 60% 40%;
}

10% {
    border-radius: 50% 50% 50% 50% / 40% 50% 50% 40%;
}

20% {
    border-radius: 60% 40% 50% 50% / 50% 30% 70% 50%;
}

30% {
    border-radius: 80% 20% 50% 50% / 80% 50% 50% 20%;
}

40% {
    border-radius: 100% 0% 0% 100% / 100% 0% 0% 100%;
}

50% {
    border-radius: 60% 40% 30% 70% / 70% 70% 30% 30%;
}

60% {
    border-radius: 50% 50% 50% 50% / 30% 30% 70% 70%;
}

70% {
    border-radius: 50% 50% 50% 50% / 30% 70% 70% 30%;
}

80% {
    border-radius: 30% 70% 30% 70% / 30% 70% 30% 70%;
}

90% {
    border-radius: 40% 60% 60% 40% / 40% 60% 60% 40%;
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

.education-content-text-box {
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.education-content-text {
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
    .education-content {
        display: flex;
        flex-direction: column-reverse;
    }

    .lottie-animation {
    width: 300px;
    height: auto;
}

    .education-content-text-box {
        width: 100%;
        margin-top: 25px;
    }

    .education-content-text h2 {
        font-size: 1.3rem;
    }

    .education-content-text p {
        font-size: 0.8rem;
    }
}

@media (min-width: 570px) and (max-width: 1100px) {
    .education-content {
        display: flex;
        flex-direction: column-reverse;
    }


    .education-content-text-box {
        width: 100%;
        margin-top: 25px;
    }

    .education-content-text h2 {
        font-size: 1.3rem;
    }

    .education-content-text p {
        font-size: 0.8rem;
    }
}

@media (min-width: 1101px) {}
</style>