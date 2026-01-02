<div class="wave-container">
    <svg viewBox="0 0 1440 150" preserveAspectRatio="none" class="wave-svg">
        <path d="M0,20 C200,40 350,15 720,10 C1100,5 1250,50 1440,80 L1440,150 L0,150 Z" fill="#bbb"/>
        <path d="M0,40 C200,60 350,35 720,30 C1100,25 1250,70 1440,100 L1440,150 L0,150 Z" fill="#777"/>
        <path d="M0,60 C200,80 350,55 720,50 C1100,45 1250,90 1440,120 L1440,150 L0,150 Z" fill="#444"/>
        <path d="M0,85 C200,105 350,80 720,75 C1100,70 1250,115 1440,145 L1440,150 L0,150 Z" fill="#000"/>
    </svg>
</div>

<style>
    .wave-container {
        width: 100%;
        height: 150px;
        background-color: #fff;
        margin-top: -30px;
    }

    .wave-svg {
        width: 100%;
        height: 100%;
        display: block;
    }

    @media (max-width: 767px) {
        .wave-container {
            height: 100px;
        }
    }

    @media (max-width: 480px) {
        .wave-container {
            height: 70px;
        }
    }
</style>
