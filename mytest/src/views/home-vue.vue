<template>
<div class="home">
    <div class="title">
    <h1>Test technique WEB-ATRIO réalisé par Cheikh Inès<br>réalisé le 04/10/2022</h1>
    </div>

    <div class="allprogressbar">  
    <div class="firstprogressbar">  
    <h2>Initalisation du test technique</h2>
    <MyProgressBar/>
    </div>

    <div class="secondprogressbar">
    <h2>Avancement de la phase de développement</h2>
    <MyProgressBar/>
    </div> 
    </div>

<div class="mybuttons">
    <button class="buttons" @click="reinitialize(width, bgColor)">Remettre à zéro les compteurs</button>
    <button class="buttons" @click="addfive(width, bgColor)">Ajouter 5%</button>
    <button class="buttons" @click="addten(width, bgColor)">Ajouter 10%</button>
</div>

</div>
</template>

<script>
import MyProgressBar from '../components/MyProgressBar.vue'

export default {
  name: 'App',
  components: {
    MyProgressBar
  },
  data: function () {
    if(0 < this.width > 25)return this.bgColor = "#7160E8";
    if(25 < this.width > 50)return this.bgColor = "#6DADE8";
    if(50 < this.width > 75)return this.bgColor = "#60E8B6";
    if(75 < this.width > 100)return this.bgColor = "#30DB63";

    return {
    bgColor: "#303030",
    width: 0,
    }
  },  methods: {
  reinitialize: function () {
    this.bgColor = "#303030";
    this.width = 0;
  },
  addfive: function () {
    this.width += 5;
  },
  addten: function () {
    this.width += 10;
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

.secondprogressbar {
    padding-top: 10px;
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