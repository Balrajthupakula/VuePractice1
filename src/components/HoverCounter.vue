<template>
    <div>
        <h3 @mouseover="Incremented">Hover {{ count }} times</h3>
    </div>
    </template>
    
    <script>
    import CounterMix from '../mixins/counter'
    export default {
        name:'HoverCounter',
        mixins:[CounterMix]

    }
    </script>
    
    <style>
    </style>