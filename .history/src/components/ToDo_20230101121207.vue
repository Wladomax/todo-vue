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
      <tbody v-for="(task, index) in tasks" :key="index">
        <tr>
          <td>{{ task.name }}</td>
          <td>To do</td>
          <td>
            <div class="text-center">
              <span class="fa fa-pen"> </span>
            </div>
          </td>
          <td>
            <div class="text-center">
              <span class="fa fa-trash"> </span>
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

  data() {
    return {
      tasks: [
        {
          name: "Do something with your life",
          status: "todo",
        },
        {
          name: "Do something with your job",
          status: "in-progress",
        },
      ],
    };
  },
};
</script>

<style scoped></style>
