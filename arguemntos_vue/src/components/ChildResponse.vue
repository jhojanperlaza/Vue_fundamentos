<template>
    
</template>

<script>
export default {
    name: "ChildResponse",
    data () {
        return {
            message: "el hijo responde al padre",
        };
    },
    methods: {
        sendMessageToParent() {
            this.$emit("child-message", this.message);
        },
    },
    mounted() {
        this.sendMessageToParent();
    }
};
</script>