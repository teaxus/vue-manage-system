<template>
    <div class="basic-container">
        <div>
            <span>Var标签；</span>
            <span>name={{configure.name}}；</span>
            <span>val={{configure.val}}；</span>
            <span>goto-tag-name={{configure.goto_tag_name}}；</span>
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
    name: 'Var',
    extends: BasicView,
    data() {
        return {
            configure: {
                name: null,
                val: null,
                goto_tag_name: null
            }
        };
    },
    mounted() {
        let attrs = this.$attrs;
        this.configure = {
            name: attrs['name'],
            val: attrs['val'],
            goto_tag_name: attrs['goto-tag-name']
        };
    }
};
</script>

<style scoped>
</style>
