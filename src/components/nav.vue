<template>
  <div class="nav_items">
    <li brand>
      <img src="../assets/logo.png" width="148px" />
    </li>
    <li v-for="(item, index) in nav" :key="index">{{item.label}}</li>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nav: [
        { label: "Dashboard", icon: "" },
        { label: "Profile", icon: "" },
        { label: "Pricing Package", icon: "" },
        { label: "Availability", icon: "" },
        { label: "Bookings", icon: "" },
        { label: "Portfolio", icon: "" },
        { label: "Albums", icon: "" },
        { label: "Subscriptions", icon: "" },
        { label: "Payments", icon: "" },
        { label: "Setting", icon: "" }
      ]
    };
  }
};
</script>

<style>
.nav_items li {
  padding-left: 60px;
  color: #d4d4d4;
  font-size: 14px;
  list-style-type: none;
}
.nav_items li:first-of-type {
  margin-bottom: 93px;
}
.nav_items li:not([brand]) {
  padding-top: 35px;
  padding: 28px;
}
</style>