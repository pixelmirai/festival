

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const cube = ref(null);
const isDragging = ref(false);
const startX = ref(0);
const startY = ref(0);
const currentX = ref(0);
const currentY = ref(0);
const rotationX = ref(0);
const rotationY = ref(0);
const spinning = ref(true);
let spinInterval = null;
let inactivityTimeout = null;

const onMouseDown = (event) => {
  startDrag(event.clientX, event.clientY);
  document.addEventListener('mousemove', onMouseMove);
  document.addEventListener('mouseup', onMouseUp);
};

const onMouseMove = (event) => {
  handleDrag(event.clientX, event.clientY);
};

const onMouseUp = () => {
  endDrag();
  document.removeEventListener('mousemove', onMouseMove);
  document.removeEventListener('mouseup', onMouseUp);
};

const onTouchStart = (event) => {
  const touch = event.touches[0];
  startDrag(touch.clientX, touch.clientY);
  document.addEventListener('touchmove', onTouchMove);
  document.addEventListener('touchend', onTouchEnd);
};

const onTouchMove = (event) => {
  const touch = event.touches[0];
  handleDrag(touch.clientX, touch.clientY);
};

const onTouchEnd = () => {
  endDrag();
  document.removeEventListener('touchmove', onTouchMove);
  document.removeEventListener('touchend', onTouchEnd);
};

const startDrag = (clientX, clientY) => {
  clearTimeout(inactivityTimeout);
  clearInterval(spinInterval);
  spinning.value = false;
  isDragging.value = true;
  startX.value = clientX - currentX.value;
  startY.value = clientY - currentY.value;
};

const handleDrag = (clientX, clientY) => {
  if (!isDragging.value) return;
  currentX.value = clientX - startX.value;
  currentY.value = clientY - startY.value;
  rotationY.value = currentX.value / 2;
  rotationX.value = -currentY.value / 2;
  updateCubeRotation();
};

const endDrag = () => {
  isDragging.value = false;
  startInactivityTimer();
};

const updateCubeRotation = () => {
  cube.value.style.transform = `rotateX(${rotationX.value}deg) rotateY(${rotationY.value}deg)`;
};

const startInactivityTimer = () => {
  inactivityTimeout = setTimeout(() => {
    spinning.value = true;
    startSpinning();
  }, 10); // 3 seconds of inactivity before spinning resumes
};

const startSpinning = () => {
  spinInterval = setInterval(() => {
    if (!spinning.value) return;
    rotationX.value += 0.5;
    rotationY.value += 1;
    updateCubeRotation();
  }, 50); // Adjust the interval for desired spinning speed
};

onMounted(() => {
  startSpinning();
});

onBeforeUnmount(() => {
  clearTimeout(inactivityTimeout);
  clearInterval(spinInterval);
  document.removeEventListener('mousemove', onMouseMove);
  document.removeEventListener('mouseup', onMouseUp);
  document.removeEventListener('touchmove', onTouchMove);
  document.removeEventListener('touchend', onTouchEnd);
});
</script>

<template>
  <div class="scene">
    <div class="cube" ref="cube" @mousedown="onMouseDown" @touchstart="onTouchStart">
      <div class="face front">Front</div>
      <div class="face back">Back</div>
      <div class="face left">Left</div>
      <div class="face right">Right</div>
      <div class="face top">Top</div>
      <div class="face bottom">Bottom</div>
    </div>
  </div>
</template>

<style scoped>
.scene {
  width: 300px;
  height: 300px;
  perspective: 600px;
}

.cube {
  width: 100%;
  height: 100%;
  position: relative;
  transform-style: preserve-3d;
  cursor: grab;
  transition: transform 0.1s ease-out;
}

.cube:active {
  cursor: grabbing;
}

.face {
  position: absolute;
  width: 300px;
  height: 300px;
  background-color: rgba(255, 255, 255, 0.9);
  border: 1px solid #ccc;
  line-height: 200px;
  text-align: center;
  font-size: 24px;
  font-weight: bold;
}

.front  { transform: translateZ(100px); }
.back   { transform: rotateY(180deg) translateZ(180px); }
.left   { transform: rotateY(-90deg) translateZ(180px); }
.right  { transform: rotateY(90deg) translateZ(180px); }
.top    { transform: rotateX(90deg) translateZ(180px); }
.bottom { transform: rotateX(-90deg) translateZ(180px); }
</style>
