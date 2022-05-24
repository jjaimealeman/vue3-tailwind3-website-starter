<template>
  <form>
    <label>{{ t('language') }}</label>
    <select class="select select-ghost" v-model="locale">
      <option value="en">en</option>
      <option value="es">es</option>
    </select>
  </form>
  <p>{{ t('hello') }}</p>
</template>

<script>
import { useI18n } from 'vue-i18n'

export default {
  name: 'App',
  setup() {
    const { locale, t } = useI18n({
      inheritLocale: true
    })

    return { locale, t }
  }
}
</script>

<i18n>
{
  "en": {
    "language": "English",
    "hello": "Hello, world!"
  },
  "es": {
    "language": "Spanish",
    "hello": "Hola, Mundo!"
  }
}
</i18n>
