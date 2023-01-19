<template>
  <div class="container">
    <h2 class="text-center mt-3">Pink panter</h2>

    <!-- input -->
    <div class="d-flex">
      <input type="text" placeholder="Insert your task" class="form-control" />
      <button class="btn btn-warning rounded-0">Submit</button>
    </div>

    <!-- Table-->
    <table class="table table-bordered">
      <thead>
        <tr>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th scope="col">Edit</th>
          <th scope="col">Delete</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Mark</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Jacob</td>
          <td>Thornton</td>
          <td>@fat</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td colspan="2">Larry the Bird</td>
          <td>@twitter</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "ToDo",
  props: {
    msg: String,
  },
};
</script>

<style scoped></style>
