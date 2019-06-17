<template>
  <!-- <baidu-map class="map" :center="{lng: 101.8037500000, lat: 36.5983200000}" :zoom="15" :scroll-wheel-zoom="true">
    <bm-marker  :center="{lng: 101.8037500000, lat: 36.5983200000}" :position="markerPoint" :dragging="true" animation="BMAP_ANIMATION_BOUNCE">
      <bm-info-window>西宁君博科技有限公司</bm-info-window>
    </bm-marker>
  </baidu-map> -->

  <baidu-map class="map" :center="{lng: 101.8037500000, lat: 36.5983200000}" :zoom="15" :scroll-wheel-zoom="true">
    <bm-marker :center="{lng: 101.8037500000, lat: 36.5983200000}" :dragging="true" animation="BMAP_ANIMATION_BOUNCE">
      <bm-label content="我爱北京天安门" :labelStyle="{color: 'red', fontSize : '24px'}" :offset="{width: -35, height: 30}"/>
    </bm-marker>
  </baidu-map>
</template>
  
<script>
import BaiduMap  from 'vue-baidu-map/components/map/Map.vue'

export default {
  components: {
    BaiduMap
  },
  data () {
    return {
    }
  }
}
</script>
<style scoped lang='less'>
  
</style>