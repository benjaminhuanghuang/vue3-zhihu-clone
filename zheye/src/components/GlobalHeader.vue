<template>
  <nav class="navbar navbar-dark bg-primary justify-content-between mb-4 px-4">
    <router-link class="navbar-brand" to="/">
      者也专栏
    </router-link>
    <ul v-if="!user.isLogin" class="list-inline mb-0">
      <li class="list-inline-item">
        <router-link class="btn btn-outline-light my-2" to="/login">
          登陆
        </router-link>
      </li>
      <li class="list-inline-item">
        <router-link class="btn btn-outline-light my-2" to="/login">
          注册
        </router-link>
      </li>
    </ul>
    <ul v-else class="list-inline mb-0">
      <!-- <li class="list-inline-item">你好 {{user.name}}</li> -->
      <!-- <li class="list-inline-item">
        <dropdown :title="`你好 ${user.name}`">
        </dropdown>
      </li> -->
      <dropdown :title="`你好 ${user.name}`">
        <dropdown-item>
          <router-link to="/create" class="dropdown-item">新建文章</router-link>
        </dropdown-item>
        <dropdown-item :disabled="true">
          <a href="#" class="dropdown-item">编辑资料</a>
        </dropdown-item>
        <dropdown-item>
          <a href="#" class="dropdown-item">退出登录</a>
        </dropdown-item>
      </dropdown>
    </ul>
  </nav>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import Dropdown from "./Dropdown.vue";
import DropdownItem from './DropdownItem.vue'

// interface
export interface UserProps {
  isLogin: boolean;
  name?: string;
  id?: number;
}

export default defineComponent({
  name: "GlobalHeader",
  components: {
    Dropdown,
    DropdownItem
  },
  props: {
    user: {
      type: Object as PropType<UserProps>,
      required: true
    }
  },
  setup () {
    return {};
  }
});
</script>
