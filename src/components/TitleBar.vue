<template>
<div class="titleBar">
    <div class="title">
        <div class="logo">
            <img src="@/assets/logo.png">
        </div>
        <div class="txt">窗口标题</div>
    </div>
    <div class="windowTool">
        <div @click="minisize">
            <i class="iconfont iconminisize"></i>
        </div>
        <div v-if="isMaxSize" @click="restore">
            <i class="iconfont iconrestore"></i>
        </div>
        <div v-else @click="maxsize">
            <i class="iconfont iconmaxsize"></i>
        </div>
        <div @click="close" class="close">
            <i class="iconfont iconclose"></i>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'TitleBar'
}
</script>

<style lang="scss" scoped>
@import url(https://at.alicdn.com/t/font_1378132_s4e44adve5.css);
.titleBar {
    height: 38px;
    line-height: 36px;
    background: #fff1f0;
    display: flex;
    border-bottom: 1px solid #f5222d;
    .title {
        flex: 1;
        display: flex;
        -webkit-app-region:drag;
        .logo {
            padding-left: 8px;
            padding-right: 6px;
            img { width: 20px; height: 20px; margin-top: 7px;}
        }
        .txt {
            text-align: left;
            flex: 1;
        }
    }
    .windowTool {
        div {
            color: #888;
            height: 100%;
            width: 38px;
            display: inline-block;
            cursor: pointer;
            i { font-size: 12px;}
            &:hover { background: #ffccc7;}
        }
        .close:hover { color: #fff; background: #ff4d4f;}
    }
}
.content {
    flex: 1;
    overflow-y: auto;
    overflow-x: auto;
}
</style>