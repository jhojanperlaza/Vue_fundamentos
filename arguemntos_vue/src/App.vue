<template>
  <div class="parent-component"></div>
  <Child :message="message" />
  <ChildResponse @child-message="captureMessage" />
  <div>
    <p>
      El mensaje del hijo es {{ mensajeChild }}
    </p>
  </div>
</template>

<script>
import Child from './components/Child.vue';
import ChildResponse from './components/ChildResponse.vue';

export default {
  name: "parent-component",
  data() {
    return {
      message: "texto para el hijo",
      mensajeChild: ""
    };
  },
  components: {
    Child,
    ChildResponse,
  },
  methods: {
    captureMessage(mess) {
      console.log(mess)
      this.mensajeChild = mess;
    },
  },
};
</script>