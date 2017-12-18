<template>
  <div class="row" id="translateForm">
    <div class="col-md-6 col-md-offset-3">
      <form id="transForm" class="well form-inline" @submit="formSubmit">
        <input class="form-control" type="text" name="" v-model="textTotranslate" placeholder="请输入需要翻译的内容" />
        <select class="form-control" v-model="language">
          <option value="en">English</option>
          <option value="ru">Russian</option>
          <option value="ko">Korean</option>
          <option value="ja">Janpenese</option>
        </select>
        <input class="btn btn-primary" type="submit" value="翻译"/>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'translateForm',
  data: function(){
    return {
      textTotranslate:"",
      language:""
    }
  },
  methods: {
    formSubmit: function(e){
      this.$emit("formSubmit",this.textTotranslate,this.language); //这个formSubmit 与上一行的方法没有关系，是自定义事件
      e.preventDefault();
    }
  },
  created: function(){
    this.language = 'en';
  }
}
</script>

<style>
#transForm{
  border: 1px #ccc solid;
  border-radius: 10px;
}
</style>
