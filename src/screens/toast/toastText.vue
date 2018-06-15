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
        <nb-title> Toast Text Style</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-content padder>
      <nb-button :on-press="handleBtnPress">
        <nb-text>Toast</nb-text>
      </nb-button>
    </nb-content>
  </nb-container>
</template>

<script>
import { Toast } from 'native-base'

export default {
  methods: {
    handleBtnPress: function () {
      Toast.show({
        text: 'Wrong password!',
        textStyle: { color: 'yellow' },
        buttonText: 'Okay'
      })
    }
  }
}
</script>
