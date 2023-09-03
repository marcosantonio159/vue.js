<template>

    <h1>App de Notas</h1>
        <div>
            <label for="nome">Nome:</label>
            <input type="text" v-model="nome">
        </div>
        <div>
            <input type="number" v-model="nota">
        </div>
        <button v-on:click="adicionarAluno">Adicionar Aluno</button>

        <h2>Alunos Aprovados</h2>
        <ul>
            <li v-for="aluno in alunosAprovados">{{ aluno.nome }} - {{ aluno.nota }}</li>
        </ul>

        <h2>Alunos Não Aprovados</h2>
        <ul>
            <li v-for="aluno in alunosNaoAprovados">{{ aluno.nome }} - {{ aluno.nota }}</li>
        </ul>

</template>

<script>
    export default{
        nome: "nome",
        nota: "nota",

        data() {
            return{
                nome: '',
                nota: '',
                alunosAprovados: [],
                alunosNaoAprovados: [],
                }
            },
            methods: {
                adicionarAluno() {
                    if (this.nota >= 7) {
                        this.alunosAprovados.push({ nome: this.nome, nota: this.nota });
                    } else {
                        this.alunosNaoAprovados.push({ nome: this.nome, nota: this.nota });
                    }
                    this.nome = '';
                    this.nota = null;
                }
            }
   }
</script>