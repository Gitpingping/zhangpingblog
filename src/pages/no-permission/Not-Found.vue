<script lang="ts">
import { defineComponent, onMounted, inject } from 'vue';
import { useRouter, Router } from 'vue-router';
export default defineComponent({

    setup() {
        const router:Router = useRouter();
        function backToIndex():void{
            router.replace('/')
        }
        return {
            backToIndex
        }
    }
})
</script>
<template>
    <div class="not-found">
        <div class="logo-btn">
            <img src="@/images/404.png" class="img-404" />
            <br />
            <p class="tips">抱歉，你访问的页面不存在</p>
            <n-button class="back-to-index" type="warning" round @click="backToIndex">返回首页</n-button>
        </div>
    </div>
</template>

<style lang="less" scoped>
@import url("@/styles/no-permission/Not-Found.less");
</style>