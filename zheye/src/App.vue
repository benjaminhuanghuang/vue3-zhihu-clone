<template>
  <div class="container">
    <global-header :user="currentUser"></global-header>
    <column-list :list="list"></column-list>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import "bootstrap/dist/css/bootstrap.min.css";
import GlobalHeader, { UserProps } from './components/GlobalHeader.vue'
import ColumnList, { ColumnProps } from "./components/ColumnList.vue";

const currentUser: UserProps = {
  isLogin: true, // false,
  name: 'ben'
}

const testData: ColumnProps[] = [
  {
    id: 1,
    title: "Test",
    description: "description.....",
    avatar: "http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5f3e3a17c305b1070f455202.jpg?x-oss-process=image/resize,m_pad,h_50,w_50"
  },
  {
    id: 2,
    title: "Test2",
    description: "description.....",
    avatar: "http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5f3e3a17c305b1070f455202.jpg?x-oss-process=image/resize,m_pad,h_50,w_50"
  },
  {
    id: 3,
    title: "Test2",
    description: "description....."
  }
];
export default defineComponent({
  name: "App",
  components: {
    ColumnList,
    GlobalHeader
  },
  setup () {
    return {
      list: testData,
      currentUser
    };
  }
});
</script>

<style></style>
