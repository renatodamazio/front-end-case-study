<template>
  <div class="ui-card">
    <div class="ui-card__header">
      <div class="ui-card__header__figure">
        <img :src="props.previewURL" :title="props.user" />
      </div>
      <div class="ui-card__header__flag">
        <img src="@/assets/images/flag.svg" alt="flag" />
      </div>
      <div class="ui-card__header__title">{{ props.user }}</div>
    </div>
    <div class="ui-card__body">
      <div class="ui-card__body__avatar">
        <Avatar :img="props.userImageURL" :title="props.user" />
      </div>

      <div class="ui-card__body__info">
        <div class="ui-card__body__text">
          <div class="ui-card__body__title">{{ props.user }}</div>
        </div>
        <div class="ui-card__tags">
          <the-tags :tags="props.tags"></the-tags>
        </div>
      </div>

      <div class="ui-card__actions">
        <div>
          <a href=""
            ><i class="ui-card__actions__icon"
              ><img src="@/assets/images/thumb-up.svg"
            /></i>
            {{ convertNumber(props.likes) }}</a
          >
        </div>
        <div>
          <a href=""
            ><i class="ui-card__actions__icon"
              ><img src="@/assets/images/view.svg"
            /></i>
            {{ convertNumber(props.views) }}</a
          >
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
.ui-card {
  display: flex;
  flex-direction: column;
  width: 100%;
  min-width: var(--ui-card-size-min-desktop);
  max-width: var(--ui-card-size-max-desktop);

  @media screen and (max-width: 600px) {
    min-width: var(--ui-card-size-min-mobile);
    max-width: var(--ui-card-size-max-mobile);
  }

  &__header {
    display: flex;
    align-items: center;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: var(--ui-card-header-height);
    flex-direction: column;

    &__title {
      font-size: var(--ui-card-header-title-fs);
      line-height: var(--ui-card-header-title-line-height);
      font-weight: var(--ui-card-header-title-fw);
      color: var(--ui-card-header-title-color);
      word-break: break-word;
      white-space: normal;
    }

    &__figure {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      background-color: #fff;
      overflow: hidden;
      border-radius: var(--ui-card-header-figure-border-radius);

      img {
        width: 100%;
        height: 100%;
      }
    }

    &__flag {
      position: absolute;
      top: 0;
      right: 24px;
    }
  }

  &__body {
    display: flex;
    flex-direction: row;
    margin-top: var(--ui-card-body-distance);

    &__title {
      color: var(--ui-color-text);
      font-size: var(--ui-card-body-title-fs);
      font-weight: var(--ui-card-body-title-fw);
      line-height: var(--ui-card-body-title-line-height);
      text-align: left;
      word-break: break-word;
      white-space: normal;
    }

    &__info {
      flex-grow: 1;
      display: grid;
      grid-gap: 4px;
      grid-template-rows: auto auto;
      padding-right: 4px;
      padding-left: 12px;
      max-width: 50%;
    }
  }

  &__tags {
    flex-grow: 1;
    grid-gap: 4px;
    display: inline-grid;
    grid-template-columns: auto auto auto;
  }

  &__actions {
    display: inline-grid;
    grid-template-columns: auto auto;
    grid-gap: 12px;

    a,
    a:active {
      text-decoration: none;
      color: var(--ui-color-text);
      display: flex;
      align-items: center;
    }

    a {
      &:hover {
        color: var(--ui-color-primary);
      }
    }

    &__icon {
      display: flex;
      align-items: center;
      margin-right: 4px;
    }
  }
}
</style>
<script lang="ts">
import { defineComponent } from "vue";
import Avatar from "./Avatar.vue";
import TheTags from "./TheTags.vue";

export default defineComponent({
  name: "Card",
  props: ["props"],
  components: {
    Avatar,
    TheTags,
  },

  setup() {
    const convertNumber = (data: any) => {
      let _number: any = parseInt(data);
      let resp;

      if (_number >= 1000 && _number < 10000) {
        resp = Math.sign(_number) * (Math.abs(_number) / 1000);
        return resp.toFixed(1) + "k";
      }

      if (_number >= 10000) {
        resp = Math.sign(_number) * (Math.abs(_number) / 10000);
        return resp.toFixed(1) + "mi";
      }

      return _number;
    };

    return {
      convertNumber,
    };
  },
});
</script>
