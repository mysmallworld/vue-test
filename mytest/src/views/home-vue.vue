<template>
<div class="home">
    <div class="title">
    <h1>Test technique WEB-ATRIO réalisé par Cheikh Inès<br>réalisé le 04/10/2022</h1>
    </div>

    <div class="allprogressbar">  
    <div class="firstprogressbar">  
    <h2>Initalisation du test technique</h2>

    <div class="row">
    <MyProgressBar/>
    </div>

    </div>

    <div class="secondprogressbar">
    <h2>Avancement de la phase de développement</h2>

    <div class="row">
    <MySecondProgressBar/>
    </div>
    </div> 
    
    </div>

<div class="mybuttons">
    <button class="buttons" @click="reinitialize()">Remettre à zéro les compteurs</button>
    <button class="buttons" @click="addfive()">Ajouter 5%</button>
    <button class="buttons" @click="addten()">Ajouter 10%</button>
</div>

</div>
</template>

<script>
import MyProgressBar from '../components/MyProgressBar.vue'
import MySecondProgressBar from '../components/MySecondProgressBar.vue'

export default {
  name: 'App',
  components: {
    MyProgressBar,
    MySecondProgressBar
  },
  data: function () {
    
    return {
      progressbar: 50,
    }
  },  methods: {
  reinitialize: function () {
    this.progressbar = 0;
  },
  addfive: function () {
    this.progressbar += 5;
  },
  addten: function () {
    this.progressbar += 10;
  }
  }
}
</script>

<style scoped>
/*Titre de la page*/
h1 {
    text-align: center;
    font-size: 18px;
    font-weight: bold;
}
.title {
    padding-top: 50px;
}

/*Titres des barres de progression*/
h2 {
    font-size: 10px;
    padding: 5px;
}

/*Barres de progression*/
.allprogressbar {
    top: 306px;
    left: 266px;
    width: 898px;
    height: 158px;
    margin: auto;
    padding: 80px;
}

/*Bouttons*/
.mybuttons {
    text-align: center;
    margin-top: 20px
}
.buttons {
    margin: 5px;
    padding: 10px;
    background: #303030;
    color: #FFFFFF;
}
</style>