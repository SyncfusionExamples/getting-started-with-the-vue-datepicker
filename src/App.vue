<template>
  <div class="wrapper">
    <ejs-datepicker placeholder="Choose a date"
      :value="dateValue"
      :min="minDate"
      :enableMask="true"
      format="dd-MMM-yy"
      start="Year"
      depth="Year"></ejs-datepicker>
  </div>
</template>

<script>
import {DatePickerComponent, MaskedDateTime} from '@syncfusion/ej2-vue-calendars';

export default {
  name: 'App',
  components: {
    'ejs-datepicker': DatePickerComponent
  },
  data(){
    return{
      dateValue: new Date("08/22/2022"),
      minDate: new Date("08/08/2022"),
      maxDate: new Date("08/26/2022") //asign this to max property e.g. :max="maxDate"
    }
  },
  provide:{
    datepicker: [MaskedDateTime]
  }
}
</script>

<style>
  @import '../node_modules/@syncfusion/ej2-base/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-buttons/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-inputs/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
  @import "../node_modules/@syncfusion/ej2-vue-calendars/styles/material.css";
.wrapper{
  max-width: 250px;
  margin: 0 auto;
}
</style>
