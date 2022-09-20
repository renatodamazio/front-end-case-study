<template>
    <div class="container">
        <div class="info">                
            <a href="https://www.backpackertrail.de/?utm_source=wapp&amp;utm_medium=referral&amp;utm_campaign=app_footer" target="_blank">
                <span>www.backpackertrail.de</span>
            </a>
        </div>
        
        <div class="copyright">
            <p>
                <a href="https://backpackertrail.atlassian.net/servicedesk/customer/portal/1/article/93716481?utm_source=wapp&amp;utm_medium=referral&amp;utm_campaign=app_data_footer" target="_blank">
                    Datenschutzerklärung
                </a>
                &nbsp;
                <a href="https://www.backpackertrail.de/impressum/?utm_source=app&amp;utm_medium=referral&amp;utm_campaign=wapp_imp" target="_blank">
                    Impressum
                </a>
            </p>
        </div>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'TheFooter'
    }
</script>

<style scoped lang="scss">
    .container {
        align-items: center;
        background: var(--ui-color-text);
        border-radius: 1.4rem 1.4rem 0 0;
        display: flex;
        height: 100%;
        justify-content: space-between;
        padding: 0 3rem;
        width: 100%;
        & > * {
            width: 50%;
            a {
                color: #fff;
                font-size: .75rem;
                text-decoration: none;
                &:hover {
                    color: var(--ui-color-primary);
                }
            }
        }
        .info {
            text-align: left;
        }
        .copyright {
            text-align: right;
        }
    }

    @media all and (max-width: 477px) {
        .container {
            justify-content: center;
            flex-direction: column;
            padding: 0 1.5rem;
            & > * {
                width: 100%;
            }
            .info {
                text-align: center;
            }
            .copyright {
                text-align: center;
            }
        }
    }
</style>