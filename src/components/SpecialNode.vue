<script setup lang="ts">
import type { NodeProps } from '@vue-flow/core'  
import { Position } from '@vue-flow/core'

// props were passed from the slot using `v-bind="customNodeProps"`
const props = defineProps<NodeProps>()
  
console.log(props.data.hello) // 'world'
</script>

<template>
  <div class="vue-flow__node-custom">
    <Handle type="target" :position="Position.Top" />
    <div>{{ label }}</div>
    <Handle type="source" :position="Position.Bottom" />
  </div>
</template>
