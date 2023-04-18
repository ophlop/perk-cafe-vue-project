<template>
    <a :href="activeUrl" class="btn-box" :class="btnColor">
        <slot></slot>
    </a>
</template>

<script>

export default {
  props: {
    activeUrl: String,
    btnColor: String
  }
}
</script>

<style scoped>
.btn-box {
    width: 200px;
    height: 30px;
    /* background-color: #baaca1; */
    position: relative;
    display: flex;
    justify-content: center;
    text-align: center;
    padding-top: 10px;
    padding-bottom: 10px;
    font-size: 20px;

    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 0.3px;
    cursor: pointer;
}

.btn-dark {
    background-color: #3d4549;
    color: #fff;

}

.btn-light {
    background-color: #baaca1;
    color: #3d4549;
}

.btn-box:hover {
    color: #ffffff;
}
</style>
