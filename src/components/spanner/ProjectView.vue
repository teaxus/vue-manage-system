<template>
    <div>
        <div class="basic-container">
            <div>这个地方是标题栏</div>
            <div>这个地方是装子元素</div>
        </div>

        <div class="basic-container" style="background-color:green">
            <ActionView >
                lllll
            </ActionView>
        </div>





<!-- demo------Begin -->
<!-- <ts-project project_name="demo_project" db_drive="UTDB.DBDrive.DriveSqlite" browser="Firefox">
    <task retry_time="3" over_time="10" name="main">
        <var name="ba" val="sssssssss" goto-tag-name="xxxxxxxxxxxxxxxxx"/>
        <storage name="kkkkkk" val="{{ba}}" />
        <storage name="fffffff" val="hahahaha" />

        <var name="sbsb">
            <storage name="kkkkkk" />
        </var>

        <var.ex-module name="key" ex-module-input-val="{{sbsb}}" ex-module-name="md5" />
        <storage name="fffffff" val="{{key}}"/>
        <var name="sbsbddd">
            <storage name="fffffff"/>
        </var>
        
        <add-row-data>
            <save column="title" val="{{sbsb}}" />
            <save column="ddd" val="{{sbsbddd}}" />
        </add-row-data>
        <wait-sleep sec="1" />
        <goto tag="xxxxxxxxxxxxxxxxx" />
    </task>
</ts-project> -->


<!--ts-project 标签外部 -->
<div>
    <!--ts-project 菜单栏 -->
    <div>
        <div>project_name=demo_project</div>
        <div> db_drive=UTDB.DBDrive.DriveSqlite</div>
        <div>browser=Firefox</div>
    </div>
    <!--ts-project 子标签的容器 -->
    <div>

        <!-- task标签外部 -->
        <div>
            <!--task 菜单栏 -->
            <div>
                <div>retry_time=3</div>
                <div>over_time=0</div>
                <div>name=main</div>
            </div>
            <!--task 子标签的容器 -->
            <div>
                <!-- var 标签外部 -->
                <div>
                    <!--var 菜单栏 -->
                    <div>
                        <div>name="ba"</div>
                        <div>val="sssssssss"</div>
                        <div>goto-tag-name="xxxxxxxxxxxxxxxxx"</div>
                    </div>
                    <!--var 子标签的容器 -->
                    <div></div>
                </div>

            

                <!-- storage 标签外部 -->
                <div>
                    <!--storage 菜单栏 -->
                    <div>
                        <div>name="kkkkkk"</div>
                        <div>val="ba"</div>
                    </div>
                    <!--storage 子标签的容器 -->
                    <div></div>
                </div>
            </div>
        </div>


    </div>
</div>


<!-- demo------End -->











    </div>
</template>

<script>
import '../../assets/css/spanner/basic-view.css';
import BasicView from './BasicView';
import ActionView from './ActionView';

export default {
    name: 'ProjectView',
    extends: BasicView,
    components: {
        ActionView
    },
    mounted() {
        console.log('project view');
    }
};
</script>

<style scoped>
</style>
