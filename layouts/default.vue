<template>
  <div class="flex flex-col w-screen h-screen antialiased text-gray-200 select-none bg-gray-950">
    <UiNavbar
      title="My App"
      :items="[
        { title: 'Home', to: '/' },
        { title: 'Users', to: '/users' },
      ]"
    />
    <div class="flex-1 p-6">
      <slot />
    </div>
  </div>
</template>
