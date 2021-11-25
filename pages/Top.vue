<template>
  <v-card
    max-width="400"
    class="mx-auto">
    <v-container fluid > 
      <v-row dense>
        <v-col cols="12">
          <v-card
            color="#00ADB5"
            light>
            <v-card-title class="text-h5">
              施錠管理システム
            </v-card-title>
            <v-spacer></v-spacer>
            <v-card-subtitle>施錠状況を確認し移動の手間を短縮</v-card-subtitle>
            <v-card-text></v-card-text>
          </v-card>
        </v-col>
        
        <v-col cols="12">
          <v-card
            color="#30E3CA"
            light>
              <v-card-title>
                利用方法 
                ①左上のタブから階層を選択する。
                ②表示されている地図から知りたい場所の番号を調べる。
                ③下にスライドして番号の場所の施錠状況が分かる。
              </v-card-title>
              <v-card-text>
                ※下に地図と施錠状況の例がある。
                <v-icon >mdi-arrow-down-bold</v-icon><v-icon >mdi-arrow-down-bold</v-icon><v-icon >mdi-arrow-down-bold</v-icon>
              </v-card-text>
            </v-card>
        </v-col>

        <v-col cols="12">
          <v-card
          color="#ffffff">
            <v-card>
               <v-img :src="require('@/assets/ichinoseki-kosen.jpg')"
               height="300"
               width="500">
               </v-img>
            </v-card>
          </v-card>
        </v-col>

        
        <v-col cols="6">
          <v-card
            color="#ff0000"
          　dark>
          <v-card-title>16 第一体育館
          </v-card-title>
          <v-card-text>
           
             <v-icon center size="50">mdi-lock</v-icon>
            ※赤の時は施錠されている。
          </v-card-text>
          </v-card>
        </v-col>
        

        <v-col cols="6">
          <v-card
           color="#00FF7F"
           light> 
           <v-card-title>18 武道館 </v-card-title>
           <v-card-text>
             <v-icon mx-auto size="50">mdi-lock-open</v-icon>
              ※緑の時は開錠されている。
           </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<style>

p.map1 img{
  width: 400px;
}
</style>

<script>
  export default {
  }
  
</script>