<template>
  <v-app>
    <!--タブ-->
    <v-navigation-drawer app v-model="drawer" color="dark">
      <v-list-item>
        <v-list-item-title class="title">
          menu
        </v-list-item-title>
        <v-btn icon>
          <v-icon color="white">mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>
      <v-divider />
      <v-list nav>
        <v-list-item v-for="menu in menus" :key="menu.title" :to="menu.url">
          <v-list-item-icon>
            <v-icon>{{menu.icon}}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{menu.title}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>    
    </v-navigation-drawer>
    <!--ヘッダーー-->
    <v-app-bar app color="dark">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>施錠管理</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
      <v-btn text to="/Login">ログイン</v-btn>
      <v-menu offset-y>
        <template v-slot:activator="{on}">
        <v-btn v-on="on" text>日本語</v-btn>
        </template>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>日本語</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>English</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-menu>
      </v-toolbar-items>
    </v-app-bar>

    <v-content>
      <router-view />
    </v-content>
　　<!--フッター-->
    <v-footer app color="dark">
      <div class="flex-grow-1"></div>
      <div>2021/4J-7group</div>
    </v-footer>
  </v-app>
  
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    drawer: false,
    menus: [
      { title: 'トップ', icon: 'mdi-web', url: '/Top' },
      { title: '一関高専1階', icon: 'mdi-numeric-1-box-multiple-outline', url: '/1F' },
      { title: '一関高専2階', icon: 'mdi-numeric-2-box-multiple-outline', url: '/2F' },
      { title: '一関高専3階', icon: 'mdi-numeric-3-box-multiple-outline', url: '/3F' },
      { title: '一関高専4階', icon: 'mdi-numeric-4-box-multiple-outline', url: '/4F' }
    ]
  })
}
</script>


<style>
.bg{
  background-image: url("~@/assets/email-pattern.png");
    background-repeat: no-repeat;
    background-size: cover;
    width: 100vw;
    height: 100vh;
}
.grey{
  color:dimgrey;
}

</style>