<template>
  <section class="single-service">
    <h2>{{services.title}}</h2>
    <img class="service-image" :src="services.thumbnail" :alt="services.title" />
    <span>{{services.date}}</span>
    <p>{{services.previewText}}</p>
  </section>
</template>
<script>
export default {
  asyncData(context) {
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
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.single-service {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  padding: 30px;
}
.service-image {
  width: 40%;
}
</style>