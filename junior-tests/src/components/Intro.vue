<template>
  <div>
    <h1>Junior Software Engineer</h1>
    <p>Du back et du front pour tester ta technique</p>
    <div class="button-container">
      <div class="test large">
        <button class="large" @click="open('https://www.codewars.com/kata/550554fd08b86f84fe000a58/train/ruby')">
          Which are in?
        </button>
        <div class="description">
          <p>Un test sur codewars à faire en ruby.</p>
          <p>
            Pas de panique si tu n'en as jamais fait, on est là pour t'aider et la
            <a href="https://ruby-doc.org/core-2.7.0/Array.html" target="_blank">doc</a> aussi !
          </p>
        </div>
      </div>
    </div>
    <div class="button-container">
      <div class="test large">
        <button class="large" @click="open('https://www.codewars.com/kata/55c6126177c9441a570000cc/train/javascript')">
          Weight for weight
        </button>
        <div class="description">
          <p>Un second test sur codewars mais cette fois tu le langage :)</p>
        </div>
      </div>
    </div>
    <div class="button-container">
      <div class="test large">
        <button class="large" @click="$emit('displayFrontTest')">Implémenter une popup</button>
        <div class="description">
          <p>On termine avec un peu de front.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Intro",
  methods: {
    open(url) {
      window.open(url, "_blank");
    },
  },
};
</script>

<style scoped>
.button-container {
  width: 100%;
  display: flex;
  justify-content: center;
  padding: 8px;
}
.description {
  text-align: left;
  box-shadow: 0px 0px 0px 5px #fc5c63 inset;
  width: 100%;
  max-width: 484px;
  padding: 8px;
  font-family: "MaisonNeue-Book";
}
.description p {
  margin-top: 0px;
}
.test {
  margin-top: 16px;
}
.test:hover .description {
  box-shadow: 0px 0px 0px 5px #fc847c inset;
}
.test:hover button {
  background-color: #fc847c;
}
</style>
