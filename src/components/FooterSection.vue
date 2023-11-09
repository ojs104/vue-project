<script setup>
import { footerText } from "@/constants/index"
</script>

<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>websloper</div>
                <div>@gmail.com</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li v-for="(foot, key) in footerText" v-bind:key="key">
                            <a href="#">{{ foot.link }} {{ foot.title }}</a>
                            <em>{{ foot.desc }}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 websloper<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>
<style lang="scss">
#footer {
    background-color: var(--mainSub-220707);
    color: #fff;
    padding: 20px;
    width: 100%;

}

.footer__inner {
    margin: auto;

}

.footer__container {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
}

.footer__text {
    /* display: flex;    */
    width: 33.3333%;
}

.footer__info {
    /* display: flex; */
    width: 33.3333%;
}

.footer__info .left {
    width: 50%;
}

.footer__info .left .title {

    margin-bottom: 40px;
    padding-top: 10px;
}

.footer__info .right {
    width: 33.3333%;
    /* display: inline-block; */
}

.footer__info .right h3 {
    font-size: 1rem;
    display: inline-block;
    margin-bottom: 40px;
    padding-top: 10px;
    color: var(--mainSub-color);
}

.footer__info .right {

    text-transform: uppercase;
    font-size: 1rem;
    margin-bottom: 20px;
    color: var(--mainSub-color);
}

@media (max-width: 800px) {
    .footer__info {
        flex-direction: column;
    }

    .footer__info .left {
        width: 100%;
    }

    .footer__info .left .desc {
        margin-bottom: 40px;
    }

    .footer__info .right {
        width: 100%;
    }
}
</style>