<template>
  <!-- It's a V-bind . use v-bind or only : -->
  <!--<button v-bind:style="{background: color}" class="btn">{{text}}</button>-->
  <!--v-on:click="onClick()"   and  @click="onClick()" BOTH ARE SAME -->
  <button @click="onClick()"
   :style="{ background: color }"
   class="btn">{{ text }}</button>
</template>
<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  methods:{                  // Functions will be in the method ,
      onClick(){             // ex:  ON button click what will happen we will control it from here.
          console.log('Clicked')
      }

                       
  }
};
</script>