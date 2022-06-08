<script>
export default {
  data() {
    return {
      times: [
        { id: 1, name: "Time 1" },
        { id: 2, name: "Time 2" },
        { id: 3, name: "Time 3" },
        { id: 4, name: "Time 4" },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de times</h2>
    </div>
    <div class="form-input">
      <input type="text" name="" id="" placeholder="Cadastrar Times" />
      <button>Salvar</button>
    </div>
    <div class="list-times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="time in times" :key="time.id">
            <th>{{ time.id }}</th>
            <th>{{ time.name }}</th>
            <th>Parle français</th>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style scoped>
.title {
  text-align: center;
  margin: 2rem 0;
}
.form-input input {
  width: 50%;
  border: 1px solid black;
  border-radius: 10px;
  padding: 0 0.5rem;
  height: 40px;
}
.form-input button {
  height: 40px;
  margin-left: 1%;
  background-color: rgb(71, 11, 103);
  font-weight: bold;
  color: white;
  border-radius: 10px;
  width: 10%;
  transition: 0.25s;
  border: 0px;
}
.list-times {
  display: flex;
  justify-content: center;
  margin: 2rem 0;
}
table {
  width: 50%;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px, rgb(0, 0, 0) 0px 0px 0px 3px;
  border-collapse: collapse;
  text-align: center;
}
table thead {
  background-color: rgb(0, 0, 0);
  color: white;
}
table thead th {
  font-weight: bolder;
}
table tbody tr:nth-child(odd) {
  background-color: rgb(63, 94, 251);
  color: white;
}
</style>
