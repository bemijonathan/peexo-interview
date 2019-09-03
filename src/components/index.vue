<template>
  <section dashboard>
      <nav class="sideNav">
          <Navbar/>
      </nav>
      <div class="calender">
          <Calender/>
      </div>
  </section>
</template>

<script>
import Navbar from "./nav"
import Calender from "./calender-container"
export default {
    components:{
        Navbar,
        Calender
    }
}
</script>

<style>

button {
    cursor: pointer;
}
body{
    /* width: 100vw; */
    /* overflow: hidden; */
}
*{
    margin: 0;
    font-family: Montserrat-Medium;
    box-sizing: border-box;
}
[dashboard]{
    display: flex;
}

.sideNav{
    background: #4D4D4D;
    padding-top: 30px;
    max-width: 332px;
    width:100%;
    height: auto;
}
.calender{
    width: calc(100% - 322px)
}
</style>