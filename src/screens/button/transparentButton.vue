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
        <nb-title>Transparent Button</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-content
      padder
      class="content-wrapper">
      <nb-button
        transparent
        light
        :style="{marginBottom: 20}">
        <nb-text>Light</nb-text>
      </nb-button>
      <nb-button
        transparent
        info
        :style="{marginBottom: 20}">
        <nb-text>Info</nb-text>
      </nb-button>
      <nb-button
        transparent
        primary
        :style="{marginBottom: 20}">
        <nb-text>Primary</nb-text>
      </nb-button>
      <nb-button
        transparent
        success
        :style="{marginBottom: 20}">
        <nb-text>Success</nb-text>
      </nb-button>
      <nb-button
        transparent
        warning
        :style="{marginBottom: 20}">
        <nb-text>Warning</nb-text>
      </nb-button>
      <nb-button
        transparent
        danger
        :style="{marginBottom: 20}">
        <nb-text>Danger</nb-text>
      </nb-button>
      <nb-button
        transparent
        dark
        :style="{marginBottom: 20}">
        <nb-text>Dark</nb-text>
      </nb-button>
    </nb-content>

  </nb-container>
</template>

<style>
.content-wrapper {
  background-color: #fff;
  padding: 20;
}
</style>
