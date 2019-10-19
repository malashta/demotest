<template>
  <div id="app">
    <header class="">
      <search-bar />
    </header>
    <section class="container">
      <todo-list />
      <pagination />
    </section>
  </div>
</template>

<script>
import { SearchBar, Pagination, TodoList } from './components';

export default {
  name: 'app',
  components: {
    SearchBar,
    Pagination,
    TodoList
  }
};
</script>
