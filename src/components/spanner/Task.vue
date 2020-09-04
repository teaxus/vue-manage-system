<template>
    <div class="basic-container">
        <div>
            <span>Task标签</span>
            <span>retry_time={{configure.retry_time}}；</span>
            <span>over_time={{configure.over_time}}；</span>
            <span>name={{configure.name}}；</span>
        </div>
        <div class="sub-action-container">
            <slot></slot>
        </div>
    </div>
</template>

<script>
import '../../assets/css/spanner/basic-view.css';
import BasicView from './BasicView';

export default {
    name: 'Task',
    extends: BasicView,
    data(){
        return {
            configure:{
                retry_time:null,
                over_time:null,
                name:null
            }
        }
    },
    mounted() {
        let attrs = this.$attrs;
        this.configure = {
            retry_time:attrs.retry_time,
            over_time:attrs.over_time,
            name:attrs.name
        }
    }
};
</script>

<style scoped>
</style>
