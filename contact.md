---
layout: default
title: 联系 | Contact
---

<div id="contact">
  <h1 class="pageTitle">Contact Me</h1>
  <div class="contactContent">
    <p class="intro">如果你想和我交流iOS开发或者想探讨其他问题，请发邮件给我。</p>
    <p>当然，你也可以关注我的<a href="http://weibo.com/fengzhichu">微博 (@-枫之楚-)</a>，发私信给我。</p>
    <p>注意：标题请以「博客」开头。<br />例如：<b>「博客」我是邮件标题</b></p>
  </div>

  <!-- Check user input value. -->
  <script>
    function validateMsg(name, email, message) {
      //var insertHTMLContact = "<table><tr><td><input type="hidden" name="_next" value="{{ site.baseurl }}/contact.html" /></td></tr></table>";

      if (name == "" || email == "" || message == "") {
          alert("你有一项忘了填哦！");
          window.location.href="{{ site.baseurl }}/contact.html";          
      } else {
          window.location.href="{{ site.baseurl }}/thankyou.html";
      };
    }
  </script>
  
  <form action="http://formspree.io/fengzhichu@foxmail.com" method="POST">
    <!--<label for="name">名字 :</label>    -->
    <input type="text" id="name" name="name" placeholder="名字 | NAME" class="full-width"><br>
    <!--<label for="email">你的邮箱地址 :</label>-->
    <input type="email" id="email" name="_replyto" placeholder="邮箱 | EMAIL : user@domain.com" class="full-width"><br>
    <!--<label for="message">你想说的话 :</label>-->
    <textarea name="message" id="message" cols="30" rows="10" placeholder="消息 | MESSAGE" class="full-width"></textarea><br>
    <input type="submit" value="Send" onclick="validateMsg(name.value, email.value, message.value)" class="button">
    <input type="text" name="_gotcha" style="display:none" />
    <!--<input type="hidden" name="_subject" value="New submission!" />-->
  </form>
</div>
