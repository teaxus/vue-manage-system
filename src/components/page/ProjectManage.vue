<template>
    <div>
        <ts-project
            project_name="demo_project"
            db_drive="UTDB.DBDrive.DriveSqlite"
            browser="Firefox"
        >
            <task retry_time="3" over_time="10" name="main">
                <value
                    goto-tag-name="xxxxxxxxxxxxxxxxx"
                    id="1599214282860055"
                    name="ba"
                    val="sssssssss"
                />
                <storage id="1599214282860110" name="kkkkkk" val="\{\{ba\}\}" />
                <storage id="1599214282860151" name="fffffff" val="hahahaha" />

                <value id="1599214282860181" name="sbsb" val="@return">
                    <storage id="1599214282860208" name="kkkkkk" />
                </value>

                <value id="1599214282860241" name="key" val="@return">
                    <ex-module
                        id="1599214282860267"
                        input-val="\{\{sbsb\}\}"
                        name="md5"
                        val="@input"
                    />
                </value>
                <storage id="1599214282860296" name="fffffff" val="\{\{key\}\}" />
                <value id="1599214282860322" name="sbsbddd" val="@return">
                    <storage id="1599214282860346" name="fffffff" />
                </value>
            </task>
        </ts-project>

        <br />
        <br />
        <br />

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
        </ts-project>-->
        <!--ts-project 标签外部 -->
        <div>
            <!--ts-project 菜单栏 -->
            <div>
                <div>project_name=demo_project</div>
                <div>db_drive=UTDB.DBDrive.DriveSqlite</div>
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
import ProjectView from '../spanner/ProjectView';
import Task from '../spanner/Task';
import Var from '../spanner/action/Var';
import Storage from '../spanner/action/Storage';
import ExModule from '../spanner/action/ExModule';

export default {
    data: function () {
        return {};
    },
    components: {
        'ts-project': ProjectView,
        "task": Task,
        "value": Var,
        "storage": Storage,
        "ex-module": ExModule
    }
};
</script>

<style scoped>
</style>

