<template>
  <footer class="h-16 relative w-full border-t dark:border-gray-800 bg-white dark:bg-gray-900 z-20">
    <div class="h-full w-full container mx-auto px-4 lg:px-8 flex items-center justify-between">
      <div class="flex items-end">
        <a href="https://nuxtjs.org" target="_blank" rel="noopener">
          <BuiltWithNuxtLight class="h-4 light-img" />
          <BuiltWithNuxtDark class="h-4 dark-img" />
        </a>
        <AppSlot name="footerLeft" class="ml-3" />
      </div>
      <div class="flex items-center space-x-4">
        <AppSlot name="footerRight" />
        <AppLangSwitcher />
        <AppColorSwitcher />
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  computed: {
    availableLocales () {
      return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale)
    }
  }
}
</script>
