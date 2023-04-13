<template>
    <div class="main">
        <!-- Passare i dati attraverso le props e generare 'carte' -->
        <div class="preview">
            <div class="container">
                <AppPreview v-for="(element, i) in preview" :key="i" :images="element.img" :types="element.type"
                    :title="element.title" />
            </div>
        </div>
        <!-- Posts -->
        <div class="posts">
            <div class="container-posts">
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
                <div class="featured-posts w-100-3">
                    <h3>FEATURED POSTS</h3>
                    <AppPreview :images="'blog-66.jpg'" :types="'RECIPES'"
                        :title="'Tips to Help You Quickly Prepare your Lunch'" />
                    <div class="featured-author">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
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
            ]
        }
    }
}
</script>
<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';

.w-100-3 {
    width: calc((100% / 3) - 20px);
    padding-right: 20px;
}

.preview {
    background-color: $color-background-1;

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
            padding: 5px 0px;
            border-bottom: 1px dotted $color-border-6;

            img {
                width: 70px;
            }

            span {
                display: block;
                padding: 0px 20px;
                padding-top: 10px;
            }

            .date {
                font-size: 12px;
                color: $color-text-3;
            }
        }

        .featured-posts {
            .card {
                width: 100%;
                padding: 20px 0px;


                .info {
                    width: 80%;
                    font-size: 9px;

                    button {
                        font-size: 7px;
                    }
                }
            }
        }
    }
}
</style>