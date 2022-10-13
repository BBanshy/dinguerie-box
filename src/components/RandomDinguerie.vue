<template>
  <div class="card">
    <img src="../assets/dinguerie.svg" style="width: 100%" />
    <div class="container">
      <div class="dinguerie">{{ dinguerie }}</div>
      <button v-on:click="getDinguerie" class="button-17" role="button">
        Balances une dinguerie
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "RandomDinguerie",
  props: {
    msg: String,
  },
  data() {
    return {
      icon: "👾",
      dinguerie: "Cliques pour faire apparaître une dinguerie",
    };
  },
  methods: {
    getDinguerie() {
      // A remplacer par un call Axios 
      // Attente création d'A.P.I.
      const dingueries = [
        "Elle a la jupe au raz du sillot !",
        "Ca m'en touche une sans réveiller l'autre.",
        "C'est pas une fois qu'on s'est chié dessus qu'il faut serrer les fesses.",
        "Casses pas la couille.",
        "À vaincre sans baril, on triomphe sans boire.",
        "Se mettre la rate au court bouillon.",
        "Le D c'est le S.",
        "D'après le théorème de Thalès, si tu roules en Mercedes; t'as Ines qui écarte ses fesses.",
        "J'ai failli faire un AVC",
        "Et bang, et bang,et bang.",
      ];
      const dinguerieId = Math.floor(Math.random() * (10 - 0) + 0);
      this.dinguerie = dingueries[dinguerieId];
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div .container .dinguerie {
  display: flex;
  justify-content: center;
}
div .card img {
  width: 150px;
  height: 150px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  width: 100%;
  height: 300px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.container {
  padding: 2px 36px;
}

/* CSS */
.button-17 {
  align-items: center;
  margin-top: 50px;
  appearance: none;
  background-color: #fff;
  border-radius: 24px;
  border-style: none;
  box-shadow: rgba(0, 0, 0, 0.2) 0 3px 5px -1px,
    rgba(0, 0, 0, 0.14) 0 6px 10px 0, rgba(0, 0, 0, 0.12) 0 1px 18px 0;
  box-sizing: border-box;
  color: #3c4043;
  cursor: pointer;
  display: inline-flex;
  fill: currentcolor;
  font-family: "Google Sans", Roboto, Arial, sans-serif;
  font-size: 14px;
  font-weight: 500;
  height: 48px;
  justify-content: center;
  letter-spacing: 0.25px;
  line-height: normal;
  max-width: 100%;
  overflow: visible;
  padding: 2px 24px;
  position: relative;
  text-align: center;
  text-transform: none;
  transition: box-shadow 280ms cubic-bezier(0.4, 0, 0.2, 1),
    opacity 15ms linear 30ms, transform 270ms cubic-bezier(0, 0, 0.2, 1) 0ms;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  width: auto;
  will-change: transform, opacity;
  z-index: 0;
}

.button-17:hover {
  background: #f6f9fe;
  color: #174ea6;
}

.button-17:active {
  box-shadow: 0 4px 4px 0 rgb(60 64 67 / 30%),
    0 8px 12px 6px rgb(60 64 67 / 15%);
  outline: none;
}

.button-17:focus {
  outline: none;
  border: 2px solid #4285f4;
}

.button-17:not(:disabled) {
  box-shadow: rgba(60, 64, 67, 0.3) 0 1px 3px 0,
    rgba(60, 64, 67, 0.15) 0 4px 8px 3px;
}

.button-17:not(:disabled):hover {
  box-shadow: rgba(60, 64, 67, 0.3) 0 2px 3px 0,
    rgba(60, 64, 67, 0.15) 0 6px 10px 4px;
}

.button-17:not(:disabled):focus {
  box-shadow: rgba(60, 64, 67, 0.3) 0 1px 3px 0,
    rgba(60, 64, 67, 0.15) 0 4px 8px 3px;
}

.button-17:not(:disabled):active {
  box-shadow: rgba(60, 64, 67, 0.3) 0 4px 4px 0,
    rgba(60, 64, 67, 0.15) 0 8px 12px 6px;
}

.button-17:disabled {
  box-shadow: rgba(60, 64, 67, 0.3) 0 1px 3px 0,
    rgba(60, 64, 67, 0.15) 0 4px 8px 3px;
}
</style>
