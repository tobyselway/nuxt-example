<template>
  <div class="flex flex-col w-screen h-screen overflow-hidden antialiased text-gray-200 select-none bg-gray-950">
    <UiNavbar
      title="My App"
      :items="[
        { title: 'Home', to: '/' },
        { title: 'Users', to: '/users' },
      ]"
    />
    <div class="flex-1 p-6 overflow-auto">
      <slot />
    </div>
  </div>
</template>
