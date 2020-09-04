<template>
    <div class="basic-container">
        <div>
            <span>ExModule标签；</span>
            <span>input_val:{{configure.input_val}}；</span>
            <span>name:{{configure.name}}；</span>
            <span>val:{{configure.val}}；</span>
        </div>

        <div class="sub-action-container">
            <slot></slot>
        </div>
    </div>
</template>

<script>
import '../../../assets/css/spanner/basic-view.css';
import BasicView from '../BasicView';

export default {
    name: 'Storage',
    extends: BasicView,
    data() {
        return {
            configure: {
                input_val: null,
                name: null,
                val: null
            }
        };
    },
    mounted() {
        let attrs = this.$attrs;
        this.configure = {
            input_val: attrs['input-val'],
            name: attrs['name'],
            val: attrs['val']
        };
    }
};
</script>

<style scoped>
</style>

