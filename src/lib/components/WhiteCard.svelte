<script lang="ts">
    let { iconClass, headerText, bodyText, isLeft } = $props();
</script>

<div class="white-card-wrapper" class:left={isLeft}>
    <div class="white-card">
        <div class="white-card-icon">
            <span class="icon {iconClass}"></span>
        </div>
        <h3>{headerText}</h3>
        <p>{bodyText}</p>
    </div>
</div>

<style>
    .white-card-wrapper {
        display: flex;
    }

    .white-card {
        background-color: #fff;
        padding: 1.5rem 1.75rem;
        border-radius: 10px;
        text-align: left;
        margin: 10px;
        max-width: 340px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
        border: 1px solid rgba(0, 0, 0, 0.06);
        transition: transform 0.2s ease, box-shadow 0.2s ease;

        &:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
        }

        h3 {
            color: #000;
            font-weight: 600;
            margin: 0.75rem 0 0.5rem;
            font-size: 1.1rem;
            line-height: 1.3;
            letter-spacing: -0.01em;
        }

        p {
            font-size: 0.85rem;
            line-height: 1.5;
            color: #666;
            margin: 0;
        }

        .white-card-icon .icon {
            width: 36px;
            height: 36px;
            background-size: 36px;
            opacity: 0.7;
        }
    }

    @media (min-width: 768px) {
        .white-card-wrapper.left {
            justify-content: flex-end;
        }
    }
</style>
