<template>
<!-- It's a V-bind . use v-bind or only : -->
 <!--<button v-bind:style="{background: color}" class="btn">{{text}}</button>-->
    <button :style="{background: color}" class="btn">{{text}}</button>
</template>
<script>
export default {
    name:'Button',
    props:{
        text:String,
        color:String
    }

}
</script>