<template>
    <div>
        <div class="title">
            <p>a</p>
            <slot name="title"> </slot>
        </div>
        <hr>
        <div>
            <slot name="content"> </slot>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
    div {
        border: 1px sold #ccc;
        box-shadow: 1px 1px 2px black;
        margin: auto;
        text-align:center;
        padding: 50px;
    }
    p {
        color: blue;
    }
</style>