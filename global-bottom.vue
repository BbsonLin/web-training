<script setup lang="ts">
/**
 * Properties:
 * - growSize: number
 * - growX: number - percent
 * - growY: number - percent
 * - growFollow: boolean - follow mouse, false to completely disable
 */
// @ts-expect-error missing types
import { currentRoute } from '@slidev/client/logic/nav.ts'
import { useMouse } from '@vueuse/core'
import { computed, onMounted, ref, watchEffect } from 'vue'

const { x, y } = useMouse()
// const { idle } = useIdle(2000)
const pressed = ref(false)
const scaleFactor = computed(() => pressed.value ? 0.4 : 1)
const formatter = computed(() => (currentRoute.value.meta?.slide as any)?.frontmatter || {})

const container = ref<HTMLDivElement>()

onMounted(() => {
  container.value = document.querySelector('#slide-container')
})

// useEventListener('click', (e) => {
//   if (formatter.value.growFollow != null)
//     return
//   const path = e.composedPath() as HTMLElement[]
//   if (!path.find(el => el.id === 'slide-container'))
//     return
//   const el = path.find(el => ['A', 'BUTTON', 'IMG', 'VIDEO'].includes(el.tagName?.toUpperCase()))
//   if (!el)
//     pressed.value = true
// })
// whenever(idle, () => {
//   pressed.value = false
// })
// onKeyDown('Escape', () => {
//   pressed.value = false
// })

const mouseX = computed(() => {
  if (!container.value)
    return 0
  return ((x.value - container.value.offsetLeft) / container.value.clientWidth) * 100
})

const mouseY = computed(() => {
  if (!container.value)
    return 0
  return ((y.value - container.value.offsetTop) / container.value.clientHeight) * 100
})

const size = computed(() => 520 * +(formatter.value.growSize || 1) * scaleFactor.value)
const blur = computed(() => 140 * +(formatter.value.growSize || 1) * scaleFactor.value)
const followMouse = computed(() => formatter.value.growFollow || pressed.value)
const left = computed(() => (followMouse.value ? mouseX.value : formatter.value.growX ?? '80'))
const top = computed(() => (followMouse.value ? mouseY.value : formatter.value.growY ?? '30'))

const transitionClass = ref('')
function updateClass() {
  transitionClass.value = followMouse.value ? '' : 'transition-all duration-600 ease-in-out'
}

watchEffect(() => {
  if (!followMouse.value)
    updateClass()
})
</script>

<!-- <style>
.bg-adlink {
  background-image: url("/adlink-bg.png") linear-gradient(to right, rgb(248, 113, 113) 0%, rgb(127, 29, 29) 100%);
  background-position: right;
  background-repeat: no-repeat;
  background-size: 480px 640px;
}
</style> -->

<template>
  <span
    absolute pointer-events-none rounded-full z--1
    bg-gradient-to-r from-red to-red-900
    op75 dark:op50
    class="bg-adlink"
    :class="transitionClass"
    :style="{
      top: `${top}%`,
      left: `${left}%`,
      width: `${size}px`,
      height: `${size}px`,
      transform: 'translate(-50%, -50%)',
      filter: `blur(${blur}px)`,
    }"
    @transitionend="updateClass"
  />
</template>


