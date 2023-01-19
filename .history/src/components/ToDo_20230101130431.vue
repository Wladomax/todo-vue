<template>
  <div class="container">
    <h2 class="text-center mt-3">Pink panter</h2>

    <!-- input -->
    <div class="d-flex">
      <input
        v-model="task"
        type="text"
        placeholder="Insert your task"
        class="form-control"
      />
      <button @click="submitTask" class="btn btn-warning rounded-0">
        Submit
      </button>
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
          <td>{{ task.status }}</td>
          <td>
            <div class="text-center" @click="editTask(index)">
              <span class="fa fa-pen"> </span>
            </div>
          </td>
          <td>
            <div class="text-center" @click="deleteTask(index)">
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
      task: "",
      editedTask: null,
      statusesAvailable: ["to do", "in progress", "done"],
      tasks: [
        {
          name: "Do something with your life",
          status: "to do",
        },
        {
          name: "Do something with your job",
          status: "in-progress",
        },
      ],
    };
  },

  methods: {
    submitTask() {
      if (this.task.lenght === 0) return;

      if (this.editedTask === null) {
        this.tasks.push({
          name: this.task,
          status: "to do",
        });
        this.task = "";
      } else {
        this.tasks[this.editedTask].name = this.task;
        this.editedTask = null;
      }
    },

    deleteTask(index) {
      this.tasks.splice(index, 1);
    },
    editTask(index) {
      this.task = this.tasks[index].name;
      this.editedTask = index;
    },
  },
};
</script>

<style scoped></style>
