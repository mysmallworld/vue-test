<template>
 <div class="progressbar">
    <span>{{width}}%</span>
    <div class="progressbar-wrapper">
    <div class="progressbar advance" :style="btnStyles"></div>
    </div>
    </div>
</template>

<script>
export default {
 name: 'SimpleButton',
  props: {
    bgColor: {
      type: String,
      default: "#6DADE8"
    },
    width: {
      type: Number,
      default: 50
    }
  },
  computed: {
    btnStyles() {
      return {
        "background-color": this.bgColor,
        width: `${this.width}%`
      };
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
  background: var(--bgColor);
  width: var(--width);
}
</style>
