<template>
  <div>
    {{text}}
    <v-text-field v-model="text"></v-text-field>
    <v-btn color="primary" v-on:click="onButtonClick">追加</v-btn>
    <ul>
      <li v-for="(item,i) in list" :key="i">{{item}} <v-btn v-on:click="onDeleteButton(i)">削除する</v-btn></li>
    </ul>
  </div>
</template>

<script>
export default {
  data: ()=>({
    text: "ああ",
    list:[
      "洗濯をする",
      "JavaScriptの勉強",
      "メールを送る"
    ]
  }),
  methods:{
    onButtonClick(){
      this.list.push(this.text)
      this.text = ""
    },
    onDeleteButton(idx){
      this.list.splice(idx,1)
    }
  }
}
</script>
