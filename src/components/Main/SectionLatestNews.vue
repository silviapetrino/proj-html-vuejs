<script>
import news from '../../data/news';


export default {
  name: 'latest-news-section',
  data() {
    return {
      news
    };
  }
 
}
</script>

<template>
  <section id="latest-news">
    <div class="container-sp">

      <div class="card-sp text-center">
        <h2 class="py-4">Latest News</h2>
        <div class="wrapper d-flex justify-content-center gap-5">
          <div class="news-box debug d-flex flex-column text-center" v-for="(newItem, index) in news" :key="`news-${index}`">
          <img :src="newItem.image" :alt="newItem.title" width="450">
          <h4 class="title py-2">{{ newItem.title }}</h4>
          <div class="date-comment">
            <span class="date">{{ newItem.date }} &#124; </span>
            <span class="comments">{{ newItem.comments + ' ' + 'comments' }}</span>
          </div>  
          <span class="abstract">{{ newItem.abstract }}</span>
        </div>
        </div>
      
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.card-sp {
  width: 100%;
  overflow: hidden;
  border-top: 5px solid $main-color;
  border-radius: 8px;
  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
  background-color: $white;
  cursor: pointer;
  transition: all .1s ease;
  position: relative;
  top: -30px;

  &:hover {
    transform: scale(1.1);
  }
  h2 {
    font-weight: $fw-600;
    color: $black;
    text-transform: capitalize;
  }
  .title, .comments {
    color: $main-color;
  }
  .title {
    font-weight: $fw-600;
  }
  .date, .abstract {
    color: $dark-gray;
  }
  .date, .comments {
    font-size: $sm-size-b;
  }
}
</style>
