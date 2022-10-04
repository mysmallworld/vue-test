<template>
 <div class="progressbar">
    <div class="progressbar-wrapper">
    <div class="progressbar advance" style="width: 50%" data-perc="50%"></div>
    </div>
    </div>
</template>

<script>
export default {
  data: function () {
    return {
      progressbar: 0,
    }
  },  methods: {
  subscribe: function () {
    this.progressbar++;
  }
  }
}
</script>


<style scoped>
.progressbar {
  padding: 5px;
}

.progressbar-wrapper {
  background-color: #303030;
  color: white;
  width: 100%;
}

.advance {  
  background-color: #6DADE8;
  width: 100%;
}
</style>
