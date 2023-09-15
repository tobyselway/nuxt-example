<template>
  <div class="flex flex-col w-screen h-screen">
    <UiNavbar
      title="My App"
      :items="[
        { title: 'Home', to: '/' },
        { title: 'Users', to: '/users' },
      ]"
    />
    <div class="flex-1 p-4">
      <slot />
    </div>
  </div>
</template>
