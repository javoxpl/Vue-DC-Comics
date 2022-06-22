<template>

<footer>

  <img src="/images/dc-logo-bg.png" alt="">
  <article>
  <ul>
    <h3>dc comics</h3>
    <li v-for="(item, index) in lists" :key ='index'>
      {{item.testo}}
    </li>
    <ul>
    <h3>shop</h3>
    <li>Shop DC</li>
    <li>Shop DC Collectibles</li>  
    </ul>
  </ul>

  <ul>
     <h3>dc</h3>
    <li>Terms Of Use</li>
    <li>Privacy policy (New)</li> 
    <li>Ad Choices</li>
    <li>Advertising</li>
    <li>Jobs</li>
    <li>Subscriptions</li>
    <li>Talent Workshops</li>
    <li>CPSC Certificates</li>
    <li>Ratings</li>
    <li>Shop Help</li>
    <li>Contact Us</li>
  </ul>
  <ul>
    <h3>sites</h3>
    <li>dc</li>
    <li>MAD Magazines</li>
    <li>DC Kids</li>
    <li>DC Universe</li>
    <li>DC Power Visa</li>

  </ul>
  </article>
  <div>
    <section>
        <button>
          sign-up now!
        </button>

       <div class="follow">
          <h3>follow us</h3>
          <div v-for="(img, index) in imgs" :key="index">
          <img :src="img.link" alt="">
        </div>
        
       </div>
       
    </section>
   </div>
 </footer> 

</template>

<script>

export default {
  name: 'AppFooter',
  props:['imgs'],
  data(){
    return{
      lists:[
        {
          testo:"characters",
          link:"",
          active: false
        },
        {
          testo:"comics",
          link:"",
          active: true
        },
        {
          testo:"movies",
          link:"",
          active: false
        },
        {
          testo:"tv",
          link:"",
          active: false
        },
        {
          testo:"games",
          link:"",
          active: false
        },
        {
          testo:"videos",
          link:"",
          active: false
        },
        {
          testo:"news",
          link:"",
          active: false
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '../style/variables';
@import '../style/generals';

footer{
    position: relative;
    background-image: url('/public/images/footer-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;
}
article{
  column-gap: 25px;
  display: flex;
  width: $width;
  margin: 0 auto;
  padding: 30px 0;
}
button{
  margin: 25px 25px 25px  0;
  border: 2px solid $bg-active;
  padding: 10px;
  background-color: transparent;
  color: $font-white;
  text-transform: uppercase;
}
section{
  justify-content: space-between;
  align-items: center;
  display: flex;
  width: $width;
  margin: 0 auto;
}
.follow{
  align-items: center;
  display: flex;
  column-gap: 20px;
  color: $bg-active;
}
.follow>h3{
  font-size: $main-font-size;
  color: $bg-active;
}

footer>img{
  z-index: 0;
  right: 200px;
  top: -100px;
  height: 500px;
  position: absolute;
}
div>img{
  float: left;
}
ul{
  padding: 10px 0;
}
ul>h3{
    font-size: $main-font-size;
}
h3{
  padding-bottom: 5px;
  text-transform: uppercase;
  color: $font-white;
}
h3:nth-child(2){
  color: $bg-active;
}

li{
  font-size: $small-font-size;
  padding: 3px 0;
  text-transform: capitalize;
  list-style-type: none;
  color: $font-light-grey;
}
div{
  position: relative;
  z-index: 1000;
  background-color: $bg-light-black;
}
h1{
  color: $bg-active;
  font-weight: 400;
}

</style>
