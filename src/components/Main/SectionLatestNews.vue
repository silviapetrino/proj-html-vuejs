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

      <div class="card-sp text-center pb-5">

        <h2 class="py-4">Latest News</h2>

        <div class="wrapper d-flex justify-content-center gap-5">
          <div class="news-box debug d-flex flex-column text-center" v-for="(newItem, index) in news" :key="`news-${index}`">
            <img :src="newItem.image" :alt="newItem.title" width="450">
            <h4 class="title py-2">{{ newItem.title }}</h4>
            <div class="date-comment pb-2">
              <span class="date">{{ newItem.date }} &#124; </span>
              <span class="comments">{{ newItem.comments + ' ' + 'comments' }}</span>
            </div>  
            <span class="abstract">{{ newItem.abstract }}</span>
          </div>
        </div>
        <!-- Inserire componente bottone  -->
      </div>

      <img width="1100" class="arrow" src="/latestnews-bottom.png" alt="latest-news-background">

    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

section#latest-news {
  background-image: url('/latestnews-background.jpg');
  background-position: center;
  background-size: cover;
}

.card-sp {
  width: 100%;
  overflow: hidden;
  border-top: 5px solid $main-color;
  border-radius: 8px;
  background-color: $white;
  cursor: pointer;
  position: relative;
  top: -30px;

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

img.arrow {
  width: 100%;
  position: relative;
  top: -30px;
}

</style>
