<template>
    <section id="intro">
        <div class="intro__inner">
            <h1 class="intro__title">
                JS developer portfolio
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
            <div class="intro__text">
                <div class="text">
                    <div>talent is</div>
                    <div>found at the end of the</div>
                    <div>effort</div>
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
}

.intro__inner {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    padding: 1vw;
}

.intro__title {
    font-size: 9vw;
    text-transform: uppercase;
    font-weight: 100;
    font-style: ExtraLight;
    font-family: 'Oswald', sans-serif;
    /* font-family: 'Montserrat', sans-serif; */
    line-height: 0.81;
    letter-spacing: -0.3vw;
    margin-bottom: 30px;
}

.intro__lines {
    display: block;
    width: 100%;

}

.intro__lines .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: var(--subBg300);
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
    height: 6px;
}

.intro__lines .line:nth-child(7) {
    height: 7px;
}

.intro__lines.bottom .line:nth-child(7) {
    height: 7px;
}

.intro__lines.bottom .line:nth-child(6) {
    height: 6px;
}

.intro__lines.bottom .line:nth-child(5) {
    height: 5px;
}

.intro__lines.bottom .line:nth-child(4) {
    height: 4px;
}

.intro__lines.bottom .line:nth-child(3) {
    height: 3px;
}

.intro__lines.bottom .line:nth-child(2) {
    height: 2px;
}

.intro__lines.bottom .line:nth-child(1) {
    height: 1px;
}

.intro__lines.bottom {
    display: none;
}

.intro__text {
    background-color: var(--subBg300);
    /* height: 37vh; */
    padding: 7vw 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--mainBg-color);
    text-align: center;
    position: relative;
    z-index: 1;
    cursor: pointer;
    transition: all 1.3s;
}

.intro__text:hover {
    background-color: #fff;
}

.intro__text:hover .text {
    opacity: 0;
}

.intro__text:hover .img {}

.intro__text .text {
    font-size: 3vw;
    line-height: 1.2;
    text-transform: uppercase;
    font-weight: 900;
    font-family: var(--maniMont);
    text-underline-position: under;
    text-decoration: underline;
    letter-spacing: -0.1vw;
    transition: all 0.6s;
}

.intro__text .img {
    position: absolute;
    /* left: 50%;
    top: 50%; */
    transform: translate(-50% -50%);
    width: 15vw;
    height: 15vw;
    /* padding: 10vw 0; */
    background-image: url(../assets/img/image1.jpg);
    background-size: cover;
    background-position: center center;
    border-radius: 50%;
    z-index: -1;
    /* opacity: 1; */
    /* filter: grayscale(100%); */
}

.intro__text .img::after {
    content: '';
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
}

@media (max-width: 800px) {
    .intro__inner {
        align-items: center;
        justify-content: center;
    }

    .intro__lines.bottom {
        display: block;
    }

    .intro__title {
        display: none;
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
        opacity: 0.3;
    }
}
</style>