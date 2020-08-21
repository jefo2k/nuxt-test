<template>
  <div class="container">
    <a-layout id="components-layout-demo-top-side-2">
      <a-layout-header class="header">
        <div class="logo" />
        <div class="profile">
          <a-icon type="bell" style="color: #595959" />
          <a-avatar size="small" icon="user" />
        </div>
      </a-layout-header>
      <a-layout>
        <a-layout-sider width="200" style="background: #fff">
          <a-menu
            mode="inline"
            :default-selected-keys="['1']"
            :default-open-keys="['sub1']"
            :style="{ height: '100%', borderRight: 0 }"
          >
            <a-sub-menu key="sub1">
              <span slot="title"><a-icon type="user" />subnav 1</span>
              <a-menu-item key="1">
                option1
              </a-menu-item>
              <a-menu-item key="2">
                option2
              </a-menu-item>
              <a-menu-item key="3">
                option3
              </a-menu-item>
              <a-menu-item key="4">
                option4
              </a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title"><a-icon type="laptop" />subnav 2</span>
              <a-menu-item key="5">
                option5
              </a-menu-item>
              <a-menu-item key="6">
                option6
              </a-menu-item>
              <a-menu-item key="7">
                option7
              </a-menu-item>
              <a-menu-item key="8">
                option8
              </a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub3">
              <span slot="title"><a-icon type="notification" />subnav 3</span>
              <a-menu-item key="9">
                option9
              </a-menu-item>
              <a-menu-item key="10">
                option10
              </a-menu-item>
              <a-menu-item key="11">
                option11
              </a-menu-item>
              <a-menu-item key="12">
                option12
              </a-menu-item>
            </a-sub-menu>
          </a-menu>
        </a-layout-sider>
        <a-layout style="padding: 0 24px 24px">
          <a-breadcrumb style="margin: 16px 0">
            <a-breadcrumb-item>Home</a-breadcrumb-item>
            <a-breadcrumb-item>List</a-breadcrumb-item>
            <a-breadcrumb-item>App</a-breadcrumb-item>
          </a-breadcrumb>
          <a-layout-content
            :style="{
              background: '#fff',
              padding: '24px',
              margin: 0,
              minHeight: '280px'
            }"
          >
            <h1>Welcome to the Nuxt test app</h1>
            <h2>This is the section one page</h2>
            <a-alert
              message="We are using antd design system."
              type="info"
              show-icon
            />
            <nuxt-link to="/">Home page</nuxt-link>
            <br /><br />
            <a-timeline>
              <a-timeline-item>
                <div style="border: 1px solid #69C0FF; padding: 8px 15px; border-radius: 4px; background: #E6F7FF;">
                  Create a services site 2015-09-01
                </div>
              </a-timeline-item>
              <a-timeline-item>
                <a-alert
                  message="Solve initial network problems 2015-09-01"
                  type="info"/>
              </a-timeline-item>
              <a-timeline-item>
                <a-alert
                  message="Info Text"
                  description="Info Description Info Description Info Description Info Description"
                  type="info" />
              </a-timeline-item>
              <a-timeline-item>
                Network problems being solved 2015-09-01
              </a-timeline-item>
            </a-timeline>
            <a-alert message="Enjoy the ride!" type="success" show-icon />
          </a-layout-content>
        </a-layout>
      </a-layout>
      <a-layout-footer class="footer">
        Powered by ACME
      </a-layout-footer>
    </a-layout>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  head: {
    title: "Nuxt Test - Section one"
  },
  data() {
    return {
      current: ["mail"],
      openKeys: ["sub1"]
    };
  },
  watch: {
    openKeys(val) {
      console.log("openKeys", val);
    }
  },
  methods: {
    handleClick(e: Event) {
      console.log("click", e);
    },
    titleClick(e: Event) {
      console.log("titleClick", e);
    }
  }
});
</script>

<style>
#components-layout-demo-top-side-2 .logo {
  width: 74px;
  height: 16px;
  background: #9b51e0;
  margin: 24px 0;
}

#components-layout-demo-top-side-2 .profile {
  /* border: solid 1px #000; */
  align-items: center;
}

.header {
  display: flex;
  justify-content: space-between;
  height: 64px;
  /* max-width: 1100px; */
  padding: 0 24px;
  background: #fff;
  filter: drop-shadow(0px 3px 10px #f0f0f0);
  /* box-shadow: 0 3px 6px -4px rgba(0, 0, 0, 0.12), 0 6px 16px 0 rgba(0, 0, 0, 0.08), 0 9px 28px 8px rgba(0, 0, 0, 0.05); */
  /* box-shadow: 5px 8px 124px 5px rgba(208, 216, 243, 0.6); */
}

.footer {
  display: flex;
  justify-content: center;
  font-size: 12px;
}
</style>
