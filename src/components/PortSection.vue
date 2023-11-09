<script setup>
import { portText } from "@/constants/index";
</script>

<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                portfolio <em>포폴 작업물</em>
            </div>
            <div class="port__wrap">
                <div v-for="(text, key) in portText" :key="key" :class="['port__item p' + (key + 1)]">
                    <span class="num">{{ key + 1 }}.</span>
                    <a :href="text.img" target="_blank">
                        <img :src="portText.img" alt="포트폴리오 이미지">
                    </a>
                    <h3 class="title">{{ text.title }}</h3>
                    <p class="desc">
                        {{ text.desc }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger"
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 1),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top 56px",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: false,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}
</script>

<style lang="scss">
#port {
    width: 100%;
    overflow: hidden;
}

.port__inner {
    padding: 16px;
}

.port__title {
    width: 100%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    font-family: var(--mainKor-font);
    text-transform: uppercase;
    color: var(--white);
    border-bottom: 0.4vw solid var(--white);
    margin-bottom: 16px;
    text-indent: -0.26vw;
}

.port__title em {
    font-size: 1.25rem;
    font-weight: 400;
    line-height: 2;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}

.port__item {
    width: 500px;
    height: 70vh;
    background-color: var(--white);
    margin-right: 20px;
    padding: 2.5rem;
}

.port__item .desc {
    color: black;
    font-size: 1.2rem;
}

.port__item .num {
    color: black;
    font-size: 2rem;
}

.port__item img {
    border-radius: 5px;
    -webkit-filter: saturate(0);
    filter: saturate(0);
    transition: all .3s;
    transition: margin-top 0.3s;
}

.port__item img:hover {
    margin-top: 0;
    filter: saturate(100%);
}

.port__item .title {
    font-size: 1.5rem;
    text-align: center;
    padding: 0.8rem 0;
    font-weight: 700;
    color: var(--black);
    border-bottom: 2px solid var(--black);
    margin-bottom: 1rem;
}

.port__item .site {
    border: 1px solid var(--black100);
    display: block;
    text-align: center;
    padding: 0.625rem 1.5rem;
    margin-top: 1.5rem;
    transition: all 0.2s;
}
</style>