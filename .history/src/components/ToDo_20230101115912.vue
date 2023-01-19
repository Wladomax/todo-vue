<template>
  <div class="container">
    <h2 class="text-center mt-3">Pink panter</h2>

    <!-- input -->
    <div class="d-flex">
      <input type="text" placeholder="Insert your task" class="form-control" />
      <button class="btn btn-warning rounded-0">Submit</button>
    </div>

    <!-- Table-->
    <table class="table table-bordered mt-5">
      <thead>
        <tr>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th scope="col" class="text-center">#</th>
          <th scope="col" class="text-center">$</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Do something with your life</td>
          <td>To do</td>
          <td>
            <div>
              <span class="fa fa-pen"> </span>
            </div>
          </td>
          <td>
            <div>
              <span class="fa fa-tresh"> </span>
            </div>
          </td>
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
