<template>
<div>
    <div style="color:red">
        <div>ffffkk_1</div>
        <div>ffffkk_2</div>
        <div>ffffkk_3</div>
    </div>
    <slot></slot>
</div>
</template>

<script>
export default {
    name: 'BasicView',
    mounted() {
        console.log('basic view');
    }
};
</script>

<style scoped>
</style>
