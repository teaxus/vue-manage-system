<template>
    <div class="basic-container project-container">
        <div>
            <span>Project标签：</span>

            <span>project_name={{configure.project_name}}；</span>
            <span>db_drive={{configure.db_drive}}；</span>
            <span>browser={{configure.browser}}；</span>
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
    name: 'ProjectView',
    extends: BasicView,
    data(){
        return {
            configure:{
                project_name:null,
                db_drive:null,
                browser:null
            }
        }
    },
    mounted() {
        let attrs = this.$attrs;
        this.configure = {
            project_name:attrs.project_name,
            db_drive:attrs.db_drive,
            browser:attrs.browser
        }
    }
};
</script>

<style scoped>
.project-container{
    padding: 15px;
}
</style>
