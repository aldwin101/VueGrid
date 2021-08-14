<template>
    <div :class="{cardView : isGrid}">
            <TweetListComp v-for="tweets in tweetListContent" 
            :key="tweets" 
            :tweetContent= 'tweets.tweet'
            :tweetCreator= 'tweets.user'
            :tweetCreated= 'tweets.created'
        />
    </div>
</template>

<script>
import TweetListComp from './TweetListComp.vue'
    export default {
        name : 'TweetList',
        components : {
            TweetListComp
        },
        data : () => {
            return {
                tweetListContent : [
                    {
                        tweet : 'It is not the strongest of the species that survive, nor the most intelligent, but the one most responsive to change.',
                        user : 'Charles Darwin',
                        created : '2021/05/27'
                    },
                    {
                        tweet : 'The starting point of all achievement is desire.',
                        user : 'Napoleon Hill',
                        created : '2019/05/13'
                    },
                    {
                        tweet : 'The most difficult thing is the decision to act, the rest is merely tenacity..',
                        user : 'Amelia Earhart',
                        created : '2018/08/08'
                    },
                    {
                        tweet : 'Start where you are. Use what you have.  Do what you can. ',
                        user : 'Arthur Ashe',
                        created : '2019/12/13'
                    },
                    {
                        tweet : 'However difficult life may seem, there is always something you can do and succeed at.',
                        user : 'Stephen Hawking',
                        created : '2020/02/13'
                    },
                ],
                isGrid : false
            }
            },mounted(){
            this.$root.$on('onClick',this.switchView);
            },
            methods: {
            switchView(){
                if(this.isGrid == true){
                    this.isGrid = false
                }else{
                    this.isGrid = true
                }
            }
        }
}
</script>

<style scoped>
.cardView {
        display: grid;
        grid-template-columns: 1fr 1fr;
        column-gap: 1vw;
    }
</style>