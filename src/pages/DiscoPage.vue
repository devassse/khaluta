<template>
  <header class="top-grid">
    <div class="gallery">
      <img src="../assets/imgs/clouds.png" alt="" srcset="">
      <img src="../assets/imgs/clouds.png" alt="" srcset="">
      <img src="../assets/imgs/clouds.png" alt="" srcset="">
      <img src="../assets/imgs/clouds.png" alt="" srcset="">
      <img src="../assets/imgs/clouds.png" alt="" srcset="">
    </div>
    <div class="check-in">
      <div class="pass-desc">
        <span>Passe semanal - 3x por Semana</span>
        <span>300Mt/dia (6hrs)</span>
      </div>
      <div class="pass-price">
        <span>900Mt/Semana (18hrs)</span>
      </div>
    </div>
  </header>
  <main>
    <section class="main-container">

    </section>
  </main>
</template>

<script>
export default {
  setup() {
    return {

    }
  }
}
</script>
<style scoped>
.top-grid {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0.8rem;
}

.gallery img {
  width: 100%;
  height: auto;
}

.gallery img:first-of-type {
  grid-column: 1/ span 2;
  grid-row: 1/span 2;
}

.check-in {
  padding: 1.2rem;
  border-radius: 15px;
  background-color: #fff;
  display: flex;
  gap: 6rem;
  justify-content: space-between;
  box-shadow: rgb(0 0 0 / 10%) 0px 4px 6px -1px, rgb(0 0 0 / 6%) 0px 2px 4px -1px;
  position: absolute;
  bottom: -35px;
  cursor: pointer;
  transition: all .1s;
}

.check-in:hover {
  box-shadow: rgb(0 0 0 / 10%) 0px 6px 8px -1px, rgb(0 0 0 / 6%) 0px 6px 8px -1px;
  background-color: #ccc;
  border: 4px inset #fff;
}

.pass-desc {
  display: flex;
  flex-direction: column;
}

.main-container {
  width: 60%;
  margin: 3rem auto;


  border: 1px dotted red;
  height: 600px;
}
</style>
