<template>
  <div class="">
    <q-layout view="hHh Lpr lff" container style="height: 100vh">
      <q-header class="bg-transparent">
        <q-toolbar class="flex-display">
          <div class="list-box" @click="drawer = !drawer">
            <q-btn flat round dense icon="list" style="color: rgba(38, 121, 191, 0.5);" />
            <q-toolbar-title class="list-box-text">Lista</q-toolbar-title>
          </div>
          <div class="search-box">
            <form>
              <input type="search" name="" id="" placeholder="Distrito, Província" autofocus class="search-input">
              <button class="search-btn"><span>
                  <svg xmlns="http://www.w3.org/2000/svg" stroke="rgba(38, 121, 191, 0.5)" fill="none"
                    viewBox="0 0 24 24" stroke-width="1.5" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round"
                      d="M15.75 15.75l-2.489-2.489m0 0a3.375 3.375 0 10-4.773-4.773 3.375 3.375 0 004.774 4.774zM21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </span>
              </button>
            </form>
          </div>
          <div class="logo-box">
            <img src="../assets/imgs/kgroup-favicon.png" alt="Khaluta Logo" srcset="">
            <span>Khaluta</span>
            <ul class="submenu">
              <li><a href="#">Baixar App</a></li>
              <li><a href="#">Contactos</a></li>
            </ul>
          </div>
        </q-toolbar>
      </q-header>

      <q-drawer v-model="drawer" :width="450" :breakpoint="600" overlay bordered class="bg-grey-3">
        <div class="close-drawer" @click="drawer = !drawer">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
            stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round"
              d="M18.75 19.5l-7.5-7.5 7.5-7.5m-6 15L5.25 12l7.5-7.5" />
          </svg>
        </div>
        <q-scroll-area class="fit">
          <q-list>
            <q-item to="/gym">
              <q-item-section>
                <div class="aside-list-item-card">
                  <div class="image-area">
                    <img src="../assets/imgs/mountains.png" alt="" srcset="">
                  </div>
                  <div class="description">
                    <div class="description-title">
                      <span class="title">Ginásio Pro-Gym</span>
                      <span class="desc">Maputo</span>
                    </div>
                    <div class="description-price">249Mt/h</div>
                  </div>
                </div>
              </q-item-section>
            </q-item>
            <q-item to="disco">
              <q-item-section>
                <div class="aside-list-item-card">
                  <div class="image-area">
                    <img src="../assets/imgs/clouds.png" alt="" srcset="">
                  </div>
                  <div class="description">
                    <div class="description-title">
                      <span class="title">Discoteca & Restaurante Malibo</span>
                      <span class="desc">Chimoio</span>
                    </div>
                    <div class="description-price">645Mt/prato</div>
                  </div>
                </div>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <div class="aside-list-item-card">
                  <div class="image-area">
                    <img src="../assets/imgs/mountains.png" alt="" srcset="">
                  </div>
                  <div class="description">
                    <div class="description-title">
                      <span class="title">Park Belas Artes</span>
                      <span class="desc">Matola</span>
                    </div>
                    <div class="description-price">95Mt/noite</div>
                  </div>
                </div>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <div class="aside-list-item-card">
                  <div class="image-area">
                    <img src="../assets/imgs/clouds.png" alt="" srcset="">
                  </div>
                  <div class="description">
                    <div class="description-title">
                      <span class="title">Ginásio Ultra</span>
                      <span class="desc">Maputo</span>
                    </div>
                    <div class="description-price">249Mt/h</div>
                  </div>
                </div>
              </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>
      </q-drawer>

      <q-page-container style="padding-top: 0;">
        <q-page>

          <div
            style="height: 100vh;background-color: #ccc;display: flex;justify-content: center;align-items: center;color: azure;">
            <!-- <iframe style="border:0;width:100%;height:100%;" loading="lazy" allowfullscreen
              referrerpolicy="no-referrer-when-downgrade" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyAt5KGgZ1MqNMZxqKpnWm-Sg4Wdn0ovgns
    &q=Space+Needle,Seattle+WA">
            </iframe> -->
            <h1 style="position:absolute;">GOOGLE MAP</h1>
          </div>
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<script>

import { ref } from 'vue'
const menuList = [
  {
    icon: 'inbox',
    label: 'Inbox',
    separator: true
  },
  {
    icon: 'send',
    label: 'Outbox',
    separator: false
  },
  {
    icon: 'delete',
    label: 'Trash',
    separator: false
  },
  {
    icon: 'error',
    label: 'Spam',
    separator: true
  },
  {
    icon: 'settings',
    label: 'Settings',
    separator: false
  },
  {
    icon: 'feedback',
    label: 'Send Feedback',
    separator: false
  },
  {
    icon: 'help',
    iconColor: 'primary',
    label: 'Help',
    separator: false
  }
]

