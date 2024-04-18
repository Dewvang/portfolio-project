<template>
    <hr class="hr-1" />
    <footer id="footer">
        <div class="footer-wrap">
                <div class="contact-wrap">
                    <div class="contact-box">
                        <h1>Contact me</h1>
                        <p>Sittigon.yeevangtaku@hotmail.com </p>
                        <p>+6689-484-8405</p>
                    </div>
                </div>
            <div class="location-wrap">
                <div class="location-box">
                    <h1>Location</h1>
                    <p>Khlong Nueng Subdistrict</p>
                    <p>Khlong Luang District</p>
                    <p>Pathum Thani Province, 12120</p>
                </div>
            </div>
            <div class="social-wrap">
                <div class="social-item" v-for="(item, key) in contact" :key="key">
                    <a :href="item.link" target="_blank">
                        <img width="25" height="25" :src="require(`@/assets/${item.img}`)" :alt="key" />
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            contact: {
                facebook: {
                    img: 'facebook.png',
                    link: ['https://www.facebook.com/sittigon.yeevangtaku/'],
                },
                instagram: {
                    img: 'instagram.png',
                    link: ['https://www.instagram.com/dewvang/'],
                },
                line: {
                    img: 'line.png',
                    link: ['https://line.me/ti/p/SIlun-5TIK'],
                },
                linkedin: {
                    img: 'linkedin.png',
                    link: ['https://www.linkedin.com/in/sittigon-yeevangtaku-ba074625b/'],
                },
            }
        }
    }
}
</script>

<style scoped>
footer {
    padding-top: 100px;
    padding-bottom: 100px;
}

.footer-wrap {
    color: white;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    text-align: center;
}

.footer-wrap h1 {
    margin-bottom: 20px;
}

.footer-wrap p {
    margin-bottom: 5px;
}

.social-wrap {
    display: flex;
    justify-content: center;
    align-items: center;
}

.social-item {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: white;
    padding: 10px;
    border-radius: 100%;
    margin: 5px;
}

.social-item:hover {
    transform: scale(1.1);
    transition: transform 0.3s ease;
}

.social-wrap {
    display: flex;
    flex-wrap: wrap;
}

.contact-box{
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
}

.location-box {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
}

@media (max-width: 569px) {
    .footer-wrap {
        flex-direction: column;
    }

    .social-wrap {
        margin-top: 50px;
    }

    .location-wrap {
        margin-top: 50px;
    }

    .footer-wrap h1 {
        font-size: 1.2rem;
    }

    .footer-wrap p {
        font-size: 0.8rem;
    }
}

@media (min-width: 570px) and (max-width: 1150px) {
    .footer-wrap {
        flex-direction: column;
    }

    .social-wrap {
        margin-top: 50px;
    }

    .location-wrap {
        margin-top: 50px;
    }
}

@media (min-width: 1151px) {}
</style>
