<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      novo_jogador: "",
      n_camisa: "",
      jogadores: [
        { id: 1, name: "Filipe", n_camisa: "10", time: "Vasco", funct: "" },
        { id: 2, name: "Paulo", n_camisa: "11", time: "Vasco", funct: "" },
        { id: 3, name: "Nicolau", n_camisa: "12", time: "Vasco", funct: "" },
        { id: 4, name: "Guilherme", n_camisa: "13", time: "Vasco", funct: "" },
      ],
    };
  },
  methods: {
    salvar() {
     if (this.novo_jogador !== "") {
      const id = uuid();
      this.jogadores.push({
        id: id,
        name: this.novo_jogador,
        time: this.novo_time,
        n_camisa: this.n_camisa
      });
      this.novo_jogador = "";
      this.novo_time = "";
      this.n_camisa = "";
      } else {
      alert("Informe as coisas!") 
      } 
     },
   excluir(jogador) {
      const indice = this.jogadores.indexOf(jogador);
      this.jogadores.splice(indice, 1);
    },
},
};
</script>
<template>
  <main>
    <div class="container">
      <div class="title">
        <h2>Gerenciamento de Jogadores</h2>
      </div>
      <div class="form-input">
        <input type="text" name="" id="" placeholder="Nome" v-model="novo_jogador" />
        <input type="number" name="" id="" placeholder="Numero da camisa" v-model="n_camisa" />
        <input type="text" name="" id="" placeholder="Time" v-model="novo_time" />
        <button @click="salvar">Salvar</button>
      </div>
      <div class="list-times">
        <table>
          <thead>
            <tr>
              <th>ID</th>
              <th>Nome</th>
              <th>N° Camisa</th>
              <th>Time ID</th>
              <th>Funções</th>
              <th>Ações</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="jogador in jogadores" :key="jogador.id">
              <th>{{ jogador.id }}</th>
              <th>{{ jogador.name }}</th>
              <th>{{ jogador.n_camisa }}</th>
              <th>{{ jogador.time }}</th>
              <th><select>
                <option>...</option>
                <option>Zagueiro</option>
                <option>Atacante</option>
                <option>Centro-Avante</option>
                <option>Goleiro</option>
                <option>Volante</option>
                <option>Meia</option>
                <option>Lateral</option>
              </select></th>
              <th><button @click="excluir">Excluir</button></th>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </main>
</template>
<style scoped>
.title {
  text-align: center;
  margin: 2rem 0;
}
.form-input {
  display: flex;
  justify-content: center;
}
.form-input input {
  width: 25%;
  border: 1px solid black;
  border-radius: 10px;
  padding: 0 0.5rem;
  height: 35px;
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
