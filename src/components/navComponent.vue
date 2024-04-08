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
            <a  href="#exp">EXPERIENCE</a>
            <a>EDUCATION</a>
            <a>SKILLS</a>
            <a>PROJECT</a>
            <a>CONTACT</a>
        </div>
    </nav>
    <hr class="hr-1" />
</template>

<script>
export default {
    data() {
        return {
            isMenuOpen: false
        };
    },
    methods: {
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
.menu-list a {
    cursor: pointer;
    color: white;
    transition: color 0.3s ease;
    padding: 10px;
    text-decoration: none;
}
.menu-list a:hover {
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