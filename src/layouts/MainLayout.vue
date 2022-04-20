<template>
  <q-layout view="hhh lpR fff">
    <q-header style="height:100px;" bordered class="bg-transparent text-white">
      <q-toolbar>
        <q-toolbar-title>
          <div class="q-mt-lg fit row no-wrap justify-center items-center content-start">
            <div>
              <img src="https://xtrm.foxthemes.me/wp-content/uploads/2018/09/white.png">
            </div>
     
          <div class="" v-for="select in selects" :key="select">
<div class="fit row no-wrap justify-center items-center content-start">
    <q-btn-dropdown color="transparent" unelevated  :label='select.label' >
      <q-list>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>{{select.name}}</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>{{select.fname}}</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>{{select.namef}}</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-btn-dropdown>
</div>
  </div>


          </div>
             </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer bordered class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          <div>Title</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>
<script>
export default {
  data () {
    return {
      onItemClick () {
        // console.log('Clicked on an Item')
      },
      selects: [
        
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'HOME' },
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'PAGES' },
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'SHOWCASES' },
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'BLOG' },
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'SHOP' },
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'PRICING' },
        {name: 'MOUNTAIN BIKING', fname: 'SNOWBOARDING', namef: 'TRAIL RUNNING', label:'CONTACT US' }

      ]
    }
  }
}
</script>
