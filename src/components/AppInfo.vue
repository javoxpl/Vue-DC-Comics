<template>
   <section class="info-box">
        <ul>
            <li v-for="(item, index) in items" :key='index'>
                <img :src="item.img" :alt="item.img">
                <span>{{item.testo}}</span> 
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name:'AppInfo',
    data(){
        return{
        items:[
            {
                img:'/images/buy-comics-digital-comics.png',
                testo:"digital comics",
                active: false
            },
            {
                img: '/images/buy-comics-merchandise.png',
                testo:"dc merchandise",
                active: false
            },
            {
                img: '/images/buy-comics-subscriptions.png',
                testo:"subscriptions",
                active: false
            },
            {
                img:'/images/buy-comics-shop-locator.png',
                testo:"comics shop locator",
                active: false
            },
            {
                img:'/images/buy-dc-power-visa.svg',
                testo:"dc power visa",
                active: false
            }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
@import '../style/generals';

.info-box{
    position: relative;
    z-index: 1000;
    height: 125px;
    background-color: $bg-active;
    margin: 0 auto;
}
li>img{
    vertical-align: middle;
    height: 35px;
}
ul{
    width: $width;
    margin: 0 auto;
}
h2{
    line-height: 70px;
    width: $width;
    margin: 0 auto;
}
li{
    width: calc(100% / 5);
    line-height: 125px;
    list-style-type: none;
    float: left;
}

span{
    text-transform: uppercase;
    padding-left: 10px;
    color: $font-white;
    font-size: $main-font-size;
}

</style>