<script setup>
const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
        <div class="col">
            <input :value="props.tarefaTemp" @input="props.editaTarefaTemp" required type="text" placeholder="Digite a descrição da tarefa" class="form-control" />
        </div>
        <div class="col-md-2">
            <button type="submit" class="btn btn-primary">Cadastrar</button>
        </div>
            <div class="col-md-2">
            <select @change="props.trocarFiltro" class="form-control">
            <option value="todas">Todas as tarefas</option>
            <option value="pendentes">Tarefas Pendentes</option>
            <option value="finalizadas">Tarefas Finalizadas</option>
            </select>
        </div> 
        </div>
    </form>
</template>
