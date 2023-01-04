<template>
  <div> {{ message }}</div>
</template>

<script>
  export default {
    name: "Child",
    props: {
      message: String,
    },
  };
  
</script>