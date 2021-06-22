<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <app-memory>
          <h1 slot="heading" class="text-center">It was great day</h1>
          <p slot="content" class="text-center">This was a goog memory....</p>
        </app-memory>
      </div>
    </div>
  </div>
</template>

<script>
  import Memory from './Memory';
  export default {
    components: {
      appMemory: Memory
    }
  }
</script>