export default {
  setup() {
    return {
      drawer: ref(true),
      menuList
    }
  }
}
</script>
<style scoped>
.flex-display {
  display: flex;
  justify-content: space-between;
}

.list-box {
  display: flex;
  align-items: center;
  background-color: rgb(216, 230, 243);
  border: 3px solid #fff;
  padding: 0.4rem 1.2rem;
  margin-top: 1rem;
  border-radius: 30px;
  cursor: pointer;
  transition: all 0.3s;
  box-shadow: rgb(0 0 0 / 10%) 0px 4px 6px -1px, rgb(0 0 0 / 6%) 0px 2px 4px -1px;
}

.list-box:hover {
  border: 3px solid rgba(38, 121, 191, 0.5);
}

.list-box:hover .list-box-text,
.q-btn:hover .q-icon:hover {
  color: rgba(38, 121, 191, 0.5) !important;
}

.q-icon,
.material-icons {
  font-size: 2.015em !important;
}

.list-box-text {
  font-size: 16px;
  font-weight: bold;
  color: rgba(38, 121, 191, 0.5);
}

.q-drawer {
  top: 0 !important;
}

.close-drawer {
  padding: 10px 15px 5px 7px;
  background-color: #eeeeee;
  position: absolute;
  top: 20px;
  right: -45px;
  border-top: 3px solid #fff;
  border-right: 3px solid #fff;
  border-bottom: 3px solid #fff;
  cursor: pointer;
  border-top-right-radius: 30px;
  border-bottom-right-radius: 30px;
}

.close-drawer svg {
  width: 20px;
  height: auto;
}

.close-drawer:hover svg {
  color: rgb(26, 75, 116);
}

.search-box {
  width: 30%;
  margin-top: 1rem;
  position: relative;
  border-radius: 25px;
  box-shadow: rgb(0 0 0 / 10%) 0px 4px 6px -1px, rgb(0 0 0 / 6%) 0px 2px 4px -1px;
}

.search-input {
  width: 100%;
  border: 1px solid transparent;
  border-radius: 25px;
  outline: none;
  padding: 11px 10px 11px 15px;
  color: rgb(26, 75, 116);
  font-weight: 500;
  border: 3px solid #fff;
  transition: all .3s;
}

.search-input:hover,
.search-input:active {
  background-color: rgb(216, 230, 243);
  border: 3px solid rgba(38, 121, 191, 0.5);
}

.search-btn {
  width: 44px;
  height: 42px;
  border: none;
  background-color: rgb(216, 230, 243);
  border-radius: 50%;
  position: absolute;
  cursor: pointer;
  right: 3px;
  top: 4px;
}

.search-btn svg {
  width: 100%;
  height: 100%;
}

.logo-box {
  display: flex;
  align-items: center;
  gap: 10px;
  background-color: #fff;
  padding: 10px 15px;
  margin-top: 0.6rem;
  border-radius: 25px;
  color: rgb(26, 75, 116);
  font-size: 1rem;
  font-weight: bold;
  position: relative;
  cursor: pointer;
  transition: all .3s;
}

.logo-box img {
  width: 30px;
}

.logo-box:hover .submenu {
  display: block;
}

.submenu {
  background-color: #fff;
  top: 2.2rem;
  position: absolute;
  padding: 5px 15px;
  list-style: none;
  display: none;
}

.submenu a {
  text-decoration: none;
  font-weight: normal;
  font-size: 0.8rem;
  color: rgb(26, 75, 116);
}

.submenu a:hover {
  text-decoration: underline;
}

/* Aside */
.q-item {
  padding: 8px !important;
}

.aside-list-item-card {
  width: 100%;
  border-radius: 10px;
  background-color: #fff;
  transition: all .3s;
  cursor: pointer;
}

.aside-list-item-card:hover {
  box-shadow: rgb(0 0 0 / 10%) 0px 4px 6px -1px, rgb(0 0 0 / 6%) 0px 2px 4px -1px;
}

.image-area img {
  width: 100%;
  height: 150px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.description {
  display: grid;
  grid-template-columns: 70fr 30fr;
  padding: 5px 10px;
}

.description-title {
  display: flex;
  flex-direction: column;
}

.description-title .title {
  font-size: 1rem;
  font-weight: 600;
}

.description-price {
  font-size: 1rem;
  font-weight: 400;
  text-align: right;
}
</style>
