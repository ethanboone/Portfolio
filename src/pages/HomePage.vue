<template>
  <div class="home flex-grow-1 d-flex flex-column justify-content-center">
    <div class="row justify-content-center">
      <div class="col-10 col-md-5 card bg-card">
        <h2 class="text-light">
          About Me
        </h2>
        <p class="text-light mt-3 mb-4">
          Hello, I'm a developer in Boise, Idaho and am learning software development at Codeworks.
          My stack includes Vanilla Javascript, Vue.js, Bootstrap, Node.js, Mongoose/MongoDb, C# .NET, and MySQL.
          I consider myself a passionate problem solver and I love the continuous learning that comes with programming.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped lang="scss">
.home{
  user-select: none;
}

.bg-card {
  background-color: rgba(0, 0, 0, 0.7);
}
</style>
