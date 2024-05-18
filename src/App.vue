<script setup lang="ts">
import { ref } from "vue";

const isAgree = ref<boolean>(false);
const isDecline = ref<boolean>(false);

const selectDecline = () => {
  isDecline.value = true;
};

const selectAgree = () => {
  isAgree.value = true;
};
</script>

<template>
  <div class="container">
    <div class="card">
      <h1 class="text-white">Cats Rock!</h1>
      <transition name="fade">
        <template v-if="isAgree">
          <p class="text-white">You said you <span> agree. </span></p>
        </template>
      </transition>
      <transition name="fade">
        <template v-if="isDecline">
          <p class="text-white">You said you <span> don’t agree. </span></p>
        </template>
      </transition>
      <transition name="fade">
        <div v-if="!isAgree && !isDecline">
          <p class="text-white">
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book. It has survived not
            only five centuries, but also the leap into electronic typesetting,
            remaining essentially unchanged.
          </p>
          <div class="buttons-container">
            <button @click="selectAgree" class="bg-primary">I agree</button>
            <button @click="selectDecline" class="bg-secondary decline-btn">
              I do not
            </button>
          </div>
        </div>
      </transition>
    </div>
  </div>
</template>

<style scoped>
@media (min-width: 550px) {
  .container {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
}

.buttons-container {
  margin-top: 4rem;
}

.card {
  background-color: #342828;
  width: 378px;
  height: 532px;
  overflow: auto;
  border-radius: 12px;
  padding: 3.3rem;
  margin-left: 10rem;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.6);
}

@media (max-width: 550px) {
  .buttons-container {
    margin-top: 2rem;
  }

  .card {
    margin: 0;
    padding: 2rem 2.5rem;
    width: 100%;
    height: 481px;
    position: absolute;
    bottom: 0;
  }
}

h1 {
  margin: 0;
  text-align: left;
  font-family: "Lato", "Roboto";
  font-weight: 400;
  font-size: 24px;
}
p {
  font-size: 16px;
  font-family: "Roboto";
}

span {
  font-weight: 700;
}

.decline-btn {
  margin-top: 1rem;
}

/* Transition classes */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
