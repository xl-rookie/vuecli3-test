<template>
    <div>
        <router-link class="ys1" to="/A">转向A页面</router-link>
        <router-link class="ys1" to="/B">转向B页面</router-link>
        <router-view/>
    </div>

</template>

<script>

</script>

<style>
    @import "../../public/ys1.css";
    /*全局样式 */
    a{
        color: green;
        font-size: 30px;


    }
    /*局部样式*/
    .ys2{
        color: red;
        font-size: 40px;
    }
</style>