<template>
    <nav>
        <div class="logo">
            <h1 @click="toPages('home')">LOGO</h1>
        </div>
        <div class="menu-list">
            <p @click="toPages('about')">ABOUT</p>
            <p>EXPERIENCE</p>
            <p>SKILLS</p>
            <p>EDUCATION</p>
            <p>PROJECT</p>
            <p>CONTACT</p>
        </div>
    </nav>
</template>

<script>
export default {
    methods: {
        toPages(page) {
            this.$router.push({ name: page }).catch(() => { });
        },
    },
}
</script>

<style scoped>
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: white;
    margin-top: 10px;
}

.menu-list {
    width: 530px;
    display: flex;
    justify-content: space-between;
    
}

.menu-list p {
    cursor: pointer;
    color: white;
    transition: color 0.3s ease;
}

.menu-list p:hover {
    color: red;
}

@media (max-width: 768px) {
    nav {
        display: flex;
        flex-direction: column;
    }

    .menu-list {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .menu-list p{
        margin-top: 10px;
    }
}


@media (min-width: 769px) and (max-width: 849px) {
    nav {
        display: flex;
        flex-direction: column;
    }
    .menu-list{
        margin-top: 20px;
    }
}


@media (min-width: 849px) {}
</style>