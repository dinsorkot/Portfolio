<script setup>
const carouselItems = [
  {
    imageSrc: 'src/assets/certificate/unity.jpg',
    caption: '',
    content: '',
  },
  {
    imageSrc: 'src/assets/certificate/depa.jpg',
    caption: '',
    content: '',
  },
  {
    imageSrc: 'src/assets/certificate/sql.jpg',
    caption: '',
    content: '',
  },
  {
    imageSrc: 'src/assets/certificate/js.jpg',
    caption: '',
    content: '',
  },
  {
    imageSrc: 'src/assets/certificate/test.jpg',
    caption: '',
    content: '',
  },
  {
    imageSrc: 'src/assets/certificate/digitalcontent.jpg',
    caption: '',
    content: '',
  },
];
</script>

<template>
  <div class="d-flex justify-content-center pt-5 position-absolute top-50 start-50 translate-middle">
    <div id="carouselExampleCaptions" class="carousel carousel-dark slide" data-bs-ride="carousel">
      <div class="carousel-indicators">
        <button
          v-for="(item, index) in carouselItems"
          :key="index"
          :data-bs-target="'#carouselExampleCaptions'"
          :data-bs-slide-to="index"
          :class="{'active': index === 0}"
          aria-label="Slide {{ index + 1 }}"
        ></button>
      </div>
      <div class="carousel-inner">
        <div
          v-for="(item, index) in carouselItems"
          :key="index"
          class="carousel-item"
          :class="{'active': index === 0}"
        >
          <img :src="item.imageSrc" class="d-block " alt="...">
          <div class="carousel-caption d-none d-md-block">
            <h5>{{ item.caption }}</h5>
            <p>{{ item.content }}</p>
          </div>
        </div>
        
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</template>
<style scoped>
img {
    width: 300px;
}
@media (min-width: 568px) {
    img {
        width: 550px;
    }
}
</style>