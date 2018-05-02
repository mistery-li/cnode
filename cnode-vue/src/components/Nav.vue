<template>
    <ul class="footer-nav">
        <li :class="{ active: item.name == $toute.name}" v-for="(item, index) in list" :key="index">
            <router-link :to="{ name: item.name }">
                <i class="iconfont" :class="[ item.icon ]"></i>
                <span>{item.title}</span>
            </router-link>
        </li>
    </ul>
</template>

<script>
export default {
    data() {
        return {
            list: [
                {
                    title: '分享',
                    name: 'share',
                    icon: 'icon-share'
                },
                {
                    title: '提问',
                    name: 'question',
                    icon: 'icon-question'
                },
                {
                    title: '招聘',
                    name: 'hr',
                    icon: 'icon-hr'
                },
                {
                    title: '我的',
                    name: 'mine',
                    icon: 'icon-mone'
                }
            ]
        }
    }
}
</script>

<style lang="less" scoped>
    .footer-nav {
        position: absolute;
        background: #fff;
        right: 0;
        bottom: 0;
        left: 0;
        z-index: 999;
        height: 50px;
        text-align: center;
        border-top: 1px solid #ddd;
    }
</style>


