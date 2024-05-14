<template>
  <div class="container">
    <div class="content">
      <h1 class="title">Binary converter</h1>
      <input type="text" placeholder="Input binary here" />
      <div class="checbox-label">
        <p>Numbers</p>
        <input type="checkbox" />
      </div>
      <div class="output">test</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #222831;
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
  height: 300px;
  width: 400px;
  padding: 20px;
}

.title {
  text-align: center;
  color: #76abae;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
}
</style>
