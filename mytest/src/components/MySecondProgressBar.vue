<template>
 <div class="progressbar">
    <div class="progressbar-wrapper">
    <div class="progressbar advance" style="width: 25%" data-perc="25%"></div>
    </div>
    </div>
</template>

<script>
export default {
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
  background-color: #7160E8;
  width: 100%;
}
</style>
