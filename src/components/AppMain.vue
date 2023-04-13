<script>
import AppPreview from './AppPreview.vue';
export default {
    nome: 'AppMain',
    components: {
        AppPreview,
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    },
    data() {
        return {
            preview: [
                {
                    img: 'blog-46.jpg',
                    type: 'PHOTOGRAPHY',
                    title: 'How To Take Better Concert Pictures in 30 Seconds'
                },
                {
                    img: 'blog-47.jpg',
                    type: 'GADGETS',
                    title: 'Gadgets That Make Your Smartphone Even Smarter'
                },
                {
                    img: 'blog-48.jpg',
                    type: 'TRAVEL',
                    title: '20 Top-Rated Tourist Attractions in Manhattan'
                },
                {
                    img: 'blog-49.jpg',
                    type: 'LIFESTYLE',
                    title: 'The Best Way to Ride a Motorcycle'
                },
                {
                    img: 'blog-50.jpg',
                    type: 'TRAVEL',
                    title: '5 Fun Things to Do at the Beach'
                },
                {
                    img: 'blog-51.jpg',
                    type: 'RECIPES',
                    title: 'Amazingly Fresh Fruit And Herb Drinks For Summer'
                }
            ],
            popularPosts: [
                {
                    img: 'blog-55.jpg',
                    title: 'Simple ways to have a pretty face',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-56.jpg',
                    title: 'Ranking the greatest players in basketball',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-57.jpg',
                    title: '4 Ways to Look Cool in Glasses',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-58.jpg',
                    title: 'Top Camper Trailer Towing Tips',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-59.jpg',
                    title: '5 Lovely Walks in New York',
                    date: 'january 12, 2019'
                },
            ],
            recentPosts: [
                {
                    img: 'blog-65.jpg',
                    title: 'Main Reasons To Stop Texting And Driving',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-66 (1).jpg',
                    title: 'Tips to Help You Quickly Prepare your Lunch',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-67.jpg',
                    title: 'Why should i buy a smartwatch?',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-68.jpg',
                    title: 'The best augmented reality smartglasses',
                    date: 'january 12, 2019'
                },
                {
                    img: 'blog-69.jpg',
                    title: '12 Healthiest Foods to Eat for Breakfast',
                    date: 'january 12, 2019'
                },
            ],
            item: [
                {
                    image: 'blog-54.jpg',
                    day: '12',
                    month: 'JAN',
                    title: 'How to Make Friends as a Grown-Up',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi, officia ratione fugiat officiis voluptate, dolores voluptatum omnis eum eveniet ad est eaque praesentiumminus maxime. Quis autem quaerat repellendus voluptatem?[...]",
                    author: 'John Doe',
                    type: 'Lifestyle, Travel',
                    comments: '12 Comments'
                },
                {
                    image: 'blog-55 (1).jpg',
                    day: '12',
                    month: 'JAN',
                    title: 'Simple ways to Have a Pretty Face',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi, officia ratione fugiat officiis voluptate, dolores voluptatum omnis eum eveniet ad est eaque praesentiumminus maxime. Quis autem quaerat repellendus voluptatem?[...]",
                    author: 'John Doe',
                    type: 'Lifestyle, Travel',
                    comments: '12 Comments'
                },
                {
                    image: 'blog-56 (1).jpg',
                    day: '12',
                    month: 'JAN',
                    title: 'Ranking the greatest players in basketball',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi, officia ratione fugiat officiis voluptate, dolores voluptatum omnis eum eveniet ad est eaque praesentiumminus maxime. Quis autem quaerat repellendus voluptatem?[...]",
                    author: 'John Doe',
                    type: 'Sport, Business',
                    comments: '12 Comments'
                },
                {
                    image: 'blog-58 (1).jpg',
                    day: '12',
                    month: 'JAN',
                    title: 'Top Camper Trailer Towing Tips',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi, officia ratione fugiat officiis voluptate, dolores voluptatum omnis eum eveniet ad est eaque praesentiumminus maxime. Quis autem quaerat repellendus voluptatem?[...]",
                    author: 'John Doe',
                    type: 'Travel, Lifestyle',
                    comments: '12 Comments'
                },
                {
                    image: null,
                    day: '8',
                    month: 'JAN',
                    title: 'Top Camper Trailer Towing Tips',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi, officia ratione fugiat officiis voluptate, dolores voluptatum omnis eum eveniet ad est eaque praesentiumminus maxime. Quis autem quaerat repellendus voluptatem?[...]",
                    author: 'John Doe',
                    type: 'Travel, Lifestyle',
                    comments: '12 Comments'
                },
            ],
            imageBlog: ['blog-13.jpg', 'blog-16.jpg', 'blog-20.jpg', 'blog-23.jpg', 'blog-29.jpg', 'blog-40.jpg'],
            instagram: ['29415304_166583630713703_1032667922171953152_n.jpg', '29415620_196477127626244_3250318472361541632_n.jpg', '29739607_2020680068220520_4509928046932787200_n.jpg', '30077195_2066750973610181_3733150062893596672_n.jpg', '30078414_1274410412703843_8290935809419247616_n.jpg', '30087804_253872848488989_8792603541668626432_n.jpg']
        }
    }
}
</script>
<template>
    <div class="main">

        <!-- PREVIEW -->
        <div class="preview">
            <div class="container">
                <AppPreview v-for="(element, i) in preview" :key="i" :images="element.img" :types="element.type"
                    :title="element.title" />
            </div>
        </div>

        <!-- POSTS -->
        <div class="posts">
            <div class="container-posts">

                <!-- POPULAR POSTS -->
                <div class="popular-posts w-100-3">
                    <h3>POPULAR POSTS</h3>
                    <div class="card-posts" v-for="(element, i) in popularPosts" :key="i">
                        <img :src="getImagePath(element.img)" :alt="element.img">
                        <div class="info">
                            <span>{{ element.title }}</span>
                            <span class="date">{{ element.date }}</span>
                        </div>
                    </div>
                </div>

                <!-- RECENT POSTS -->
                <div class="recent-posts w-100-3">
                    <h3>RECENT POSTS</h3>
                    <div class="card-posts" v-for="(element, i) in recentPosts" :key="i">
                        <img :src="getImagePath(element.img)" :alt="element.img">
                        <div class="info">
                            <span>{{ element.title }}</span>
                            <span class="date">{{ element.date }}</span>
                        </div>
                    </div>
                </div>

                <!-- FEATURED POSTS -->
                <div class="featured-posts w-100-3">
                    <h3>FEATURED POSTS</h3>
                    <AppPreview :images="'blog-66.jpg'" :types="'RECIPES'"
                        :title="'Tips to Help You Quickly Prepare your Lunch'" />
                    <div class="featured-author">
                        <h3>FEATURED AUTHOR</h3>
                        <div class="card-posts">
                            <img src="../assets/avatar.jpg" alt="img">
                            <div class="info">
                                <span>John Doe</span>
                                <span class="date">Lorem ipsum dolor</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!--CENTER  -->
        <div class="center">
            <div class="wrapper">
                <div class="item">
                    <div class="box" v-for="(element, i) in item" :key="i">
                        <div class="image">
                            <img :src="getImagePath(element.image)" alt="blog" v-show="element.image != null">
                            <img :src="getImagePath(imageBlog[i])" :alt="imageBlog[i]"
                                v-for="(element, i ) in element.image == null ? imageBlog : ''" :key="i"
                                class="imageSpecial">
                        </div>
                        <div class="info">
                            <div class="date">
                                <div class="day">
                                    <span>{{ element.day }}</span>
                                </div>
                                <div class="month">
                                    <span>{{ element.month }}</span>
                                </div>
                            </div>
                            <div class="text">
                                <h3>{{ element.title }}</h3>
                                <span>{{ element.text }}
                                </span>
                                <div class="icon">
                                    <i class="fa-regular fa-user"></i>
                                    <span>By {{ element.author }}</span>
                                    <i class="fa-regular fa-folder"></i>
                                    <span>{{ element.type }}</span>
                                    <i class="fa-regular fa-comments"></i>
                                    <span>{{ element.comments }}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="sidebar">
                    <div class="box">
                        <h3>LATEST FROM TWITTER</h3>
                        <div class="twitter">
                            <div class="icon">
                                <i class="fa-brands fa-twitter"></i>
                            </div>
                            <div class="text">
                                <span>If you have any suggestions fot the next updates, let us know</span>
                                <div class="date">
                                    <span>01:05 PM Sep 18th</span>
                                </div>
                            </div>
                        </div>
                        <div class="twitter">
                            <div class="icon">
                                <i class="fa-brands fa-twitter"></i>
                            </div>
                            <div class="text">
                                <span>We have just updated Porto Admin. Check the changelog for more information.</span>
                                <div class="date">
                                    <span>01:04 PM Sep 18th</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="box">
                        <h3>PHOTOS FROM INSTAGRAM</h3>
                        <div class="instagram">
                            <img :src="getImagePath(instagram[i])" :alt="instagram[i]" v-for="(element, i ) in 6" :key="i"
                                class="imageSpecial">
                        </div>
                    </div>
                    <div class="box">
                        <h3>TAGS</h3>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';

