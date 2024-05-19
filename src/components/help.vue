<template>
  <div class="container">
    <div class="content">
      <h2>How to use this converter?</h2>
      <p>
        Firstly, select if you want to translate from binary to numbers, or from
        binary to letters with the switch. As you type, the converter will
        dynamically convert the binary input to numbers/letters output.
      </p>
      <img src="../assets/image-help.png" />
      <button @click="$emit('goBack')">Go Back</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  border: 3px solid #76abae;
  background: #31363f;
  -webkit-box-shadow: 8px 8px 24px 0px rgba(118, 171, 174, 1);
  -moz-box-shadow: 8px 8px 24px 0px rgba(118, 171, 174, 1);
  box-shadow: 8px 8px 24px 0px rgba(118, 171, 174, 1);
  border-radius: 7px;
  max-height: 550px;
  max-width: 500px;
  color: #76abae;
  padding: 20px;
}

h2 {
  text-align: center;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  margin-bottom: 10px;
}

p {
  text-transform: uppercase;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  font-size: 13px;
  text-align: center;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

img {
  max-height: 353px;
  max-width: 341px;
}

button {
  text-align: center;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  margin-top: 40px;
  font-size: 12px;
  text-decoration: underline;
  cursor: pointer;
  background: none;
  border: none;
}
</style>
