<template>
    <hr class="hr-1" />
    <div class="project" id="project">
        <h1>Project</h1>
        <div class="project-wrap">
            <div class="project-item" v-for="(web, key) in webProject" :key="key">
                <a :href="web.link" target="_blank">
                    <div class="image-wrapper">
                        <img width="250" height="auto" :src="require(`@/assets/${key}.jpg`)" :alt="web.name" />
                        <div class="overlay">
                            <p>{{ web.name }}</p>
                            <p>{{ web.skillUse.join(', ') }}</p>
                        </div>
                    </div>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            webProject: {
                web1: {
                    name: 'Food web',
                    skillUse: ['html', 'css'],
                    link: 'https://serene-lolly-f3d878.netlify.app/'
                },
                web2: {
                    name: 'Portfolio web',
                    skillUse: ['html', 'css', 'bootstrap'],
                    link: 'https://sittigon-yeevangtaku.netlify.app/'
                },
                web3: {
                    name: 'Food web',
                    skillUse: ['html', 'css'],
                    link: 'https://heroic-smakager-d99866.netlify.app/'
                },
                web4: {
                    name: 'Personal web',
                    skillUse: ['html', 'css'],
                    link: 'https://vocal-kitten-7b9623.netlify.app/'
                },
                web5: {
                    name: 'Product web',
                    skillUse: ['html', 'css'],
                    link: 'https://monumental-brigadeiros-92f336.netlify.app/'
                },
                web6: {
                    name: 'Game web',
                    skillUse: ['html', 'css'],
                    link: 'https://beautiful-cascaron-1d49e9.netlify.app/'
                },
                web7: {
                    name: 'Calculator web',
                    skillUse: ['html', 'css', 'Javascript'],
                    link: 'https://fantastic-raindrop-188e24.netlify.app/'
                },
                web8: {
                    name: 'Color random web',
                    skillUse: ['html', 'css', 'Javascript'],
                    link: 'https://comforting-crisp-037b95.netlify.app/'
                },
                web9: {
                    name: 'Weather web',
                    skillUse: ['html', 'css', 'Javascript'],
                    link: 'https://subtle-moxie-e4046d.netlify.app/'
                },
                web10: {
                    name: 'Pirme number web',
                    skillUse: ['html', 'css', 'Javascript'],
                    link: 'https://classy-ganache-7f96e3.netlify.app/'
                },
                web11: {
                    name: 'Todo web',
                    skillUse: ['html', 'css', 'Javascript'],
                    link: 'https://timely-shortbread-776579.netlify.app/'
                },
                web12: {
                    name: 'Try api',
                    skillUse: ['html', 'css', 'Javascript'],
                    link: 'https://sage-dango-4f5044.netlify.app/'
                },
            }
        }
    },
    
};
</script>

<style scoped>
.project {
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding-top: 50px;
    padding-bottom: 100px;
    background-image: url('/src/assets/section.svg');
    background-size: 120%;
    background-position: top;
    background-repeat: no-repeat;
}

.project-wrap {
    padding-top: 50px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.project-item {
    padding: 20px;
    position: relative;
    transition: transform 0.3s ease;
}

.project-item img {
    border: 2px white solid;
    border-color: #a445b2;
    box-shadow: 0 0 15px #a445b2;
    border-radius:10px ;
}


.project-item:hover {
    transform: scale(1.1);
}

.image-wrapper {
    position: relative;
}

.overlay {
    width: 99%;
    position: absolute;
    top: 78%; 
    left: 50%; 
    transform: translate(-50%, -50%); 
    opacity: 0;
    transition: opacity 0.3s ease;
    text-align: center;
    text-decoration: none;
    font-weight: bolder;
    color: white;
    background-color: rgba(0, 0, 0, 0.5);
}

.project-item:hover .overlay {
    opacity: 1;
}
</style>