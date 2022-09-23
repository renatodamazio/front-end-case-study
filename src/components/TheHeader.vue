<template>
  <div class="container">
    <img
      class="logo"
      @click="navigateTo('')"
      src="@/assets/images/logo.svg"
      alt="BackPacker logo"
    />

    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>

    <div class="sidebar">
      <div class="hamburger-menu">
        <span class="icon" @click="toggleSideBar"></span>
      </div>

      <div
        class="sidebar__overlay"
        v-if="isActive"
        @click="toggleSideBar"
      ></div>

      <div :class="['content', { 'content--active': isActive }]">
        <span class="close" @click="toggleSideBar"></span>
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </nav>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, watch, ref } from "vue";
import { useRoute } from "vue-router";
import router from "../router";

export default defineComponent({
  name: "TheHeader",
  setup() {
    const isActive = ref(false);
    const route = useRoute();

    const toggleSideBar = () => {
      isActive.value = !isActive.value;
    };

    const navigateTo = (name: string) => {
      router.push(`/${name}`);
      toggleSideBar();
    };

    watch(route, () => (isActive.value = false));

    return {
      isActive,
      navigateTo,
      toggleSideBar,
    };
  },
});
</script>

<style scoped lang="scss">
.container {
  //
  align-items: center;
  background: none;
  display: flex;
  height: 100%;
  justify-content: space-between;
  padding: 10px calc(var(--ui-navbar-height) + var(--ui-global-margin)) 10px
    var(--ui-global-margin);
  position: relative;
  width: 100%;
  transition: width 2s;
  .logo {
    height: 90%;
    z-index: 9;
    &:hover {
      cursor: pointer;
    }
  }
  & > nav {
    padding-right: 20px;
    z-index: 99;
    a {
      color: #fff;
      text-decoration: none;
      &:not(:first-child) {
        margin-left: 1rem;
      }
      &.router-link-exact-active {
        color: var(--ui-color-link-hover);
      }
      &:hover {
        color: var(--ui-color-link-hover);
      }
    }
  }
  .sidebar {
    position: absolute;
    right: 0;
    top: 0;
    width: auto;

    &__overlay {
      position: fixed;
      top: 0;
      width: 100%;
      height: 100%;
      left: 0;
      background-color: transparent;
    }
    .hamburger-menu {
      align-items: center;
      display: flex;
      height: var(--ui-navbar-height);
      justify-content: center;
      position: relative;
      right: var(--ui-global-margin);
      width: var(--ui-navbar-height);
      .icon {
        background: linear-gradient(
          to bottom,
          transparent,
          transparent calc((var(--HAMBURGER_ICON_SIZE) / 9) * 4),
          #fff calc((var(--HAMBURGER_ICON_SIZE) / 9) * 4),
          #fff calc((var(--HAMBURGER_ICON_SIZE) / 9) * 5),
          transparent calc((var(--HAMBURGER_ICON_SIZE) / 9) * 5),
          transparent
        );
        display: inline-block;
        height: var(--HAMBURGER_ICON_SIZE);
        position: relative;
        width: var(--HAMBURGER_ICON_SIZE);
        &:hover {
          cursor: pointer;
        }
        &::after,
        &::before {
          background: #fff;
          content: "";
          height: calc(var(--HAMBURGER_ICON_SIZE) / 9);
          left: 0;
          position: absolute;
          width: 100%;
        }
        &::after {
          bottom: 0;
        }
        &::before {
          top: 0;
        }
      }
    }
    .content {
      background: rgba($color: #e7e7e7, $alpha: 0.98);
      height: 100vh;
      position: fixed;
      right: 0;
      top: 0;
      transform: translateX(var(--ui-sidebar-width));
      width: var(--ui-sidebar-width);
      transition: 0.5s ease-in-out;
      z-index: 9;
      .close {
        background: linear-gradient(
          45deg,
          transparent,
          transparent calc((var(--HAMBURGER_ICON_SIZE) / 9) * 6),
          #fff calc((var(--HAMBURGER_ICON_SIZE) / 9) * 6),
          #fff calc((var(--HAMBURGER_ICON_SIZE) / 9) * 7),
          transparent calc((var(--HAMBURGER_ICON_SIZE) / 9) * 7),
          transparent
        );
        border-radius: 5px;
        display: inline-block;
        height: var(--HAMBURGER_ICON_SIZE);
        margin: 25px;
        overflow: hidden;
        position: relative;
        width: var(--HAMBURGER_ICON_SIZE);
        &:hover {
          cursor: pointer;
        }
        &::after {
          background: linear-gradient(
            -45deg,
            transparent,
            transparent calc((var(--HAMBURGER_ICON_SIZE) / 9) * 6),
            #fff calc((var(--HAMBURGER_ICON_SIZE) / 9) * 6),
            #fff calc((var(--HAMBURGER_ICON_SIZE) / 9) * 7),
            transparent calc((var(--HAMBURGER_ICON_SIZE) / 9) * 7),
            transparent
          );
          content: "";
          height: 100%;
          left: 0;
          position: absolute;
          top: 0;
          width: 100%;
        }
      }
      nav {
        align-items: center;
        border-top: 1px solid var(--ui-color-header);
        display: flex;
        flex-direction: column;
        margin: 0 auto;
        padding: 20px 0;
        justify-content: center;
        width: calc(100% - 20px);
        a {
          color: var(--ui-color-text);
          margin: 1rem auto;
          text-decoration: none;
          &.router-link-exact-active {
            color: var(--ui-color-link-hover);
          }
          &:hover {
            color: var(--ui-color-link-hover);
          }
        }
      }
      &--active {
        display: flex;
        flex-direction: column;
        transform: translateX(0%);
      }
    }
  }
}
</style>
