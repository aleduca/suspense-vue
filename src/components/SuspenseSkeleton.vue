<template>
  <div class="card">
    <div id="img"></div>
    <div class="card-body">
      <h5></h5>
      <p></p>
      <div id="button"></div>
    </div>
  </div>
</template>

<style scoped>
.card {
  width: 18rem;
  background-color: #ececec;
}

.card #img {
  width: 100%;
  height: 200px;
  border: solid 1px #efefef;
  background-color: #fff;
}

.card-body {
  color: #fff;
  height: 450px;
}

.card-body h5 {
  height: 50px;
  background-color: #fff;
}

.card-body p {
  height: 300px;
  background-color: #fff;
}

.card-body #button {
  width: 100%;
  height: 40px;
  background-color: #fff;
}
</style>