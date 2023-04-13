<template>
    <div class="footer">
        <div class="footer-top">
            <div class="container">
                <div class="about padding-20">
                    <h4 class="title">ABOUT THE BLOG</h4>
                    <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Odit voluptatum neque molestiae maiores
                        iusto animi sequi quia doloremque blanditiis repudiandae laborum.
                    </span>
                    <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Odit voluptatum neque molestiae maiores
                        iusto animi sequi quia doloremque blanditiis repudiandae laborum.
                    </span>
                    <h5>VIEW MORE <i class="fa-solid fa-chevron-right"></i> </h5>

                </div>
                <div class="recent-posts padding-20">
                    <h4 class="title">RECENT POSTS</h4>
                    <div class="box">
                        <div class="image">
                            <img src="../assets/our-office-4-square.jpg" alt="office1">
                        </div>
                        <div class="text">
                            <h5>Lorem ipsum dolor sit, consectetur adipisicing elit.</h5>
                            <span class="date"> 12:53 AM Dec 19th</span>
                        </div>
                    </div>
                    <div class="box">
                        <div class="image">
                            <img src="../assets/our-office-5-square.jpg" alt="office2">
                        </div>
                        <div class="text">
                            <h5>Lorem ipsum dolor sit, consectetur adipisicing elit.</h5>
                            <span class="date"> 12:53 AM Dec 19th</span>
                        </div>
                    </div>
                </div>
                <div class="recent-comments padding-20">
                    <h4 class="title">RECENT COMMENTS</h4>
                    <div class="box" v-for="(element, i) in 2" :key="i">
                        <i class="fa-solid fa-chevron-right"></i>
                        <span class="user">John Doe</span>
                        <span class="type">Commented on </span>
                        <span class="comment">lorem ipsum dolor sit amet.</span>
                        <span class="date">12:55 AM Dec 19th</span>
                    </div>
                </div>
                <div class="categories padding-20">
                    <h4 class="title">CATEGORIES</h4>
                    <div class="box">
                        <div class="button-black">
                            <span v-for="(element, i ) in categories">{{ element }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">

            </div>

        </div>

    </div>
</template>
<script>
export default {
    nome: 'AppFooter',
    data() {
        return {
            categories: ["GADGETS", "PHOTOGRAPHY", "LIFESTYLE", "FASHION", "RECIPES", "TRAVEL", "BUSINESS", "ARCHITECTURE", "REVIEWS", "SPORTS", "VIDEOS", "TECHNOLOGY", "DESIGN"]
        }
    }
}
</script>
<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';
@use '../styles/general.scss';

.footer {
    .footer-top {
        height: 300px;
        background-color: $color-background-6;

        .container {
            @include mixins.center;
            padding: 50px 0px;
            display: flex;
            justify-content: space-between;

            .title {
                color: $color-white;
                font-size: 12px;
                font-weight: bolder;
                padding-bottom: 20px;
            }

            .date {
                color: $color-text-3;
                font-size: 10px;
                display: block;
                padding-top: 10px;
            }

            .about {
                width: 25%;

                h5 {
                    color: $color-white;
                    font-size: 9px;
                    font-weight: bolder;

                    i {
                        font-size: 8px;
                    }
                }

                span {
                    color: $color-text-3;
                    font-size: 10px;
                    display: block;
                    padding: 10px 0px;
                }
            }

            .recent-posts {
                width: 25%;

                .box {
                    display: flex;

                    .image {
                        img {
                            width: 60px;
                            border-radius: 50%;
                        }
                    }

                    .text {
                        padding-left: 20px;

                        h5 {
                            color: $color-text-1;
                        }
                    }
                }
            }

            .recent-comments {
                width: 25%;

                .box {
                    i {
                        color: $color-primary;
                        font-size: 8px;
                        padding-right: 5px;
                    }

                    .user {
                        color: $color-text-1;
                        font-size: 13px;
                    }

                    .type {
                        color: $color-text-3;
                        font-size: 12px;
                        padding: 0px 5px;
                    }

                    .comment {
                        color: $color-primary;
                        font-size: 13px;
                    }
                }
            }

            .categories {
                width: 25%;

                .box {
                    .button-black {
                        display: flex;
                        flex-wrap: wrap;
                    }
                }
            }
        }
    }

    .footer-bottom {
        height: 100px;
        background-color: $color-background-8;

        .container {
            @include mixins.center;
        }
    }
}
</style>