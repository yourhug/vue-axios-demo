<template>
<div class="admin-content" style="padding:50px 50px 0">
    <h2 v-text="article.title"></h2>
    <p>作者：{{article.author.loginname}}　　发表于：{{$utils.goodTime(article.create_at)}}</p>
    <hr>
    <article v-html="article.content"></article>
    <h3>网友回复：</h3>
    <ul>
      <li v-for="(i,index) in article.replies" :key="index">
        <p>评论者：{{i.author.loginname}}　　评论于：{{$utils.goodTime(i.create_at)}}</p>
        <article v-html="i.content"></article>
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    name : "Content",
    data () {
      return {
        id: this.$route.params.id,
        article: {
          author: {
            loginname:""
          }
        }
      }
    },
    created () {
      this.getData();
    },
    mounted () {
      $(".admin-content").css("height",(document.documentElement.clientHeight-36-50)+"px");
    },
    methods: {
      getData () {
        this.$api.get('topic/' + this.id, null, r => {
          console.log(r.data);
          this.article = r.data;
        })
      }
    }
  }
</script>
