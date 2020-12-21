<template>
  <section class="beacons">
    <div class="container">
      <div class="section-header">
        <h1>Choose beacons and fill in the order form?</h1>
      </div>

      <Card v-for="card in cards" :key="card.id" :item="card"/>
    </div>
  </section>
</template>

<script>
import Card from './Card.vue';

export default {
  components: {
    Card,
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          title: 'ASensor',
          image: './item1.png',
          price: 15,
          info: 'ASensor is a BLE beacon with multiple advertising data formats. The BLE is a very low power 2.4G radio that can transmit the beacon information efficiently. The typical beacon battery life is 1.5 year in default settings 3-Axis, 12-bit accelerometer magna aliqua.',
        },
        {
          id: 2,
          title: 'ARM Cortex - M0',
          image: './item2.png',
          price: 13,
          info: 'ARM Cortex - M0 32-bit processor Dialog solution, long battery life Support Bluetooth Smart 4.0 Builtin 1 x CR2450 battery holder Temperature sensor for environment monitoring Configurable by App AprilBeacon',
        },
        {
          id: 3,
          title: 'Estimote Proximity Beacons',
          image: './item3.png',
          price: 25,
          info: 'Estimote Proximity Beacons lifetime: 2 years range: up to 70 m packets: iBeacon™ or Eddystone™ features: motion & temperature sensor, NFC',
        },
        {
          id: 4,
          title: 'Aprilbeacon 227L (150M Range)',
          image: './item4.png',
          price: 30,
          info: 'Aprilbeacon 227L (150M Range) iBeacon size: 66mm*36mm*22mm Default frequency: 900ms Setting frequency: 100ms or more System: IOS 7.0, Android 4.3 Color: green iBeacon + white case',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.beacons{
  display: block;
  position: relative;
  float: left;
  width: 100%;
  color: #282828;
  box-sizing: border-box;
}

.section-header {
  width: 100%;
  position: relative;
  float: left;
  min-height: 1px;
  padding-left: 15px;
  padding-right: 15px;

  h1 {
    text-align: center;
    color: #282828;
    margin: 30px 0;
  }
}
</style>
