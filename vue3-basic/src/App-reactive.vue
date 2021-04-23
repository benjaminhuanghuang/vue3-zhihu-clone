<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <h1>{{ count }}</h1>
    <h1>{{ double }}</h1>
    <button @click="increase">+1</button>
    <ul>
      <li v-for="number in numbers" :key="number">{{number}}</li>
    </ul>
    <h1>{{person}}</h1>
  </div>
</template>

<script lang="ts">
import { computed, reactive, toRefs } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
interface DataProps {
  count: number;
  double: number;
  increase: () => void;
  numbers: number[];
  person: {name?:string}
}
export default {
  name: "App",

  setup() {
    const data: DataProps = reactive({
      count: 0,
      increase: () => {
        data.count++;
      },
      double: computed(() => data.count * 2),
      numbers:[1,2,3],
      person:{}
    });
    // vue3 can modify data
    data.numbers[0] = 5;
    data.person.name= "abc";
    // ref obj
    const refData = toRefs(data);
    return {
      ...refData,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
