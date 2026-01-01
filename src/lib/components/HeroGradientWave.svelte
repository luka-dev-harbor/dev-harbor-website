<div class="hero-wave-container">
    <svg viewBox="0 0 1440 200" preserveAspectRatio="none" class="hero-wave-svg">
        <!-- Layer 1: Light gray wave -->
        <path
            d="M0,80 Q360,140 720,80 T1440,80 L1440,200 L0,200 Z"
            fill="#e8e8e8"
        />
        <!-- Layer 2: Medium-light gray wave -->
        <path
            d="M0,100 Q360,160 720,100 T1440,100 L1440,200 L0,200 Z"
            fill="#c0c0c0"
        />
        <!-- Layer 3: Medium gray wave -->
        <path
            d="M0,120 Q360,175 720,120 T1440,120 L1440,200 L0,200 Z"
            fill="#888888"
        />
        <!-- Layer 4: Dark gray wave -->
        <path
            d="M0,145 Q360,190 720,145 T1440,145 L1440,200 L0,200 Z"
            fill="#444444"
        />
        <!-- Layer 5: Black wave -->
        <path
            d="M0,170 Q360,200 720,170 T1440,170 L1440,200 L0,200 Z"
            fill="#000000"
        />
    </svg>
</div>

<style>
    .hero-wave-container {
        position: relative;
        width: 100%;
        height: 180px;
        background-color: #fff;
        margin-top: -1px;
        overflow: hidden;
    }

    .hero-wave-svg {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: block;
    }

    @media (max-width: 767px) {
        .hero-wave-container {
            height: 120px;
        }
    }

    @media (max-width: 480px) {
        .hero-wave-container {
            height: 90px;
        }
    }
</style>
