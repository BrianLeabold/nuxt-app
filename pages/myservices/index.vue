<template>
  <section id="main" class="content">
    <h2>Services</h2>
    <div class="services">
      <Service
        v-for="service in services"
        :key="service.id"
        :thumbnail="service.thumbnail"
        :title="service.title"
        :id="service.id"
        :date="service.date"
        :previewText="service.previewText"
      />
    </div>
  </section>
</template>
<script>
import Service from '@/components/Service'
export default {
  components: {
    Service
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          services: [
            {
              id: '3',
              title: 'Delicious Pizza',
              date: '10/5/2019',
              previewText: 'Pizza Pizza',
              thumbnail:
                'https://www.kingarthurflour.com/sites/default/files/styles/featured_image/public/recipe_legacy/20-3-large.jpg?itok=1EY8KWJG'
            },
            {
              id: '2',
              title: 'Zucchini Crust Pizza',
              date: '10/1/2019',
              previewText: 'Awesome Crust',
              thumbnail:
                'https://therecipecritic.com/wp-content/uploads/2018/08/zucchini_crust_pizza-1-of-1.jpg'
            },
            {
              id: '1',
              title: 'Breakfast Pizza',
              date: '9/25/2019',
              previewText: 'The best of both worlds',
              thumbnail:
                'https://www.skinnytaste.com/wp-content/uploads/2018/02/breakfast-pizza-1-8.jpg'
            }
          ]
        })
      }, 1500)
    })
  }
}
</script>
<style scoped>
.services {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
.service {
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}
.preview-image {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
.date {
  background: #ccc;
  color: #000;
  padding: 2px 5px;
  bottom: 0;
  left: 0;
}
</style>