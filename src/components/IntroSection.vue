<script setup>
import { introText } from "@/constants/index"

</script>

<template>
    <section id="intro">
        <div class="intro__inner">
            <h1 class="intro__title" v-for="(intro, key) in introText" v-bind:key="key">
                {{ intro.title }}
            </h1>

            <div class="intro__lines" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>

            <div class="intro__text" v-for="(intro, key) in introText" v-bind:key="key">
                <div class="text">
                    {{ intro.text[0] }}
                    {{ intro.text[1] }}
                    {{ intro.text[2] }}
                </div>
                <div class="img">

                </div>
            </div>

            <div class="intro__lines bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
        </div>
    </section>
</template>
<style lang="scss">
#intro {
    height: 100vh;
    margin-top: 50px;
}


.intro__inner {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    padding: 1vw;
}

.intro__title {
    font-size: 8.7vw;
    font-weight: 100;
    text-transform: uppercase;
    font-family: "Playfair Display";
    color: #ffffff;
    line-height: 0.81;
    letter-spacing: -0.3vw;

}



.intro__lines {
    display: block;
    width: 100%;
    padding: 1vw;
}

.intro__lines .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: #ffffff;
    margin-bottom: 0.5vw;
}

.intro__lines .line:nth-child(1) {
    height: 1px;
}

.intro__lines .line:nth-child(2) {
    height: 2px;

}

.intro__lines .line:nth-child(3) {
    height: 3px;
}

.intro__lines .line:nth-child(4) {
    height: 4px;
}

.intro__lines .line:nth-child(5) {
    height: 5px;
}

.intro__lines .line:nth-child(6) {
    height: 5px;
}

.intro__lines .line:nth-child(7) {
    height: 7px;
}

.intro__lines.bottom {
    display: none;
}


/* bottom */
.intro__lines.bottom .line:nth-child(1) {
    height: 7px;
}

.intro__lines.bottom .line:nth-child(2) {
    height: 6px;

}

.intro__lines.bottom .line:nth-child(3) {
    height: 5px;
}

.intro__lines.bottom .line:nth-child(4) {
    height: 4px;
}

.intro__lines.bottom .line:nth-child(5) {
    height: 3px;
}

.intro__lines.bottom .line:nth-child(6) {
    height: 2px;
}

.intro__lines.bottom .line:nth-child(7) {
    height: 1px;
}




.intro__text {
    background-color: #ccc;
    width: 98%;
    /* height: 37vh; */
    padding: 10vw 0;
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
    position: relative;
    cursor: pointer;
    transition: all 1.3s;
}

.intro__text .text {
    font-family: "Playfair Display";
    font-size: 3.4vw;
    font-weight: 700;
    line-height: 1;
    text-transform: uppercase;
    letter-spacing: 0.1vw;
    margin-top: 6vw;
    z-index: 1000;
    color: #ffffff;
    text-align: center;
    margin-top: 10px;
}

.intro__text .img {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    width: 15vw;
    height: 15vw;
    /* padding: 10vw 0; */
    background-image: url(../assets/img/intro.png);
    background-size: cover;
    background-position: center center;
    border-radius: 50%;
    filter: grayscale(100%);
}

.intro__text .img::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100px;
    transform: all 0.5s;
}

.intro__text:hover {
    background-color: var(--mainBg-color);
}

.intro__text:hover .text {
    opacity: 0;
}

.intro__text:hover .img::after {
    opacity: 0;
}


@media (max-width: 800px) {
    .intro__title {
        display: none;
    }

    .intro__inner {
        justify-content: center;
        align-items: center;
    }

    .intro__lines.bottom {
        display: block;
    }

    .intro__text .text {
        font-size: 30px;
    }

    .intro__text .text>div:nth-child(2) {
        filter: brightness(0.5);
    }

    .intro__text .img {
        width: 300px;
        height: 300px;
    }

    .intro__text .img::after {
        opacity: 0.3s;
    }
}
</style>