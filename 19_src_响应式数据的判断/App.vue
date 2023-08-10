<template>
    <h3>我是App组件</h3>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import { ref, reactive, toRefs, readonly, isRef, isReactive, isReadonly, isProxy } from 'vue'
export default {
    name: 'App',
    setup() {
        let car1 = reactive({ name: '奔驰', price: '40W' })
        let sum = ref(0)
        let car2 = readonly(car1)

        console.log(isRef(sum))
        console.log(isReactive(car1))
        console.log(isReadonly(car2))
        console.log(isProxy(car1))
        console.log(isProxy(car2))
        console.log(isProxy(sum))
    }
}
</script>