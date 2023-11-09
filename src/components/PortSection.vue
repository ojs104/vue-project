<script setup>
import { portText } from "@/constants/index"
</script>

<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                portfolio <em>포폴 작업물</em>
            </div>
            <div class="port__wrap">
                <div class="port__item p1" v-for="(port, key) in portText" v-bind:key="key">
                    <span class="num">{{ port.num }} </span>
                    <a href="#">
                        <img :src="port.img" alt="리액트를 이용한 포트폴리오">
                    </a>
                    <h3 class="title">리액트를 이용한 포트폴리오</h3>
                    <p class="desc">
                        이 사이트는 정말 인상적인 포트포폴리옵 입니다.
                        특히 스무스한 효과와 가로모드등 높은 퀄리티를 자랑합니다.
                        디테일과 꼼꼼함이 넘치는 포트폴리오는 개발자의 뛰어난 능력을 엿볼 수 있습니다.GSAP와 React.js를 이용하여 사이트를 표현한 것은 기술적인
                        능력과 창의성을 강조하는데, 부족함이 없으며, 세심한 코딩과 디테일한 작업으로 그외 개별적인 감각과 능력이 빛을 발휘할 것 같습니다.
                    </p>
                    <button>사이트보기</button>
                </div>

            </div>
        </div>

    </section>
</template>
<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
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
                scrollTrigger: { // "ScrollTrigger"가 올바른 대소문자로 수정됨
                    trigger: "#port",
                    start: "top 56px", // start 옵션의 값도 수정됨
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: true,
                    invalidateOnRefresh: true,
                    anticipatePin: 1
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
    position: sticky;
    top: 70px;
    left: 0;
    width: 70%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    font-family: var(--mainKor-font);
    text-transform: uppercase;
    color: var(--white200);
    border-bottom: 0.4vw solid var(--white200);
    margin-bottom: 100px;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}

.port__item {
    width: 500px;
    height: 70vh;
    margin-right: 20px;
}

.port__item .num {
    font-size: 2rem;
    font-family: var(--mainNum-font);
    color: #ffffff;
    font-weight: 800;

}

.port__item img {
    width: 300px;
    height: auto;
    margin-top: 2rem;
    margin: 0 auto;
    display: block;

}

.port__item .title {
    font-size: 1.5rem;
    text-align: center;
    font-family: var(--mainKor-font);
    margin-top: 1.5rem;
    margin-bottom: -1rem;
    border-bottom: 2px solid black;
    color: var(--black300);

}

.port__item .desc {
    font-size: 1rem;
    font-family: var(--mainKor-font);
    margin-top: 1.4rem;
    display: inline-block;
    padding: 10px;
}

.port__item button {
    color: var(--black300);
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    background-color: #ffffff;
    width: 450px;
    margin: 1rem 1rem 1rem 1.5rem;
}

.port__item button:hover {
    background-color: #0056b3;
}

.port__item.title h3 {
    /* text-align: center; */
}


.port__item.p1 {
    background-color: #eee;
}


.port__item.p2 {
    background-color: #eee;
}

.port__item.p3 {
    background-color: #eee;
}

.port__item.p4 {
    background-color: #eee;
}

.port__item.p5 {
    background-color: #eee;
}

.port__item.p6 {
    background-color: #eee;
}

.port__item.p7 {
    background-color: #eee;
}

.port__item.p8 {
    background-color: #eee;
}

.port__item.p9 {
    background-color: #eee;
}

.port__item.p10 {
    background-color: #eee;
}
</style>