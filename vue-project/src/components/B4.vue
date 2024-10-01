<template>
    <div class="text-center">
      <v-menu
        open-on-hover
      >
        <template v-slot:activator="{ props }">
          <v-btn
            color="primary"
            v-bind="props"
          >
            Quan tri vien
          </v-btn>
        </template>
  
        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
  </template>
  <script>
    export default {
      data: () => ({
        items: [
          { title: 'thong tin ca nhan' },
          { title: 'doi mat khau' },
          { title: 'dang xuat' },
          
        ],
      }),
    }
  </script>