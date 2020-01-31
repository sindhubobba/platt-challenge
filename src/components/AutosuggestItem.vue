<template>
    <div @keydown="onKey">
        {{item}}
    </div>
</template>
<script>
export default {
    name: "AutosuggestItem",
    props:{
        item: String
    },
    methods:{
        onKey(){
            console.log('key event')
        }
    }
}
</script>