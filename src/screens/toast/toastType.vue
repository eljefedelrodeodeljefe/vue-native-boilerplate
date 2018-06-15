<template>
  <nb-container>
    <nb-header has-tabs>
      <nb-left>
        <nb-button
          transparent
          :on-press="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Toast Type</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-content padder>
      <nb-button
        :style="stylesObj.mb15"
        :on-press="handleBtnPress1">
        <nb-text>Default Toast</nb-text>
      </nb-button>
      <nb-button
        :style="stylesObj.mb15"
        :on-press="handleBtnPress2">
        <nb-text>Success Toast</nb-text>
      </nb-button>
      <nb-button
        :style="stylesObj.mb15"
        :on-press="handleBtnPress3">
        <nb-text>Warning Toast</nb-text>
      </nb-button>
      <nb-button
        :style="stylesObj.mb15"
        :on-press="handleBtnPress4">
        <nb-text>Danger Toast</nb-text>
      </nb-button>
    </nb-content>
  </nb-container>
</template>

<script>
import { Toast } from 'native-base'

export default {
  data: function () {
    return {
      stylesObj: {
        mb15: {
          marginBottom: 15
        }
      }
    }
  },
  methods: {
    handleBtnPress1: function () {
      Toast.show({
        text: 'Wrong password!',
        buttonText: 'Okay'
      })
    },
    handleBtnPress2: function () {
      Toast.show({
        text: 'Wrong password!',
        buttonText: 'Okay',
        type: 'success'
      })
    },
    handleBtnPress3: function () {
      Toast.show({
        text: 'Wrong password!',
        buttonText: 'Okay',
        type: 'warning'
      })
    },
    handleBtnPress4: function () {
      Toast.show({
        text: 'Wrong password!',
        buttonText: 'Okay',
        type: 'danger'
      })
    }
  }
}
</script>
