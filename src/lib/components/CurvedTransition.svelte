<div class="curved-transition">
    <svg viewBox="0 0 1440 150" preserveAspectRatio="none" class="curve-svg">
        <path
            d="M0,0 C480,100 960,100 1440,0 L1440,150 L0,150 Z"
            fill="#000"
        />
    </svg>
</div>

<style>
    .curved-transition {
        position: relative;
        width: 100%;
        height: 150px;
        background-color: #fff;
        margin: 0;
        overflow: hidden;
    }

    .curve-svg {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: block;
    }

    @media (max-width: 767px) {
        .curved-transition {
            height: 100px;
        }
    }

    @media (max-width: 480px) {
        .curved-transition {
            height: 70px;
        }
    }
</style>
