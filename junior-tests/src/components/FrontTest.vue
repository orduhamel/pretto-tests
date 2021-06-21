<template>
  <div>
    <h1>Implémenter une popup</h1>
    <p>
      Pour commencer, tu vas devoir "forker" ce site depuis le repo
      <a href="https://github.com/F-Hameau/pretto-tests" target="_blank">Github</a>
    </p>
    <p>
      Ensuite, on code ! Le but ici est d'afficher le contenu de l'input ci-dessous dans une popup au clic sur le
      bouton
    </p>
    <div>
      <input class="large" type="text" placeholder="Texte à mettre dans la popup" />
    </div>
    <div>
      <button class="large">Afficher la popup</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "FrontTest",
};
</script>

<style scoped>
input {
  font-family: "MaisonNeue-Medium";
  font-size: 16px;
  margin-bottom: 24px;
  padding: 15px 0px;
  text-align: center;
}
</style>
