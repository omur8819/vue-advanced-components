<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <br><br>
        <button @click="selectedComponent = 'appMemory'" class="btn-sm btn btn-primary">appMemory</button>
        <button @click="selectedComponent = 'appNewMemory'" class="btn-sm btn btn-primary">appNewMemory</button>
        <button @click="selectedComponent = 'appAuthor'" class="btn-sm btn btn-primary">appAuthor</button>
        <br><br>
        <p>{{selectedComponent}}</p>
        <hr>


        <component :is="selectedComponent">
          <h1 slot="heading" class="text-center">It was great day</h1>
          <p slot="content" class="text-center">This was a good memory....</p>

        </component>


        <!-- <app-memory>
          <h1 slot="heading" class="text-center">It was great day</h1>
          <p slot="content" class="text-center">This was a goog memory....</p>
        </app-memory> -->
      </div>
    </div>
  </div>
</template>

<script>
  import Memory from './components/Memory.vue';
  import NewMemory from './components/NewMemory.vue';
  import Author from './components/Author.vue';
  export default {
    data: function(){
      return {
        selectedComponent: ""
        }
    },
    components: {
      appMemory: Memory,
      appAuthor: Author,
      appNewMemory: NewMemory,
    }
  }
</script>

