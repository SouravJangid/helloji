<template>
    <div class="dposition">
        <div class="txt">
            <div class="glowing-cube">
                <div class="top">❤️</div>
                <div>
                    <span style="--i:0;"></span>
                    <span style="--i:1;"></span>
                    <span style="--i:2;"></span>
                    <span style="--i:3;"></span>
                </div>
            </div>
        </div>
        <div class="video">
            <iframe width="560" id="player" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1&loop=1&playlist=YX-0CQVHmrs" title="YouTube video player" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
    </div>
</template>




<style scoped>
.dposition {
    display: grid;
    grid-template-columns: 60% 20%;
    gap: 5%;
    text-align: left;
    padding: 5% 20% 5% 20%;
}

/* .video {} */

.glowing-cube {
    position: relative;
    width: 150px;
    height: 150px;
    transform-style: preserve-3d;
    animation: cube-rotate 4s linear infinite;
}

@keyframes cube-rotate {
    0% {
        transform: rotatex(-30deg) rotatey(0deg);
    }

    100% {
        transform: rotatex(-30deg) rotatey(360deg);
    }
}

.glowing-cube div {
    position: absolute;
    inset: 0;
    transform-style: preserve-3d;
}

.glowing-cube div span {
    position: absolute;
    inset: 0;
    background: linear-gradient(#151515, #3aff5e);
    transform: rotatey(calc(90deg * var(--i))) translatez(calc(150px / 2));
}

.glowing-cube .top {
    position: absolute;
    inset: 0;
    background: #222;
    transform: rotatex(90deg) translatez(calc(150px / 2));
    display: flex;
    justify-content: center;
    align-items: center;
    color: var(--top-font-color);
    font-size: 7rem;
}

.glowing-cube .top::before {
    content: '';
    position: absolute;
    background: #3aff5e;
    inset: 0;
    transform: translatez(calc(0px - calc(150px + 100px)));
    filter: blur(30px);
    box-shadow: 0 0 120px rgba(58, 134, 255, 0.2),
        0 0 200px rgba(245, 58, 255, 0.4),
        0 0 300px #00ff2f,
        0 0 400px #51fd71,
        0 0 500px #3aff5e;
}

@media screen and (max-width:1024px) {  
.dposition {
    padding: 5% 0 5% 15%;
}
.video{
    margin-left: -150%;
}
}

@media screen and (max-width:768px) {  
.dposition {
    grid-template-columns: none;
    grid-template-rows:auto;
    text-align:center;
    padding: 5% 0 5% 0;
}
.txt{
    padding-left: 35%;
}
.video{
    margin: 25% 5% 0 0;
}
}

</style>
