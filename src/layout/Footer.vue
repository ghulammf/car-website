<script setup>
import logoipsum from "../assets/logoipsum.svg";
import facebook from "../assets/facebook-logo.png";
import instagram from "../assets/instagram-logo.png";
import linkedin from "../assets/linkedin-icon.png";
</script>

<template>
  <div id="contact" class="bg-slate-950 text-white mt-14">
    <div
      class="w-[90%] m-auto py-10 px-3 grid gap-8 sm:grid-cols-2 md:grid-cols-4 md:py-16"
    >
      <div class="grid gap-3">
        <img :src="logoipsum" alt="" />
        <p class="text-medium">
          Auto Heaven is your one-stop destination for hassle-free car buying
          Find, compare, and buy
        </p>
        <div class="icon flex w-fit justify-between gap-3">
          <img :src="facebook" alt="" class="w-8 h-auto" />
          <img :src="instagram" alt="" class="w-8 h-auto" />
          <img :src="linkedin" alt="" class="w-8 h-auto" />
        </div>
      </div>
      <div class="info grid md:gap-3">
        <h1>Shop</h1>
        <p>Classic Car</p>
        <p>Old Model Car</p>
        <p>Luxury Brand</p>
      </div>
      <div class="info grid md:gap-3">
        <h1>Support</h1>
        <p>3 Month free Service</p>
        <p>Product Manual</p>
        <p>Privacy Policy</p>
        <p>Product FAQ</p>
      </div>
      <div class="info grid md:gap-3">
        <h1>Contact</h1>
        <p>+62 234 567 8901</p>
        <p>Contact us</p>
        <p>Terms of service</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.icon img {
  filter: grayscale(1);
  transition: all 0.5s;
}
.icon img:hover {
  filter: grayscale(0.2);
}
.info h1 {
  font-size: large;
  font-weight: bold;
  margin: 3px 0;
}

.info p {
  cursor: pointer;
}
</style>
