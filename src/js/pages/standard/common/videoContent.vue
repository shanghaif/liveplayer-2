<template>
    <div class="wrapper">
        <div class="content-item" v-for="v in items">
            <div class="content-item-image">
                <image class="content-item-background" :src="v.image"></image>
                <text class="content-item-category"></text>
                <div class="content-item-bottom">
                    <text class="content-item-count">{{v.playCount}}</text>
                    <text class="content-item-name">{{v.commentCount}}</text>
                    <text class="content-item-time">{{v.time}}</text>
                </div>
            </div>
            <text class="content-item-description">{{v.description}}</text>
        </div>
    </div>
</template>

<style scoped>
    .wrapper{
    }
    .content-item{
        padding:20px;
        width:375px;
        height:250px;
        flex-direction: column;
    }
    .content-item-image{
        width:335px;
        height:200px;
        flex-direction: column;
        justify-content: space-between;
        border-bottom-left-radius: 20px;
        border-bottom-right-radius: 20px;
        border-top-left-radius: 20px;
        border-top-right-radius: 20px;
    }
    .content-item-description{
        width:375px;
        height:50px;
    }
    .content-item-background{
        position: absolute;
        width:375px;
        height:200px;
    }
    .content-item-category{
        align-self: flex-end;
        color: rgba(255, 255, 255, 1);
    }
    .content-item-bottom{
        flex-direction: row;
        justify-content: space-between;
    }
    .content-item-name{
        align-self: flex-start;
        color: rgba(255, 255, 255, 1);
    }
    .content-item-count{
        align-self: flex-start;
        color: rgba(255, 255, 255, 1);
    }
    .content-item-time{
        align-self:flex-end;
    }
</style>

<script>
    export default {
        props: {
            items: {
                type: Array,
                default: [
                    {
                        category: '',
                        name: '',
                        count: 1,
                        image: '',
                        description: ''
                    }
                ]
            }
        },
        data() {
            return {}
        }
    };
</script>
