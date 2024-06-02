<template>
    <li class="border">
        <img src="https://cdn-icons-png.flaticon.com/512/16470/16470858.png" alt="" width="150" height="150">
        <slot name="header-Card"></slot>
        <slot name="content-Card"></slot>
    </li>
</template>

<script>
export default {
    name: "CustomCard"
}
</script>

<style>

</style>