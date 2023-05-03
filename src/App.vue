<!-- <script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script> -->

<template>
 <div class="todoapp">
    <h1 class="todoapp__title">todos</h1>

    <div class="todoapp__content">
      <header class="todoapp__header">
        <button
          class="todoapp__toggle-all"
        ></button>

        <form>
          <input
            type="text"
            class="todoapp__new-todo"
            placeholder="What needs to be done?"
          />
        </form>
      </header>

      <TransitionGroup
        name="list"
        tag="section"
        class="todoapp__main"
      >
        <TodoItem
        />
      </TransitionGroup>

      <footer class="todoapp__footer">
        <span class="todoapp__active-count">
        items left
        </span>

        <StatusFilter />

        <button
          class="todoapp__clear-completed"
        >
          Clear completed
        </button>
      </footer>
    </div>

    <Message
      class="is-warning"
      ref="errorMessage"
    >
      <template >
        <p></p>
        <button>x</button>
      </template>

      <template #header>
        <p>Server Error</p>
      </template>
    </Message>
  </div>

  <!-- <RouterView /> -->
</template>
