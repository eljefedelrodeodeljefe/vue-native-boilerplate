<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header has-segment>
      <nb-left>
        <nb-button
          transparent
          :on-press="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-segment>
          <nb-button
            :active="seg === 1 ? true : false"
            first
            :on-press="updateSegment1"
          >
            <nb-text>Puppies</nb-text>
          </nb-button>
          <nb-button
            last
            :active="seg === 2 ? true : false"
            :on-press="updateSegment2"
          >
            <nb-text>Cubs</nb-text>
          </nb-button>
        </nb-segment>
      </nb-body>
      <nb-right>
        <nb-button transparent>
          <nb-icon name="search" />
        </nb-button>
      </nb-right>
    </nb-header>

    <nb-content padder>
      <nb-text v-if="seg===1">Puppies Selected</nb-text>
      <nb-text v-if="seg===2">Cubs Selected</nb-text>
    </nb-content>
  </nb-container>
</template>

<script>
export default {
  data: function () {
    return {
      seg: 2
    }
  },
  methods: {
    updateSegment1: function () {
      this.seg = 1
    },
    updateSegment2: function () {
      this.seg = 2
    }
  }
}
</script>
