<script lang="ts">
    let { iconClass, headerText, bodyText, isLeft } = $props();
</script>

<div class="white-card-wrapper col-12 col-lg-6 p-0" class:left={isLeft}>
    <div class="white-card">
        <div class="white-card-icon">
            <span class="icon {iconClass}"></span>
        </div>
        <div class="white-card-header">
            <h3>{headerText}</h3>
        </div>
        <div class="white-card-body">
            <p class="text-muted mb-0">{bodyText}</p>
        </div>
    </div>
</div>

<style>
    .white-card-wrapper {
        display: flex;

        .white-card {
            background-color: #fff;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: left;
            margin: 25px;
            max-width: 400px;

            .white-card-header {
                color: #000;
                font-weight: 500;
                margin-top: 0.5rem;

                h3 {
                    margin-bottom: 0.25rem;
                }
            }

            .white-card-icon {
                .icon {
                    width: 50px;
                    height: 50px;
                    background-size: 50px;
                    margin-left: -5px;
                    margin-top: -5px;
                }
            }
        }
    }

    @media (min-width: 768px) {
        .white-card-wrapper.left {
            justify-content: flex-end;
        }
    }
</style>