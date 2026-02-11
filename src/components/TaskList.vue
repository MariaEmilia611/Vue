<template>
    <div class="task-list-container">
        <h2>Lista de Tarefas</h2>

        <div class="controls">
            <button class="btn-add">Adicionar Nova Tarefa</button>
            <button class="btn-toggle-all">
                Marcar Todas
            </button>
            <button class="btn-clear">
                Limpar Concluidas
            </button>
        </div>

        <div class="tasks-coitainer">
            <div class="peding-tasks">
                <h3>Tarefas Pendentes</h3>
                <span>Lista de Tarefas Pendentes</span>
            </div>

            <div class="completed-tasks">
                <h3>Tarefas Concluidas</h3>
                <span>Lista de Tarefas Concluidas</span>
            </div>

        </div>
    </div>
</template>