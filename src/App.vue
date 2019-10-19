<template>
  <div id="app">
    <header class="">
      <search-bar :placeholderTxt="'Enter an activity..'" />
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
  },
	data() {
  	return {
  		todoInputStr: ''
		}
	}
};
</script>

<style lang="scss">
  @import "~reset-css/reset.css";

  body {
    background: #edf0f1;
    padding: 80px 0 0 0;
  }

  body, input, button {
    font-family: 'Roboto', sans-serif;
  }

  .noFill {
    fill: none;
  }

  header {
    width: 100%;
    height: 80px;

    position: fixed;
    padding: 15px;
    top: 0;
    left: 0;
    z-index: 5;

    background: #25b99a;
    box-shadow: 0px 2px 4px rgba(44, 62, 80, 0.15);
    border-bottom-right-radius: 10px;
    border-bottom-left-radius: 10px;
  }

  header button {
    width: 50px;
    height: 50px;

    position:absolute;
    top:15px;
    right:15px;
    z-index:2;

    border-radius: 25px;
    background: #fff;
    border: 0px;
    box-shadow: none;
    outline: none;
    cursor: pointer;

    -webkit-appearance: none;
    -moz-appearance: none;
  }

  header button svg {
    width: 16px;
    height: 16px;

    position: absolute;
    top: 50%;
    left: 50%;

    margin: -8px 0 0 -8px;
  }

  header button svg .fill {
    fill: #25b99a;
  }
</style>
