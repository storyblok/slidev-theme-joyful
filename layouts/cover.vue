<template>
  <div class="slidev-layout cover relative">
    <TheHeader />
    <div class="my-auto">
      <slot></slot>
    </div>
  </div>
</template>

<style>
.slidev-layout.cover h1 {
  font-weight: 600;
}
</style>
