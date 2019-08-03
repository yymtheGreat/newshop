<template>
  <el-container class="bigbox">
    <el-header class="topbox">
        <el-row>
            <el-col :span="4"><div class="grid-content bg-purple">1</div></el-col>
            <el-col :span="16"><div class="grid-content bg-purple-light">2</div></el-col>
            <el-col :span="4"><div class="grid-content bg-purple"></div><a href="#" class="out">退出</a></el-col>
        </el-row>
    </el-header>
    <el-container>
        <el-aside width="200px" class="lfbox">Aside</el-aside>
        <el-main class="rtbox">Main</el-main>
    </el-container>
  </el-container>
</template>
<style scoped>
    .bigbox{ 
        background-color: red;
        height: 100%;
    }
    .lfbox{
        background-color: green;
    }
    .rtbox{
        background-color: blue
    }
    .out {
        line-height: 60px;
        text-decoration: none;
    }
</style>
