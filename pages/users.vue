<script setup lang="ts">
import { faker } from '@faker-js/faker';

faker.seed(2487534756348);

interface User {
  id: string
  name: string
  email: string
}

function createUser(): User {
  const id = faker.string.uuid();
  const sex = faker.person.sexType();
  const firstName = faker.person.firstName(sex);
  const lastName = faker.person.lastName();
  const email = faker.internet.email({ firstName, lastName });
  const name = `${firstName} ${lastName}`;
  return { id, name, email };
}

const users: User[] = Array(6)
  .fill({})
  .map(createUser);
</script>

<template>
  <h2 class="text-2xl font-bold text-emerald-500">
    Users
  </h2>
  <ul class="flex flex-wrap gap-4 mt-4">
    <li v-for="user in users" :key="user.id" class="p-4 bg-gray-900 border-2 shadow-lg border-slate-800 rounded-2xl">
      <p class="text-lg font-bold tracking-tight text-gray-300">
        {{ user.name }}
      </p>
      <p class="text-sm font-semibold text-emerald-600">
        {{ user.email }}
      </p>
    </li>
  </ul>
</template>
