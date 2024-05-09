<template>
  <div class="container mt-5 d-flex">
    <button class="btn btn-primary" type="button" data-bs-target="#multiItemCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
    <div id="multiItemCarousel" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div v-for="(slide, index) in slides" :key="index" :class="['carousel-item', { 'active': index === 0 }]">
          <div class="row g-4">
            <div v-for="(item, itemIndex) in slide.items" :key="itemIndex" class="col-md-4 col-lg-3 px-2">
              <card-comp :title="item.title" :text="item.description"></card-comp>
            </div>
          </div>
        </div>
      </div>
    </div>
   
      <button class="btn btn-primary" type="button" data-bs-target="#multiItemCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
  </div>
</template>

<script>
import CardComp from './CardComp.vue';
export default {
  name: 'CarouselComp',
  data() {
    return {
      slides: [
        {
          items: [
            {
              title: 'Item 1',
              description: 'This is item 1',
              image: 'https://via.placeholder.com/400x300?text=Item+1'
            },
            {
              title: 'Item 2',
              description: 'This is item 2',
              image: 'https://via.placeholder.com/400x300?text=Item+2'
            },
            {
              title: 'Item 3',
              description: 'This is item 3',
              image: 'https://via.placeholder.com/400x300?text=Item+3'
            },
            {
              title: 'Item 3',
              description: 'This is item 3',
              image: 'https://via.placeholder.com/400x300?text=Item+8'
            }
          ]
        },
        {
          items: [
            {
              title: 'Item 4',
              description: 'This is item 4',
              image: 'https://via.placeholder.com/400x300?text=Item+4'
            },
            {
              title: 'Item 5',
              description: 'This is item 5',
              image: 'https://via.placeholder.com/400x300?text=Item+5'
            },
            {
              title: 'Item 6',
              description: 'This is item 6',
              image: 'https://via.placeholder.com/400x300?text=Item+6'
            }
          ]
        }
      ]
    };
  },

  components: {
    CardComp
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>