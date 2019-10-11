<template>
    <div id="main">
        <div class="attach">
            <div class="slider_case">
                <v-slider v-bind="options">
                   <img src="../img/pic1.jpg">
                    <img src="../img/pic2.jpg">
                </v-slider>
            </div>

            <pre>{{options}}</pre>
        </div>
    </div>
</template>

<script>
    import slider from './slider.vue'

    export default {
        name: 'main',
        
        data () {
            return {
                options: {
                    items: 2,
                    margin: 5,
                    nav: true,
                    dots: false,
                    loop: true,
                    speed: 250,
                    timing: 'ease-in-out',
                    offset: 1,
                    sibling: false,
                    responsive : {
                        0: {
                            items: 1,
                            nav: true
                        },
                        768: {
                            items: 1
                        },
                        999: {
                            items: 1
                        }
                    }
                }
            }
        },

        components: {
            'v-slider': slider,
        }
    }
</script>

<style>
    * {
        margin: 0;
        padding: 0;
        border:0;
        max-height: 99999999px;
        -webkit-font-smoothing: antialiased;


        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
    }

    #main {
        font-family: "Roboto", Arial, sans-serif;
        font-size: 14px;
    }

    .attach {
        width: 100%;
        max-width: 1000px;
        min-width: 480px;
        padding: 50px 15px;
        margin: 0 auto;
        position: relative;
    }

    .slider_case {
        margin-bottom: 40px;
    }

    .item {
        background: #00800b;
        text-align: center;
        padding: 100px 0;
        color: #fff;
        font-size: 26px;
        font-style: italic;
        font-weight: 300;
    }

    .item.active {
        background: #ff3f4d;
    }
    
    .item.super {
        background: #04a0c5;
    }

    pre {
        border:1px solid #eee;
        padding:15px;
        background: #f5f5f5;
    }



</style>