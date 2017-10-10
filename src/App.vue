<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br>
        <button class="btn btn-primary" @click="currentComponent = 'appBlue' ">Load Blue Template</button>
        <button class="btn btn-success" @click="currentComponent = 'appGreen'" >Load Green Template</button>
        <button class="btn btn-danger" @click="currentComponent = 'appRed'" >Load Red Template</button>
        <hr>
        <component :is='currentComponent'>
          <h2 slot="titleBlue">i am the blue title by slot</h2>
          <h2 slot="titleRed"> i am the red title by slot</h2>
          <h2 slot="titleGreen"> i am the Green title by slot</h2>
        </component>
      </div>
    </div>
  </div>
</template>

<script>
import Blue from './components/Blue.vue';
import Green from './components/Green.vue';
import Red from './components/Red.vue';

export default {
  data () {
    return {
      currentComponent: 'appBlue'
    }
  },
  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red
  }
}
</script>

<style>
</style>
