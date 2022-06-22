<template>

  <div id="app">
      <app-header :link = "LinksNavbar"/> 
      <main>
        <app-jumbotron/>
        <section>
          <app-grid/>
       
          <app-info/>
        </section>
        
      </main>
    
      <app-footer :imgs = "FooterImages"/>

   </div> 

</template>

<script>

import AppHeader from './components/AppHeader.vue';
import AppGrid from './components/AppGrid.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppInfo from './components/AppInfo.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppGrid,
    AppFooter,
    AppJumbotron,
    AppInfo,
  },
  data(){ 
    return {
      LinksNavbar:[
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
          testo:"collectibles",
          link:"",
          active: false
        },
        {
          testo:"videos",
          link:"",
          active: false
        },
        {
          testo:"fans",
          link:"",
          active: false
        },
        {
          testo:"news",
          link:"",
          active: false
        },
        {
          testo:"shop",
          link:"",
          active: false
        }
      ],
      activeIndex:0,
      FooterImages:[
          {
          testo:"facebook",
          link:'/images/footer-facebook.png'
          },
          {
          testo:"twitter",
          link:'/images/footer-twitter.png'
          },
          {
          testo:"youtube",
          link:'/images/footer-youtube.png'
          },
          {
          testo:"pinterest",
          link:'/images/footer-pinterest.png'
          },
          {
          testo:"periscope",
          link:'./images/footer-periscope.png'
          },
      ],  
          }
        }
      }
</script>

<style lang="scss">
@import './style/variables';
@import './style/generals';

</style>
