<template>
  <div>
    <div >user Details</div>
    <div class="row" >
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <div class="panel panel-default">
          <div class="panel-heading">
            <h4>Your Data</h4>
          </div>
          <div class="panel-body">
            <p>Mail: {{ userEmail }}</p>
            <p>Password: {{ password }}</p>
            <p>Age: {{ age }}</p>
            <p style="white-space: pre">Message: {{ message }}</p>
            <p>
              <strong>Send Mail?</strong>
            </p>
            <button @click="!isSubmitted">Go Back</button>
          </div>
        </div>
  
  
    </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {userEmail:String, password: String, age:Number, message:String, isSubmitted:Boolean },
  methods: {
    switched(isOn) {
      this.isSubmitted === isOn
        // this.$emit("input", this.isSubmitted);
      console.log(this.isSubmitted);
    }
  }
};
</script>

<style scoped>
#on,
#off {
  width: 40px;
  height: 20px;
  background-color: lightgray;
  padding: 2px;
  display: inline-block;
  margin: 10px -2px;
  box-sizing: content-box;
  cursor: pointer;
  text-align: center;
}
#on:hover,
#on.active {
  background-color: lightgreen;
}
#off:hover,
#off.active {
  background-color: lightcoral;
}
</style>
