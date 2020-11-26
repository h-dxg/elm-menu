<template>
  <div>
    <el-row>
      <el-col
        :span="8"
        :offset="8"
      >
        <el-menu
          default-active="1"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
          background-color="#545c64"
          text-color="#fff"
          active-text-color="#ffd04b"
        >
          <el-submenu
            v-for="(i, index) in router"
            :key="index"
            :index="i.id"
          >
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>{{ i.name }}</span>
            </template>

            <div v-if="i.children">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span>{{ i.name }}</span>
              </template>
              <Menu :router="i.children"> </Menu>
            </div>
          </el-submenu>

          <!-- <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>导航一</span>
            </template>
            <el-submenu index="1-4">
              <template slot="title">选项4</template>
              <el-submenu index="1-6">
                <template slot="title">选项5</template>
                <el-menu-item index="1-4-1">选项1</el-menu-item>
              </el-submenu>
            </el-submenu>
          </el-submenu>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>导航一</span>
            </template>
          </el-submenu> -->
        </el-menu>
      </el-col>
    </el-row>
  </div>
</template>
<script>
import Menu from "@/components/menu.vue";
export default {
  name: "Menu",
  components: {
    Menu
  },
  props: {
    router: Array
  },
  created () {
    console.log(this.router, "router");
  },
  methods: {
    handleOpen (key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose (key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
