<template>
  <a :href="url" class="project-container" target="_blank">
    <img :src="imgLink" :alt="title">
    <div class="project-title">{{ title }}</div>
    <div class="project-subtitle">{{ subtitle }}</div>
  </a>
</template>

<script>
export default {
  props: ['id', 'title', 'subtitle', 'url'],
  computed: {
    imgLink () {
      return require(`../assets/${this.id}.png`)
    }
  }
}
</script>

<style>
  .project-container {
    width: 128px;
    height: 128px;
    border-radius: 30px;
    display: block;
    border: 1px solid #e0e0e0;
    box-shadow: .125em .125em .375em #e0e0e0;
    text-decoration: none;
  }
  .project-container:hover {
    border-color: #d0d0d0;
    box-shadow: .125em .125em .375em #d0d0d0;
  }
  .project-container:active {
    box-shadow: 0 0 .375em #d0d0d0;
  }

  .project-title {
    font-size: 1rem;
    text-align: center;
  }

  .project-subtitle {
    font-size: .8rem;
    width: 200%;
    margin-left: -50%;
    margin-top: -30px;
    text-align: center;
    border-radius: 3px;
    padding: .2rem;
    color: #aaa;
    background: rgba(0, 0, 0, 0.8);
    position: relative;
    z-index: 999;
    opacity: 0;
  }
  .project-container:hover .project-subtitle {
    opacity: 1;
    margin-top: .5rem;
    transition: all .3s;
  }
</style>
