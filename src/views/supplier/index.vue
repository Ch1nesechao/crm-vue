<template>
    <div class="supplier-box">
        <!--操作部分-->
        <div class="execute-box">
            <!--
                size:大小
                type:颜色
                plain:镂空
                round:圆角
                loading:加载
            -->
            <el-button-group>
                <el-button type="danger" icon="el-icon-edit" size="mini">新建</el-button>
                <el-button type="danger" icon="el-icon-delete" size="mini">删除</el-button>
            </el-button-group>
        </div>
        <!--查询部分-->
        <div class="search-box">
            <el-form :inline="true" :model="formInline" class="demo-form-inline">
                <el-form-item label="审批人">
                    <el-input v-model="formInline.user" placeholder="审批人" size="mini"></el-input>
                </el-form-item>
                <el-form-item label="活动区域">
                    <el-select v-model="formInline.region" placeholder="活动区域" size="mini">
                        <el-option label="区域一" value="shanghai" ></el-option>
                        <el-option label="区域二" value="beijing"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item>
                    <el-button type="primary" size="mini">查询</el-button>
                </el-form-item>
            </el-form>
        </div>
        <!--表格部分-->
        <div class="table-box">
            <el-table
                    :data="tableData"
                    border
                    tooltip-effect="dark"
                    style="width: 100%">
                <el-table-column
                        type="selection"
                        align="center"
                        width="55">
                </el-table-column>
                <el-table-column
                        prop="date"
                        label="日期"
                        align="center"
                        width="180">
                    <!--width不加px  不写则均分剩余的宽度-->
                </el-table-column>
                <el-table-column
                        prop="name"
                        label="姓名"
                        align="center"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="address"
                        align="center"
                        label="地址"
                        show-overflow-tooltip
                >
                </el-table-column>
                <el-table-column
                        align="center"
                        label="操作"
                >
                    <template>
                        <!--这种方式是可以展示的-->
                        <el-button type="primary" size="mini">编辑</el-button>
                        <el-button type="danger" size="mini">删除</el-button>
                    </template>
                </el-table-column>
            </el-table>
        </div>
        <!--页码部分-->
        <div class="page-box">
            <el-pagination
                    background
                    layout="prev, pager, next"
                    page-size="5"
                    current-page="1"
                    align="center"
                    :total="1000">
            </el-pagination>
        </div>
    </div>
</template>

<script>
    import obj from "@/views/supplier/index";
    export default obj;
</script>

<style lang="less">
@import "index";
</style>