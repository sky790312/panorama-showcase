<template>
  <a-entity>
    <a-image
      :src="panorama.imageSrc"
      :width="vThumbnail.imageWidth"
      :height="vThumbnail.imageHeight"
      :position="vThumbnail.imagePosition">
    </a-image>
    <a-plane
      :position="vThumbnail.planePosition"
      :color="vThumbnail.planeColor"
      :width="vThumbnail.planeWidth">
      <a-text
        :value="panorama.title"
        :width="vThumbnail.textSize"
        :color="vThumbnail.textColor"
        :position="vThumbnail.textPosition">
      </a-text>
    </a-plane>
  </a-entity>
</template>

<script>

export default {
  name: 'VThumbnail',

  props: {
    panorama: {
      type: Object,
      default () {
        return {}
      }
    }
  },

  data () {
    return {
      vThumbnail: {
        imageWidth: 7,
        imageHeight: 7,
        imagePosition: '0 0 45',
        planePosition: '0 -4 45',
        planeColor: '#000',
        planeWidth: '7',
        textColor: '#fff',
        textSize: 20,
        textPosition: '-2.2 .1 0'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '../../css/variables'

</style>
