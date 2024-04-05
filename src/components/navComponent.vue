<template>
    <nav>
        <div class="logo">
            <h1 @click="toPages('home')">LOGO</h1>
        </div>
        
        <div class="hamburger-menu" :class="{ open: isMenuOpen }" @click="toggleMenu">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
        </div>

        <div class="menu-list" :class="{ open: isMenuOpen }">
            <p @click="toPages('about')">ABOUT</p>
            <p @click="toPages('experience')">EXPERIENCE</p>
            <p @click="toPages('skills')">SKILLS</p>
            <p @click="toPages('education')">EDUCATION</p>
            <p @click="toPages('project')">PROJECT</p>
            <p @click="toPages('contact')">CONTACT</p>
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            isMenuOpen: false
        };
    },
    methods: {
        toPages(page) {
            this.$router.push({ name: page }).catch(() => {});
            this.isMenuOpen = false;
        },
        toggleMenu() {
            this.isMenuOpen = !this.isMenuOpen;
        }
    }
}
</script>

<style scoped>
.logo{
    cursor: pointer;
}
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: white;
    margin-top: 10px;
}
.menu-list {
    display: flex;
    justify-content: space-between;
}
.menu-list p {
    cursor: pointer;
    color: white;
    transition: color 0.3s ease;
    padding: 10px;
}
.menu-list p:hover {
    color: red;
}
.hamburger-menu {
    display: none;
    cursor: pointer;
    padding: 10px;
    transition: transform 0.3s ease;
}

.bar {
    width: 25px;
    height: 3px;
    background-color: white;
    margin: 5px 0;
    transition: transform 0.3s ease, opacity 0.3s ease;
}

.hamburger-menu.open .bar:nth-child(1) {
    transform: translateY(8px) rotate(45deg);
}

.hamburger-menu.open .bar:nth-child(2) {
    opacity: 0;
}

.hamburger-menu.open .bar:nth-child(3) {
    transform: translateY(-8px) rotate(-45deg);
}

@media (max-width: 569px) {
    
    nav {
        display: flex;
        flex-direction: column;
    }
    .menu-list {
        display: none;
        flex-direction: column;
        justify-content: center;
        align-items: center; 
        transition: all 1s ease;    
    }
    .menu-list.open {
        display: flex;        
    }
    .menu-list p {
        padding: 10px;
        margin: 5px 0;
    }
    .hamburger-menu {
        display: block;
    }
}

@media (min-width: 570px) and (max-width: 800px) {
    nav {
        display: flex;
        flex-direction: column;
    }
    .menu-list{
        margin-top: 20px;
    }
}


@media (min-width: 801px) {}
</style>