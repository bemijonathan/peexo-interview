<template>
  <div>
    <nav class="calender-nav">
      <a>Explore photos</a>
      <a>Find a photographer</a>
      <a></a>
      <a>
        <img src="../assets/profile.png" width="60" />
      </a>
      <a>Oghenetega</a>
    </nav>

    <section calender>
      <h2>Avialability</h2>
      <div class="search-form">
        <div>
          <span>Calendar view</span>
          <span>List view</span>
        </div>
        <div>
          <input class="input search-date" placeholder="search" />
          <button class="search-button">+ ADD SCHEDULE</button>
        </div>
      </div>
      <div class="full-calender">
        <a class="current-month">September 2019</a>
        <button class="date-button">Today</button>
      </div>
      <Calendar />
    </section>
  </div>
</template>

<script>
import Calendar from "./calender";

export default {
  components: {
    Calendar
  }
};
</script>

<style>
[calender] h2 {
  margin-top: 50px;
}
[calender] .search-form {
  display: flex;
  justify-content: space-between;
  margin-top: 20px;
}
.full-calender {
  margin-top: 24px;
  display: flex;
  /* justify-content: center; */
  align-items: center;
}
.current-month {
  color: #4d4d4d;
  font-family: Montserrat;
  font-size: 18px;
  font-weight: 400;
  line-height: 22px;
  text-align: left;
}
.date-button {
  margin-left: 10px;
  border: 1px solid #ffb603;
  border-radius: 5px;
  background: none;
  width: 84px;
  height: 31px;
  color: #ffb603;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
  /* line-height: 17px; */
  text-align: center;
}
[calender] h2 {
  color: #4d4d4d;
  font-family: Lora;
  font-size: 24px;
  font-weight: 700;
  line-height: 29px;
  text-align: left;
}
[calender] span {
  color: #b58000;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
  line-height: 19px;
  text-align: left;
}
.calender-nav {
  height: 97px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
  /* background: red; */
  padding: 0 53px 0 40px;
  background-color: #fffdf9;
  box-shadow: 0 1px 4px 0 rgba(204, 204, 204, 0.5);
}
[calender] {
  background-color: #fffdf7;
  padding: 0 53px 0 40px;
}
.search-date {
  background-color: #fffefc;
  border: 1px solid #d4d4d4;
  border-radius: 5px;
  width: 375px;
  height: 41px;
  padding: 10px;
  outline: none;
}
.search-button {
  margin-left: 20px;
  border: none;
  outline: none;
  background-color: #ffb603;
  border-radius: 5px;
  width: 171px;
  height: 41px;
  color: #ffffff;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 500;
  text-align: center;
}
.search-date::placeholder {
  color: #d4d4d4;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
  line-height: 17px;
  text-align: left;
}
</style>