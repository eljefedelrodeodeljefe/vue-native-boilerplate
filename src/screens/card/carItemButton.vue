<template>
  <nb-container :style="{backgroundColor: '#fff'}">
    <nb-header>
      <nb-left>
        <nb-button
          transparent
          :on-press="() => this.props.navigation.goBack()"
        >
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Button CardItem</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-content padder>
      <nb-card
        :style="{marginBottom: 15}"
        transparent>
        <nb-card-item
          header
          button
          :on-press="handleHeaderClick">
          <nb-text>NativeBase</nb-text>
        </nb-card-item>

        <nb-card-item
          button
          :on-press="handleBodyClick">
          <nb-body>
            <nb-text>Click on any carditem.</nb-text>
          </nb-body>
        </nb-card-item>

        <nb-card-item
          footer
          button
          :on-press="handleFooterClick">
          <nb-text>GeekyAnts</nb-text>
        </nb-card-item>
      </nb-card>
    </nb-content>
  </nb-container>
</template>

<script>
export default {
  methods: {
    handleHeaderClick: function () {
      alert('This is Card Header')
    },
    handleBodyClick: function () {
      alert('This is Card Body')
    },
    handleFooterClick: function () {
      alert('This is Card Footer')
    }
  }
}
</script>
