<script>
export default {
    name: 'TieSVG',
    methods: {
        playAgain() {
            this.$emit('play-again')
        }
    }
}
</script>

<template>
    <div class="message">
        <div class="player-score-container">
            <svg width="33" height="34" viewBox="0 0 33 34" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M13.1484 34V27.2715H21.5527V0.306641H26.0469L32.7754 7.03516V27.2715L26.0469 34H13.1484ZM6.95312 34L0.199219 27.2715V7.03516L6.95312 0.306641H19.8262V7.03516H11.4219V34H6.95312Z"
                    fill="white" />
            </svg>
        </div>
        <div @click="playAgain" class="play-again-btn">
            <svg width="389" height="79" viewBox="0 0 389 79" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="388" height="79" transform="translate(0.5)" fill="black" />
                <path
                d="M58.6786 20.1818V58H50.1104L36.4457 38.1307H36.2241V58H25.957V20.1818H34.6729L48.1161 39.9773H48.4116V20.1818H58.6786ZM63.5352 58V20.1818H90.7908V28.4545H73.8022V34.9545H89.3874V43.2273H73.8022V49.7273H90.717V58H63.5352ZM105.485 58L94.3317 20.1818H105.781L110.951 43.4489H111.246L117.377 20.1818H126.388L132.519 43.5227H132.815L137.985 20.1818H149.434L138.281 58H128.457L122.031 36.875H121.735L115.309 58H105.485ZM163.117 58V20.1818H179.515C182.396 20.1818 184.815 20.5696 186.772 21.3452C188.742 22.1207 190.225 23.2164 191.222 24.6321C192.232 26.0478 192.737 27.7159 192.737 29.6364C192.737 31.0275 192.429 32.2955 191.813 33.4403C191.21 34.5852 190.361 35.5455 189.265 36.321C188.169 37.0843 186.889 37.6136 185.424 37.9091V38.2784C187.049 38.34 188.526 38.7524 189.856 39.5156C191.185 40.2666 192.244 41.3068 193.032 42.6364C193.82 43.9536 194.214 45.5047 194.214 47.2898C194.214 49.358 193.672 51.1984 192.589 52.8111C191.518 54.4238 189.991 55.6918 188.009 56.6151C186.027 57.5384 183.664 58 180.918 58H163.117ZM173.384 49.8011H178.185C179.909 49.8011 181.201 49.4811 182.063 48.8409C182.925 48.1884 183.356 47.2282 183.356 45.9602C183.356 45.0739 183.153 44.3229 182.746 43.7074C182.34 43.0919 181.762 42.6241 181.011 42.304C180.272 41.9839 179.379 41.8239 178.333 41.8239H173.384V49.8011ZM173.384 35.4716H177.594C178.493 35.4716 179.287 35.33 179.977 35.0469C180.666 34.7637 181.201 34.3575 181.583 33.8281C181.977 33.2865 182.174 32.6278 182.174 31.8523C182.174 30.6828 181.755 29.7902 180.918 29.1747C180.081 28.5469 179.022 28.233 177.742 28.233H173.384V35.4716ZM207.675 58H196.596L209.079 20.1818H223.113L235.596 58H224.516L216.244 30.5966H215.948L207.675 58ZM205.607 43.0795H226.437V50.7614H205.607V43.0795ZM233.431 28.4545V20.1818H266.3V28.4545H254.925V58H244.806V28.4545H233.431ZM269.13 28.4545V20.1818H301.999V28.4545H290.624V58H280.505V28.4545H269.13ZM305.863 58V20.1818H316.13V49.7273H331.42V58H305.863ZM335.57 58V20.1818H362.826V28.4545H345.837V34.9545H361.423V43.2273H345.837V49.7273H362.752V58H335.57Z"
                fill="white" />
            </svg>
        </div>
        <div class="computer-score-container">
            <svg width="33" height="34" viewBox="0 0 33 34" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M13.1484 34V27.2715H21.5527V0.306641H26.0469L32.7754 7.03516V27.2715L26.0469 34H13.1484ZM6.95312 34L0.199219 27.2715V7.03516L6.95312 0.306641H19.8262V7.03516H11.4219V34H6.95312Z"
                    fill="white" />
            </svg>
        </div>
    </div>
</template>

<style>
.play-again-btn {
    cursor: pointer;
}

@media screen and (max-width: 767px) {
    
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .message {
        width: 100%;
        height: 100px;
    }

    .player-score-container {
        display: flex;
        justify-content: center;
        width: 30px;
        position: absolute;
        right: 300px;
    }

    .computer-score-container {
        display: flex;
        justify-content: center;
        width: 30px;
        position: absolute;
        left: 300px;
    }

    .play-again-btn {
        background-color: black;
        border-radius: 4px;
        width: 160px;
        height: fit-content;
        display: flex;
        justify-content: center;
    }

    .play-again-btn svg {
        width: 150px;
    }

    .computer-score-container svg {
        width: 50px;
    }
}
</style>
