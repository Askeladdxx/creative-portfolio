<template>
  <div class="creative-portfolio">
    <div class="navbar row justify-between q-mx-xl">
      <q-img
        class="navbar-logo q-my-lg q-mx-md"
        src="https://scontent.fmnl9-1.fna.fbcdn.net/v/t1.15752-9/358816589_962559958161259_5649692621280805571_n.png?_nc_cat=110&ccb=1-7&_nc_sid=ae9488&_nc_eui2=AeGdkrL6Ogqt72vmzmzGpAwo5TyHM5Y6kQ_lPIczljqRDxAqSbUHHqVILOsxbKVc1K2BJ6nUWqU7aF5CqdJvPRDP&_nc_ohc=V9zcfjdnu14AX_vHfil&_nc_ht=scontent.fmnl9-1.fna&oh=03_AdQ8ht69lBwLyQl9cuewDvrZKOhCbAwQHtoy70XDveXTiQ&oe=64D318C0"
      />

      <div class="flex flex-center">
        <div v-for="(navbtns, index) in navbtns" :key="index" class="q-mx-sm">
          <q-btn dense no-caps flat class="btn-navbar bg-teal q-pa-xs">
            {{ navbtns }}
          </q-btn>
        </div>
      </div>
    </div>
    <div class="body column items-center q-mt-xl">
      <div class="q-pt-lg">
        <h1 class="intro-header text-center q-mb-xl text-bold">
          Joshua Yves Edellon
        </h1>
        <h2>Creative Portfolio</h2>
      </div>
      <div class="flex flex-center">
        <div v-for="(button, index) in buttons" :key="index">
          <q-btn
            dense
            no-caps
            flat
            class="btn-category q-mx-sm bg-teal q-pa-xs"
            @click="handleButtonClick(button)"
          >
            {{ button }}
          </q-btn>
        </div>
      </div>
      <div class="home-image"></div>
    </div>
  </div>
</template>
<script src="./script/portfolio"></script>

<style lang="scss">
@import "./style/portfolio.scss";
</style>
