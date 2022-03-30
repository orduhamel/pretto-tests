<template>
  <div>
    <button @click="openModal" class="large">Afficher la popup</button>
    <portal to="front-test-modal">
      <modal v-show="showModal" class="modal-backdrop">
        <div class="modal">
          <div class="modal-header">
            <h2>Vous avez écrit :</h2>
          </div>
          <p class="modal-body">{{ text }}</p>
          <button @click="closeModal">Fermer</button>
        </div>
      </modal>
    </portal>
  </div>
</template>

<script>
export default {
  name: "FrontTestModal",
  data() {
    return {
      showModal: false
    }
  },
  props: {
    text: {
      type: String,
      default: "Aucun input ajouté"
    }
  },
  methods: {
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    }
  }
}
</script>

<style>
.modal-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.125);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  width: 50%;
  background: #FFFFFF;
  box-shadow: 2px 2px 20px 1px;
  overflow-x: auto;
  display: flex;
  flex-direction: column;
}

.modal-header {
  padding: 15px;
  text-align: center;
  border-bottom: 1px solid #eeeeee;
  color: #4AAE9B;
}

.modal-body {
  position: relative;
  padding: 20px 10px;
}
</style>
