<template>
  <header class="top-grid">
    <div class="gallery">
      <img src="../assets/imgs/mountains.jpg" alt="" srcset="">
      <img src="../assets/imgs/mountains.jpg" alt="" srcset="">
      <img src="../assets/imgs/mountains.jpg" alt="" srcset="">
      <img src="../assets/imgs/mountains.jpg" alt="" srcset="">
      <img src="../assets/imgs/mountains.jpg" alt="" srcset="">
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
      <div class="gym-description">
        <span class="title">Ginásio Pro-Gym</span>
        <div class="status-time">
          <span class="open-status">Aberto</span>
          <span class="time-close">Fecha 22hrs</span>
        </div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque excepturi magnam voluptatibus, veritatis, eum
          odio amet magni reiciendis, iusto rerum accusantium blanditiis dolorem doloremque? Ipsa excepturi iste nisi ex
          officia?</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque excepturi magnam voluptatibus, veritatis, eum
          odio amet magni reiciendis, iusto rerum accusantium blanditiis dolorem doloremque? Ipsa excepturi iste nisi ex
          officia?</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque excepturi magnam voluptatibus, veritatis, eum
          odio amet magni reiciendis, iusto rerum accusantium blanditiis dolorem doloremque? Ipsa excepturi iste nisi ex
          officia?</p>
      </div>
      <div class="gym-time-table">
        <span class="time-table-title">Horários de funcionamento</span>
        <table class="time-table">
          <tr>
            <td>Segunda-feira</td>
            <td>das 07:00 - 22:00</td>
          </tr>
          <tr>
            <td>Sábado</td>
            <td>das 09:00 - 19:00</td>
          </tr>
          <tr>
            <td>Domingo</td>
            <td>das 09:00 - 17:00</td>
          </tr>
        </table>
      </div>
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
  display: grid;
  grid-template-columns: 60fr 40fr;
  gap: 4rem;


  border: 1px dotted red;
  height: 600px;
}
.status-time{
  margin-bottom: 2rem;
}
.title {
  font-size: 1.6rem;
  font-weight: bold;
}
.open-status{
  background-color: rgb(153, 246, 153);
  padding: 0.2rem 0.4rem;
}
.time-close {
  margin-left: 1.4rem;
  font-weight: lighter;
}

.time-table-title{
  font-size: 1.2rem;
  font-weight: bold;
}
.time-table {
  margin-top: 1.4rem;
}
</style>
