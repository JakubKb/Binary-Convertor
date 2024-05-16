<template>
  <div class="container">
    <div class="content">
      <h1 class="title">Binary converter</h1>
      <div class="binary-input-row">
        <div class="inputs-row">
          <p>Numbers</p>
          <input type="checkbox" id="switch" /><label for="switch"
            >Toggle</label
          >
          <p>Letters</p>
          <input
            type="text"
            placeholder="Input binary here"
            class="binary-input"
          />
        </div>
      </div>
      <div class="output-wrapper">
        <h2>Output:</h2>
        <input class="output" disabled />
      </div>
    </div>
    <button class="help">click here for help</button>
    <help-vue :style="{ display: helpDisplay }" />
  </div>
</template>

<script>
import helpVue from "./help.vue";

export default {
  data() {
    return {
      helpDisplay: "none",
    };
  },
  components: {
    helpVue,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #222831;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
}
.content {
  border: 3px solid #76abae;
  background: #31363f;
  -webkit-box-shadow: 8px 8px 24px 0px rgba(118, 171, 174, 1);
  -moz-box-shadow: 8px 8px 24px 0px rgba(118, 171, 174, 1);
  box-shadow: 8px 8px 24px 0px rgba(118, 171, 174, 1);
  border-radius: 7px;
  height: 400px;
  width: 400px;
  padding: 20px;
  display: flex;
  flex-direction: column;
}

.title {
  text-align: center;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  margin-bottom: 10px;
}

.binary-input {
  background: transparent;
  border: #76abae 2px solid;
  border-radius: 5px;
  color: #76abae;
  padding: 5px;
  font-family: "Roboto", sans-serif;
  margin-right: 5px;
}

.inputs-row {
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  justify-content: space-around;
  gap: 5px;
}

.output {
  background: transparent;
  border: #76abae 2px solid;
  border-radius: 5px;
  padding: 5px;
  font-family: "Roboto", sans-serif;
  margin-top: 15px;
  height: 200px;
  width: 100%;
  color: #76abae;
}

h2 {
  text-align: center;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  margin-top: 15px;
}

.inputs-row p {
  text-transform: uppercase;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  font-size: 13px;
}

input[type="checkbox"] {
  height: 0;
  width: 0;
  visibility: hidden;
}

label {
  cursor: pointer;
  text-indent: -9999px;
  width: 50px;
  height: 25px;
  background: grey;
  display: block;
  border-radius: 100px;
  position: relative;
}

label:after {
  content: "";
  position: absolute;
  top: 5px;
  left: 5px;
  width: 15px;
  height: 15px;
  background: #fff;
  border-radius: 90px;
  transition: 0.3s;
}

input:checked + label {
  background: #76abae;
}

input:checked + label:after {
  left: calc(100% - 5px);
  transform: translateX(-100%);
}

label:active:after {
  width: 10px;
}

.help {
  text-align: center;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  margin-top: 20px;
  font-size: 12px;
  text-decoration: underline;
  cursor: pointer;
  background: none;
  border: none;
}
</style>
