<template>
  <div class="container">
    <h4>Benzer Ürünler</h4>
    <hr />
    <div class="scroll-olacak">
      <span class="ok sag">
        <f-icon @click="kaydir(true)" icon="arrow-right"></f-icon>
      </span>
      <span class="ok sol">
        <f-icon @click="kaydir(false)" icon="arrow-left"></f-icon>
      </span>
      <div
        ref="urunler"
        style="position: relative"
        :style="{ left: left + 'rem' }"
        class="urunler d-flex"
      >
        <div v-for="(urun, index) in urunler" :key="index" class="card urun">
          <img class="card-img-top" :src="urun.resim" alt="Card image cap" />
          <div class="card-body text-center">
            <h5 class="card-title">{{ urun.baslik }}</h5>
            <div
              class="d-flex flex-row justify-content-center align-items-center"
            >
              <div class="bg-danger text-light rounded p-2">
                {{ urun.indirim }}%
              </div>
              <div class="d-flex flex-column">
                <span class="text-secondary"
                  ><del> {{ urun.eskiFiyat }}TL </del></span
                >
                <span> {{ urun.fiyat }}TL</span>
              </div>
            </div>
            <a href="#" class="mt-3 w-75 btn btn-outline-secondary rounded-btn"
              ><f-icon icon="shopping-cart" /> Sepete Ekle</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      left: 0,
      urunler: [
        {
          baslik: "Orkun Ayakkabı",
          eskiFiyat: 50.0,
          fiyat: 30,
          indirim: 40,
          resim: require("../assets/ayakkabi.jpg"),
        },
        {
          baslik: "Iphone P",
          eskiFiyat: 50000,
          fiyat: 25000,
          indirim: 50,
          resim: require("../assets/telefon.jpg"),
        },
        {
          baslik: "Batuhan Ayakkabı",
          eskiFiyat: 50.0,
          fiyat: 30,
          indirim: 40,
          resim: require("../assets/ayakkabi.jpg"),
        },
        {
          baslik: "Iphone P",
          eskiFiyat: 50000,
          fiyat: 25000,
          indirim: 50,
          resim: require("../assets/telefon.jpg"),
        },
        {
          baslik: "Orkun Ayakkabı",
          eskiFiyat: 50.0,
          fiyat: 30,
          indirim: 40,
          resim: require("../assets/ayakkabi.jpg"),
        },
        {
          baslik: "Iphone P",
          eskiFiyat: 50000,
          fiyat: 25000,
          indirim: 50,
          resim: require("../assets/telefon.jpg"),
        },
        {
          baslik: "Batuhan Ayakkabı",
          eskiFiyat: 50.0,
          fiyat: 30,
          indirim: 40,
          resim: require("../assets/ayakkabi.jpg"),
        },
        {
          baslik: "Iphone P",
          eskiFiyat: 50000,
          fiyat: 25000,
          indirim: 50,
          resim: require("../assets/telefon.jpg"),
        },
        {
          baslik: "Orkun Ayakkabı",
          eskiFiyat: 50.0,
          fiyat: 30,
          indirim: 40,
          resim: require("../assets/ayakkabi.jpg"),
        },
        {
          baslik: "Iphone P",
          eskiFiyat: 50000,
          fiyat: 25000,
          indirim: 50,
          resim: require("../assets/telefon.jpg"),
        },
      ],
    };
  },
  methods: {
    kaydir(sagaMi) {
      if (sagaMi) this.left -= 18;
      else this.left += 18;
      if (this.left * -1 >= this.$refs.urunler.scrollWidth / 16 - 4 * 18) {
        this.left = 0;
      }
      if (this.left > 0) {
        this.left = 0;
      }
    },
  },
};
</script>

<style>
.rounded-btn {
  border-radius: 70px !important;
}
.urun {
  border: none !important;
  width: 18rem;
}
.urunler {
  width: max-content;
  transition: all 1s ease;
}
.scroll-olacak {
  position: relative;
  overflow: hidden;
}
.ok {
  padding: 5px;
  background-color: white;
  color: gray;
  border-radius: 30px;
  top: 30%;
  text-align: center;
  z-index: 9;
  width: 30px;
  height: 35px;
  position: absolute;
  box-shadow: 0.5px 0.5px 10px 0px gray;
}
.sag {
  right: -5px;
}
.sol {
  left: -5px;
}
</style>