<template>
    <nav :class="[wrap, widthFull]">
        <ul v-for="elem in menu" :key="elem.title" >
            <li :class="[color]"><a :href="elem.url" :class="[color]">{{ elem.title}}</a></li>
        </ul>
    </nav>
</template>

<script>

export default {
  props: {
    menu: Array,
    wrap: String,
    width: String,
    color: String
  }
//   data () {
//     return {
//         wrapClass: 'yes'
//     }
//   }
}
</script>

<style scoped>
nav {
    display: inline-flex;
    justify-content: space-between;
    gap: 26px;
    row-gap: 0px;
}

ul {
    padding: 0;
    width: fit-content;
    height: 10px;

}

a, li {
    list-style: none;
    text-decoration: none;
    font-size: 20px;
    font-weight: 300;
}

a:hover {
    text-decoration: underline 1px;
}

.wrap {
    flex-wrap: wrap;
}

.nowrap {
    flex-wrap: nowrap;
}

.widthFull {
    width: 100%;
}

.width-50 {
    width: 50%;
}

.colorDark {
    color: #3d4549;
}

.colorLight {
    color: #ffffff;
}
</style>
