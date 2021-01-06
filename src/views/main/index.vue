<template>
    <div class="main-box">
        <el-container>
            <el-aside width="200px">
                <!--左侧顶部-->
                <div class="title-wrapper">
                    <img src="../../assets/mi-logo.png">
                    <span>crm的管理系统</span>
                </div>
                <!--侧边导航栏-->
                <!--active默认高亮   只有当为el-menu-item时有效-->
                <el-scrollbar class="scrollerbar">
                    <el-menu
                            default-active="1"
                            class="el-menu-vertical-demo"
                    >
                        <!--不能展开  里面没内容-->
                        <el-menu-item index="1">
                            <i class="el-icon-menu"></i>
                            <span slot="title">系统首页</span>
                        </el-menu-item>
                        <!--表示的是导航   可以展开-->
                        <el-submenu index="2">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>商品相关</span>
                            </template>

                            <el-menu-item index="2-1">
                                <i class="el-icon-menu"></i>
                                <span slot="title">品牌管理</span>
                            </el-menu-item>

                            <el-menu-item index="2-2">
                                <i class="el-icon-menu"></i>
                                <span slot="title">分类管理</span>
                            </el-menu-item>

                            <el-menu-item index="2-3">
                                <i class="el-icon-menu"></i>
                                <span slot="title">商品管理</span>
                            </el-menu-item>
                        </el-submenu>

                        <el-menu-item index="3">
                            <i class="el-icon-menu"></i>
                            <span slot="title">运营商管理</span>
                        </el-menu-item>
                    </el-menu>
                </el-scrollbar>
            </el-aside>
            <el-container>
                <el-header>主界面</el-header>
                <el-main>
                    <div class="main-body">
                        <router-view/>
                    </div>
                </el-main>
            </el-container>
        </el-container>
    </div>
</template>

<script>
import obj from "@/views/main/index";
export default obj;
</script>

<style lang="less">
   @import "index";
</style>