.w-100-3 {
    width: calc((100% / 3) - 5px);
}

.preview {
    background-color: $color-background-1;
    padding: 30px 0px;

    .container {
        @include mixins.center;
        display: flex;
        flex-wrap: wrap;
    }
}

.posts {
    background-color: $color-white;

    .container-posts {
        padding: 20px 0px;
        @include mixins.center;
        display: flex;
        justify-content: space-between;

        h3 {
            font-size: 15px;
        }

        .card-posts {
            display: flex;
            padding: 10px 0px;
            border-bottom: 1px dotted $color-border-6;

            img {
                width: 60px;
            }

            span {
                display: block;
                padding: 0px 20px;
            }

            .date {
                font-size: 12px;
                color: $color-text-3;
            }
        }

        .featured-posts {

            h3 {
                padding-bottom: 30px;
            }

            .card {
                width: 100%;
                padding: 0px;
                margin-bottom: 30px;

                .info {
                    width: 90%;
                    font-size: 9px;

                    button {
                        font-size: 7px;
                    }
                }
            }
        }

        .featured-author {
            height: 50%;

            h3 {
                padding-bottom: 30px;
            }

            img {
                width: 100px;
            }
        }
    }
}

.center {
    background-color: $color-white;

    .wrapper {
        @include mixins.center;
        display: flex;

        .item {
            width: 70%;

            .box {

                .image {
                    img {
                        width: 100%;
                    }

                    .imageSpecial {
                        width: calc(100% / 3);
                    }
                }

                .info {
                    padding: 20px 0px;
                    display: flex;

                    .date {
                        .day {
                            background-color: $color-background-1;
                            padding: 10px 5px;
                            text-align: center;
                        }

                        .month {
                            background-color: $color-background-6;
                            font-size: 10px;
                            padding: 5px;
                            color: $color-white;
                            text-align: center;
                        }
                    }

                    .text {
                        padding-left: 20px;

                        h3 {
                            padding-bottom: 20px;
                        }

                        span {
                            color: $color-text-3;
                            font-size: 13px;
                        }

                        .icon {
                            padding-top: 20px;
                            font-size: 13px;
                            color: $color-text-3;

                            i {
                                padding-right: 5px;
                            }

                            span {
                                padding-right: 10px;
                            }
                        }
                    }
                }
            }
        }

        .sidebar {
            width: 30%;

            .box {
                padding-left: 20px;
                padding-bottom: 30px;

                h3 {
                    font-size: 13px;
                    padding-bottom: 15px;
                }

                .twitter {
                    display: flex;
                    padding: 10px 0px;

                    .icon {
                        padding-right: 10px;
                    }

                    .text {
                        color: $color-text-3;

                        .date {
                            color: $color-primary;
                            padding-top: 10px;
                        }
                    }

                }

                .instagram {

                    display: flex;
                    flex-wrap: wrap;

                    img {
                        width: calc(100% /3);
                    }
                }
            }
        }
    }
}
</style>