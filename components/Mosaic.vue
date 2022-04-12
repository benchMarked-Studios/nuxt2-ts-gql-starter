<template>
  <div class="image-mosaic">
    <img
      class="card border-t-4 border-l-4"
      width="135px"
      height="191px"
      src="~assets/images/profile_upper_left.png"
    />

    <img
      class="card z-10 border-t-4"
      width="209px"
      height="213px"
      src="~assets/images/profile_center.png"
    />

    <img
      class="card border-t-4 border-r-4"
      width="192px"
      height="108px"
      src="~assets/images/profile_upper_right.png"
    />

    <img
      class="card border-b-4 border-l-4"
      width="151px"
      height="110px"
      src="~assets/images/profile_lower_left.png"
    />

    <img
      class="card border-b-4 mt-1"
      width="191px"
      height="110px"
      src="~assets/images/profile_center_lower.png"
    />

    <img
      class="card -mt-20 border-b-4 border-r-4"
      width="195px"
      height="191px"
      src="~assets/images/profile_lower_right.png"
    />
  </div>
</template>

<script lang="ts" setup>
export default {
  name: 'Mosaic',
}
</script>

<style scoped>
.image-mosaic {
  display: grid;
  gap: 0rem;
  grid-template-columns: 135px 209px 192px;
  grid-template-rows: 191px 117px;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #353535;
  font-size: 3rem;
  color: #fff;
  border-radius: 4px;
  transition: all 500ms;
  overflow: hidden;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
}

@media (max-width: 640px) {
  .image-mosaic {
    display: none;
  }
}
</style>
