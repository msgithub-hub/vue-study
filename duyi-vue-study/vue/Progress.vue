<template>
    <div class="progress" style="display: flex;">
        <div class="progress-bar">
            <div class="progress-bar-outer" :style="{height:strokeWith +'px'}">
                <div class="progress-bar-inner" :style="{width:percentage +'%',backgroundColor:stroke}"></div>
            </div>
        </div>
        <div class="progress-text" :style="{fontSize:progressTextFontSize+'px'}">100%</div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                name: '哈哈哈'
            }
        },
        props: {
            strokeWith: {
                type: Number,
                default: 6,
            },
            percentage: {
                type: Number,
                required: true,
                default: 0,
                validator(value) {
                    return value >= 0 && value <= 100
                }
            },
            stroke() {
                let color;
                switch (this.status) {
                    case 'success':
                        color = '#13ce66';
                        break;
                    case 'exeption':
                        color = '#ff4949';
                        break;
                    default:
                        color = '#20a0ff';
                        // break;
                }
                return color;
            },
        },
        computed: {
            progressTextFontSize() {
                return 12 + this.strokeWith * 0.4
            }
        }
    }
</script>

<style scoped>
    .progress-bar {
        width: 90%;
        /*line-height: 2rem;*/
        /*margin-left: 5%;*/
        /*background-color: yellow;*/
    }

    .progress-bar-outer {
        background-color: #cccccc;
        border-radius: 6px;

    }

    .progress-bar-inner {
        width: 50%;
        height: 100%;
        border-radius: 6px;
        background-color: red;
        transition: width 0.5s ease;
    }

    .progress-text {
        margin-top: -8px;
        margin-left: 2px;
    }
</style>