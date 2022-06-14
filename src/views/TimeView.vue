<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      times: [
        {
          id: "",
          name: "Informe o seu time!",
          actions: "",
        },
      ],
    };
  },
  methods: {
     salvar() {
      if (this.novo_time !== "") {
        const novo_id = uuid();
        this.times.push({
          id: novo_id,
          name: this.novo_time,
        });
        this.novo_time = "";
      } else {
        alert("Informe um time!");
      }
    },
    excluir(time) {
      const indice = this.times.indexOf(time);
      this.times.splice(indice, 1);
    },
  },
};
    
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de times</h2>
    </div>
    <div class="form-input">
      <input
        type="text"
        name=""
        id=""
        placeholder="Cadastrar Times"
        v-model="novo_time"
      />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
            <th></th>
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="time in times" :key="time.id">
            <th>{{ time.id }}</th>
            <th>{{ time.name }}</th>
            <th></th>
            <th><button>Reescrever</button></th>
            <th><button @click="excluir (time)">Excluir</button></th>
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
