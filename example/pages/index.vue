<template>
  <div>
      <u-banner/>
      <u-section title="CORONAVIRUS UPDATE">
          <p class="corona_virus_warning">CBS remains open and are working hard to provide essential services to our telecommunications and electricity industries during these difficult and uncertain times. We want to assure you that we are taking the current situation very seriously, we have staff working from home where possible and have implemented extra precautions throughout the building to ensure the health and safety of our staff, customers and suppliers. As you will be aware, the situation is constantly changing, as is the advice issued by the Government and the World Health Organisation. As a company, we will be listening to the official advice and will act in accordance with it, together with reacting to the situations of both our customers and suppliers, many of which are already operating at reduced levels. Our business may be disrupted at some point in the future but, for now, it is business as usual.

Our thoughts are with those who have been affected by the spread of COVID-19. Please, follow the advise issued by the Government and W.H.O. Stay Safe.</p>
      </u-section>
      <u-section title="PRODUCTS" class="layout">
       <u-tabs>
                <u-tab title="Tab1">1123</u-tab>
                <u-tab title="Tab2">1123</u-tab>
        </u-tabs>
      </u-section>
  </div>
</template>

<script>
import SFirstMenu from '~/components/index/s-first-menu.vue'

export default {
    components: {
        SFirstMenu
    },
    data() {
        return {
            link: 'https://www.baidu.com'
        }
    }
}
</script>


<style lang="scss" scoped>
.g-index {
    height: 360px;
    background-image: url('https://p.qpic.cn/zckj/0/3e5401081932e825a927a087c87dab891521104527794/0');
    background-size: contain;
}

.corona_virus_warning {
    padding-left: 10px;
    padding-right: 10px;
}
</style>
