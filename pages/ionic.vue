<template>
  <ion-grid class="ion-padding ion-margin">
    <ion-row class="ion-justify-content-center">
      <ion-col size-lg="4" size-xs="12">
        <ion-text color="tertiary">
          <h3>IONIC Demo</h3>
        </ion-text>
        <ion-card class="ion-padding ion-margin">
          <ion-item>
            <ion-label position="floating">First Name</ion-label>
            <ion-input></ion-input>
          </ion-item>

          <ion-item>
            <ion-label position="floating">Last Name</ion-label>
            <ion-input></ion-input>
          </ion-item>

          <ion-list>
            <ion-item>
              <ion-label position="floating">Gender</ion-label>
              <ion-select>
                <ion-select-option value="male">Male</ion-select-option>
                <ion-select-option value="female">Female</ion-select-option>
                <ion-select-option value="other">Other</ion-select-option>
              </ion-select>
            </ion-item>
          </ion-list>

          <ion-item>
            <ion-label>Date</ion-label>
            <ion-datetime-button datetime="datetime"> </ion-datetime-button>
            <ion-modal :keep-contents-mounted="true">
              <ion-datetime id="datetime"></ion-datetime>
            </ion-modal>
          </ion-item>

          <ion-item>
            <ion-label position="floating">Description</ion-label>
            <ion-textarea></ion-textarea>
          </ion-item>

          <ion-item>
            <ion-checkbox> </ion-checkbox>
            <ion-label class="ion-padding-start"
              >I agree to the terms and conditions</ion-label
            >
          </ion-item>

          <ion-item>
            <ion-label>Remember Me</ion-label>
            <ion-toggle color="primary"></ion-toggle>
          </ion-item>

          <ion-button @click="presentAlert" class="ion-padding"
            >Submit</ion-button
          >
        </ion-card>
      </ion-col>
    </ion-row>
  </ion-grid>
</template>
<script>
import {
  IonCheckbox,
  IonItem,
  IonLabel,
  IonButton,
  IonInput,
  alertController,
  IonDatetime,
  IonDatetimeButton,
  IonModal,
  IonTextarea,
  IonSelectOption,
  IonSelect,
  IonList,
  IonToggle,
  IonCol,
  IonGrid,
  IonRow,
  IonText,
} from "@ionic/vue";
export default {
  layoutName: "default",
  components: {
    IonCheckbox,
    IonItem,
    IonLabel,
    IonButton,
    IonInput,
    IonDatetime,
    IonDatetimeButton,
    IonModal,
    IonTextarea,
    IonSelectOption,
    IonSelect,
    IonList,
    IonToggle,
    IonCol,
    IonGrid,
    IonRow,
    IonText,
  },
  methods: {
    async presentAlert() {
      const alert = await alertController.create({
        header: "Success..",
        subHeader: "Submitted",
        buttons: [
          {
            text: "OK",
            role: "confirm",
            handler: () => {
              window.location.reload();
            },
          },
        ],
      });
      await alert.present();
    },
  },
};
</script>

<style lang="">
</style>