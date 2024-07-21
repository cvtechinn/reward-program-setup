<template>
    <div :class="['panel', { 'panel--open': isOpen }]">
      <button class="close-btn" @click="togglePanel">Close</button>
      <div class="panel-content">
        <slot></slot>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SlideoutPanel',
    props: {
      isOpen: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      togglePanel() {
        this.$emit('toggle');
      }
    }
  }
  </script>
  
  <style scoped>
  .panel {
    position: fixed;
    top: 0;
    right: -300px;
    width: 300px;
    height: 100%;
    background-color: white;
    box-shadow: -2px 0 5px rgba(0, 0, 0, 0.5);
    transition: right 0.3s ease;
    z-index: 1000;
  }
  .panel--open {
    right: 0;
  }
  .close-btn {
    position: absolute;
    top: 10px;
    left: 10px;
    background: none;
    border: none;
    font-size: 18px;
    cursor: pointer;
  }
  .panel-content {
    padding: 20px;
    justify-content: left;
  }
  </style>
  