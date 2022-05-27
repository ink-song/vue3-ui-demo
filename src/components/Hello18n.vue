<!-- @format -->

<template>
  <div>
    <button @click="changeLans">切换语言</button>
    <p>{{ t('message') }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { useI18n } from 'vue-i18n'
export default defineComponent({
  name: 'HelloI18n',
  setup(ctx, prop) {
    const { t } = useI18n({
      inheritLocale: true,
      useScope: 'local',
    })
    console.log(ctx, prop)

    function changeLans() {
      console.log(111)
    }

    // Something todo ..
    return { t, changeLans }
  },
})
</script>

<i18n>
{
  "en": {
    "hello": "Hello i18n in SFC!"
  }
}
</i18n>
