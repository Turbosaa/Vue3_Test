<template>
    <div class="son">
        <h3>我是Son组件（孙），{{ car.name }}--{{ car.price }}W</h3>
        <button @click="car.price++">修改price</button>
    </div>
</template>

<script>
import { inject } from 'vue'
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Son',
    setup() {
        let car = inject('car')
        return { car }
    }
}
</script>

<style>
.son {
    background-color: orange;
    padding: 10px;
}
</style>