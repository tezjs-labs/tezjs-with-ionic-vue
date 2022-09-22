<template>
  <ion-header
    collapse="fade"
    :translucent="true"
    class="container ion-padding"
    style="display: flex"
  >
    <ion-toolbar>
      <a href="/"
        ><img
          style="width: 45px; height: 55px"
          src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
          alt=""
      /></a>
    </ion-toolbar>

    <ion-toolbar
      style="
        color: #6b7280;
        font-size: 1rem;
        line-height: 1.5rem;
        font-weight: 500;
      "
    >
      <div class="ion-float-right">
        <tez-link to="/" class="ion-padding-horizontal">Home</tez-link>
        <tez-link to="/ionic" class="ion-padding-horizontal">Ionic</tez-link>
        <a href="https://github.com/tezjs/tezjs" target="blank"> TezJS </a>
      </div>
    </ion-toolbar>
  </ion-header>
</template>

<script>
import {
  IonHeader,
  IonToolbar,
  IonItem,
  IonLabel,
  IonButton,
  IonCol,
  IonGrid,
  IonRow,
} from "@ionic/vue";
export default {
  layoutName: "default",
  components: {
    IonHeader,
    IonToolbar,
    IonItem,
    IonLabel,
    IonButton,
    IonCol,
    IonGrid,
    IonRow,
  },
};
</script>