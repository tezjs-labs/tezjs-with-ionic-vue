<script>
import headerComponent from "/@/components/header.vue";
import footerComponent from "/@/components/footer.vue";
import { IonPage, IonContent } from "@ionic/vue";
export default {
  components: {
    headerComponent: headerComponent,
    footerComponent: footerComponent,
    IonPage,
    IonContent,
  },
};
</script>
<template>
  <ion-page>
    <ion-content :scroll-y="true">
      <headerComponent></headerComponent>
      <tez-slot></tez-slot>
      <footerComponent></footerComponent>
    </ion-content>
  </ion-page>
</template>
