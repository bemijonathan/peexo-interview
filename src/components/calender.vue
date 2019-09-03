<template>
  <div class="dates">
    <div class="days">
      <div class="week_days" v-for="(day, i) in days" :key="i">{{day}}</div>
    </div>
    <div class="days">
      <div v-for=" index in 35" :key="index">
        <div class="week_days_dates" :class="{'flex-day': within(index)}">
          <div>
            <a v-if="index <= numberOfDays">{{index}}</a>
            <div
              v-if="checkIndex(index)"
              :style="`width:${getspan(index).width}px;margin: 0  ${getspan(index).margin}px`"
              style="  background-color: #FFB603;
  border: 1px solid #D4D4D4;
  border-radius: 2px;position:absolute; padding:20px"
            >{{getContent(index)}}</div>
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
      days: ["SUN", "MON", "TUES", "WED", "THURS", "FRI", "SAT"],
      month: "Semptember",
      numberOfDays: 30,
      events: [
        {
          day: 2,
          span: 1,
          event: "Mrs. Steven daughter’s wedding photography",
          end: 2
        },
        {
          day: 11,
          span: 3,
          event: "Mrs. Peter daughter’s wedding photography",
          end: 13
        },
        {
          day: 28,
          span: 1,
          event: "Mrs. Steven daughter’s wedding photography",
          end: 28
        }
      ],
      dates: []
    };
  },
  methods: {
    checkIndex(index) {
      let x = this.events.find(e => e.day === index);
      if (x === undefined) {
        return false;
      } else {
        return true;
      }
    },
    getspan(index) {
      let x = this.events.find(element => index === element.day);
      let a = {
        width: 125 * x.span,
        margin: 4 * x.span
      };

      return a;
    },
    getContent(index) {
      let x = this.events.find(element => index === element.day);
      return x.event;
    },
    within(index) {
      let x = this.events.find(
        element => index >= element.day && index <= element.end
      );
      console.log(x);
      if (x === undefined) {
        return !false;
      } else {
        return !true;
      }
    }
  },
  computed: {}
};
</script>

<style>
.calender-nav a {
  margin:0 10px;
}
.flex-day {
  background-color: #ffffff !important;
  
  border: 1px solid #d4d4d4;
  border-radius: 2px;
  display: flex !important;
  justify-content: center !important;
  align-items: center !important;
}
.week_days_dates :not(.flex-day) {
}
.dates {
  margin-top: 20px;
  margin-bottom: 126px;
}
.days {
  display: grid !important;
  grid-template-columns: repeat(7, 1fr);
  width: 100%;
}
.week_days_dates {
  background-color: #fff3d4;
  /* background-color: #ffffff; */
  border: 1px solid #d4d4d4;
  border-radius: 2px;
  display: block;
  justify-content: center;
  align-items: center;
  width: 134px;
  /* width: 147px; */
  height: 125px;
}
.week_days {
  color: #4d4d4d;
  font-family: Montserrat;
  font-size: 12px;
  font-weight: 400;
  background-color: #ffffff;
  border: 1px solid #d4d4d4;
  border-radius: 2px;
  width: 134px;
  height: 50px;
  text-align: center !important;
  padding: 17px 0;
  box-sizing: border-box;
  margin: 0 !important;
}
</style>