<template>
<div>
     <v-list>
      <v-list-group
        v-for="(item, i) in items"
        :key="i"
        v-model="item.active"
        :prepend-icon="item.icon"
        no-action
      >
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item
          v-for="subItem in item.subItems"
          :key="subItem.title"
          :to="subItem.to"
        >
          <v-list-item-content>
            <v-list-item-title v-text="subItem.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
</div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'mdi-home',
          subItems: [
            {
              title: '학교소개',
              to: '/'
            },
            {
              title: '구성도',
              to: '/position'
            },
            {
              title: '내선번호',
              to: '/callNumbers'
            }
          ]
        },
        {
          title: '예약서비스',
          icon: 'mdi-clock',
          active: true,
          subItems: [
            {
              title: '노트북',
              to: '/laptop'
            },
            {
              title: '배차',
              to: '/car'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style>

</style>
