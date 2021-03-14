<template>
  <div class="project--container">
    <div class="project">
      <div class="project--text">
        <h3>{{ name }}</h3>
        <p>{{ description }}</p>
        <ul>
          <li v-for="(item, idx) in list" :key="`${name}-${idx}`">
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="project--image">
        <img :src="image.src" :alt="image.alt" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: {
    name: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true,
    },
    list: {
      type: Array,
      default: () => { return [] }
    },
    image: {
      type: Object,
      default: undefined
    }
  }
}
</script>

<style lang="scss">
  .project--container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;

    margin: 50px 0 0;
  }
  .project {
    display: flex;
    align-items: center;
    justify-content: center;
    
    background-color: #fefefe;
    border-radius: 12px;

    width: 60vw;
    max-width: 900px;
    height: 450px;
  }
  .project--text {
    flex: 1 1 0;

    height: 400px;
    padding: 50px 0 50px 50px;

    h3 {
      font-weight: 600;
      font-size: 30px;
    }
    p {
      font-size: 18px;
      font-weight: 500;
      line-height: 24px;
    }
  }
  .project--image {
    flex: 1 1 0;
  }
</style>