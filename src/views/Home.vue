<template>
  <div class="home">
<l-map
v-model="zoom"
v-model:zoom="zoom"
:center="[48.856614, 2.3522219]"
>
<l-tile-layer
url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
></l-tile-layer>
<l-marker :lat-lng="[48.856614, 2.3522219]">
<l-icon icon-url='https://static-cdn.jtvnw.net/emoticons/v1/301980461/2.0'  :icon-size="[56, 56]" />
</l-marker>
      
</l-map>
  </div>
</template>

<script >
import { LMap, LTileLayer, LMarker } from "@vue-leaflet/vue-leaflet";
import { ref } from 'vue'

export default {
    name: 'Home',
    components: {
        LMap,
        LTileLayer,
        LMarker,
    },
    setup() {
        const zoom = ref(5);
        return {
            zoom,
        }
    }
}
</script>

<style scoped>
.home{ 
    width: 100%;
    height: 100%;
    overflow: hidden;
}

</style>
