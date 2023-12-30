<template>
<div>
    <button @click="Incremented">Clicked {{ count }} times</button>
</div>
</template>

<script>
import CounterMix from '../mixins/counter'
export default {
    name:'ClickCounter',
    mixins:[CounterMix]
}
</script>

<style>
</style>