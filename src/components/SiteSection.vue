<script setup>
import { siteText } from "@/constants/index"
</script>

<template>
    <section id="site">
        <div class="site__inner">
            <div class="site__title">
                Site Coding <em>나의 작업물</em>
            </div>
            <div class="site__wrap">
                <div :class="['site__item', 's' + (key + 1)]" v-for="(site, key) in siteText" :key="key">
                    <span class="num">{{ key + 1 }}.</span>
                    <div class="text">
                        <div>{{ site.text[0] }}</div>
                        <div>{{ site.text[1] }}</div>
                        <div>{{ site.text[2] }}</div>
                    </div>
                    <h3 class="title">{{ site.title }}</h3>
                    <div class="btn">
                        <a href="#">{{ site.code }}</a>
                        <a href="#">{{ site.view }}</a>
                    </div>
                    <div class="info">
                        <span>{{ site.info[0] }}</span>
                        <span>{{ site.info[1] }}</span>
                        <span>{{ site.info[2] }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- //site -->
</template>
<style>
.site__inner {
    padding: 16px;

}

.site__title {
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

.site__title em {
    font-size: 1.25rem;
    font-weight: 400;
    line-height: 2;
}

.site__item {
    position: sticky;
    left: 0;
    height: 70vh;

    display: flex;
    align-items: center;

    justify-content: center;

    flex-direction: column;
}

.site__item.s1 {
    background-color: var(--subBg100);
    top: 180px;
}

.site__item.s2 {
    background-color: var(--subBg200);
    top: 200px;
}

.site__item.s3 {
    background-color: var(--subBg300);
    top: 220px;
}

.site__item.s4 {
    background-color: var(--subBg400);
    top: 240px;
}


.site__item .num {
    font-size: 5vw;
    line-height: 1;
    font-weight: 900;
    font-family: var(--mainNum-font);
    position: absolute;
    left: 1vw;
    top: 1vw;
}

.site__item .text {
    text-align: center;
    margin-bottom: 1rem;
}

.site__item .text>div {
    font-size: 3vw;
    line-height: 1;
    font-weight: 900;
    text-transform: uppercase;
    text-decoration: underline;
    font-family: var(--mainPop-font);
}

.site__item .title {
    font-family: var(--mainKor-font);
    margin-bottom: 1rem;
}

.site__item .btn a {
    text-decoration: underline;
    text-transform: uppercase;
    color: var(--black200);
    font-size: 1rem;
    transition: all 0.3s;
}

.site__item .btn a:hover {
    color: var(--black);
}

.site__item .info {
    position: absolute;
    left: 0;
    bottom: 3%;
    width: 98%;
    margin-left: 1%;
    border-top: 1px solid var(--black);
    border-bottom: 1px solid var(--black);
    display: flex;
    justify-content: space-between;
}


.site__item .info span {
    font-family: var(--mainKor-font);
    font-size: 12px;
    padding: 3px 0;
    text-transform: uppercase;
}

@media (max-width: 800px) {
    .site__title {
        width: 100%;
        margin-bottom: 10vw;
        font-size: 30px;
        height: auto;
        top: 68px;
        z-index: 1000;
        background-color: var(--mainBg-color);
    }

    .site__item.s1 {
        top: 140px;
    }

    .site__item.s2 {
        top: 160px;
    }

    .site__item.s3 {
        top: 180px;
    }

    .site__item.s4 {
        top: 200px;
    }

    .site__item .num {
        font-size: 80px;
        left: 20px;
        top: 20px;
    }

    .site__item .text>div {
        font-size: 26px;
    }

    .site__item .info {
        flex-direction: column;
        width: 90%;
        margin-left: 5%;
        padding: 5px 0;
    }
}
</style>