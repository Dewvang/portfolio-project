<template>
    <hr class="hr-1" />
    <div class="skills" id="skills">
        <h1>Programming</h1>
        <div class="skills-dev">
            <div class="skills-item" v-for="skill in devSkill" :key="skill">
                <img width="100" height="100" :src="require(`@/assets/${skill}.svg`)" alt="" />
                {{ capitalize(skill) }}
            </div>
        </div>
        <h1>Other</h1>
        <div class="skills-engineer">
            <div class="skills-item" v-for="skill in engineerSkill" :key="skill">
                <img width="100" height="100" :src="require(`@/assets/${skill}.svg`)" alt="" />
                {{ capitalize(skill) }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            devSkill: ['c','html','css','javascript','tailwind','vue','vscode','bootstrap'],
            engineerSkill: ['autocad','sketchup','dialux','canva','github','git']
        }
    },
    methods: {
        capitalize(text) {
            if (!text) return '';
            return text.charAt(0).toUpperCase() + text.slice(1);
        }
    }
}
</script>

<style scoped>
.skills{
    color: white;
    display: flex;
    flex-direction: column;
    padding-top: 50px;
    padding-bottom: 50px;
    background-image: url('/src/assets/hero.svg');
    background-size: 120%; 
    background-position: top; 
    background-repeat: no-repeat; 
    
}
.skills-dev{
    margin-top:20px ;
    margin-bottom:50px ;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
.skills-item{
    padding: 25px;
    display: flex;
    flex-direction:column ;
    text-align: center;
    transition: transform 0.3s ease;
    cursor: pointer;
}

.skills-item img{
    margin-bottom:10px ;
}

.skills-item:hover {
    transform: scale(1.1);
    border: 1px white solid;
    border-radius: 10px;
    border-color: #a445b2;
    box-shadow: 0 0 10px #a445b2;
}

h1 {
    color: white;
    font-size: 2rem;
    text-align: center;
    text-shadow: 0 0 50px #a445b2;
}

.skills-engineer{
    margin-top:20px ;
    margin-bottom:50px ;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
</style>
