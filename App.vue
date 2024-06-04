<template>
<center>
<fieldset>

      <h1>BMI Calculator</h1>
<br><br>
        <label for="weight">Weight (kg):</label>
        <input type="number" v-model="weight">
        <br><br>
        <label for="height">Height (m):</label>
        <input type="number" v-model="height">

      <p>Your BMI is: {{ bmi }}</p>
      <p class="ab">KNOW Your HEALTHS CARE</p>
      
      </fieldset>
 </center> 
  </template>
<script>
export default {
  data() {
    return {
      weight: 0,
      height: 0
    };
  },
  computed: {
    bmi() {
      if (this.weight && this.height) {
        // BMI = weight (kg) / (height (m) ^ 2)
        return (this.weight / (this.height ** 2));
      }
      return 0;
    }
  }
};
</script>
<style>
fieldset{
  width:400px;
  height:400px;
  background-color: gray;
  border-radius:80px;
  margin:100px;
  box-shadow: 1000px blue;
}
input{
  border-radius:80px;
  color:green;
  
}
h1{
  color:white;

}
body{
  color:white;
  background:violet;
}
label{
  font-family:'poppin'serif;
}
.ab{
  margin:100px;

}

</style>
