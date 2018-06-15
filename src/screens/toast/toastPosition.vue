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
        <nb-title>Toast Position</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-content padder>
      <nb-button
        :style="stylesObj.mb20"
        :on-press="handleBtnPress1">
        <nb-text>Top Toast</nb-text>
      </nb-button>
      <nb-button
        :style="stylesObj.mb20"
        :on-press="handleBtnPress2">
        <nb-text>Bottom Toast</nb-text>
      </nb-button>
    </nb-content>
  </nb-container>
</template>

<script>
// import React from 'react'
import { Toast } from 'native-base'

export default {
  data: function () {
    return {
      stylesObj: {
        mb20: {
          marginBottom: 20
        }
      }
    }
  },
  methods: {
    handleBtnPress1: function () {
      Toast.show({
        text: 'Wrong password!',
        buttonText: 'Okay',
        position: 'top'
      })
    },
    handleBtnPress2: function () {
      Toast.show({
        text: 'Wrong password!',
        buttonText: 'Okay',
        position: 'bottom'
      })
    }
  }
}
</script>
