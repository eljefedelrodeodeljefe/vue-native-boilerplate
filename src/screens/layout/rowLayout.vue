<template>
  <nb-container>
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
        <nb-title>Row Grid</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>
    <nb-grid>
      <nb-row :style="{ backgroundColor: '#635DB7' }"/>
      <nb-row :style="{ backgroundColor: '#00CE9F' }"/>
    </nb-grid>
  </nb-container>
</template>
