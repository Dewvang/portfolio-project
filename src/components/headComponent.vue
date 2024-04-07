<template>
    <header>
        <div class="header-content">
            <h1 class="gradient-text">Hi, I'm Dew.</h1>
            <h2>I'm an electrical engineer,</h2>
            <h2>but now I want to be a Dev.</h2>
        </div>
        <div>
            <img :src="require('@/assets/Profile.png')" alt="" />
        </div>
    </header>
</template>

<script>

export default {
};
</script>

<style scoped>
header {
    display: flex;
    margin-top: 100px;
}

.header-content {
    width: 60%;
    display: flex;
    justify-content: center;
    flex-direction: column;
}

.header-content h1 {
    font-size: 4rem;
    color: transparent;
    -webkit-background-clip: text;
    background-clip: text;
    background-image: linear-gradient(-225deg,
            #a445b2 0%,
            #d41872 52%,
            #ff0066 100%);
}

.header-content h2 {
    font-size: 3rem;
    color: white;
}

@keyframes borderAnimation {

    0%,
    100% {
        border-radius: 30% 70% 70% 30% / 30% 52% 48% 70%;
    }

    10% {
        border-radius: 50% 50% 20% 80% / 25% 80% 20% 75%;
    }

    20% {
        border-radius: 67% 33% 47% 53% / 37% 20% 80% 63%;
    }

    30% {
        border-radius: 39% 61% 47% 53% / 37% 40% 60% 63%;
    }

    40% {
        border-radius: 39% 61% 82% 18% / 74% 40% 60% 26%;
    }

    50% {
        border-radius: 100%;
    }

    60% {
        border-radius: 50% 50% 53% 47% / 72% 69% 31% 28%;
    }

    70% {
        border-radius: 50% 50% 53% 47% / 26% 22% 78% 74%;
    }

    80% {
        border-radius: 50% 50% 53% 47% / 26% 69% 31% 74%;
    }

    90% {
        border-radius: 20% 80% 20% 80% / 20% 80% 20% 80%;
    }
}

header img {
    background-image: linear-gradient(45deg, #3023ae 0%, #ff0099);
    background-blend-mode: multiply;
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    animation: borderAnimation 50s infinite alternate;
}

@media (max-width: 569px) {
    header {
        display: flex;
        flex-direction: column-reverse;
        justify-content: center;
        align-items: center;
        margin-top: 50px;
    }

    .header-content {
        width: 100%;
        display: flex;
        justify-content: center;
        align-content: center;
        text-align: center;
        margin-top: 20px;
    }

    header img {
        width: 300px;
        height: 300px;
    }

    .header-content h1 {
        font-size: 2.5rem;
    }

    .header-content h2 {
        font-size: 1.5rem;
    }
}

@media (min-width: 570px) and (max-width: 1120px) {
    header {
        display: flex;
        flex-direction: column-reverse;
        justify-content: center;
        align-items: center;
        margin-top: 40px;
    }

    .header-content {
        width: 100%;
        display: flex;
        justify-content: center;
        align-content: center;
        text-align: center;
        margin-top: 20px;
    }

    header img {
        width: 400px;
        height: 400px;
    }

    .header-content h1 {
        font-size: 3rem;
    }

    .header-content h2 {
        font-size: 2rem;
    }
}

@media (min-width: 1121px) {}
</style>