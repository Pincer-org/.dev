<script setup>
import T from './T.vue'
</script>
<template>
  <figure>
    <figcaption>
      <p>bot.py</p>
      <svg width="36" height="8" viewBox="0 0 36 8" fill="none" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="32" cy="4" rx="4.00001" ry="4" fill="#DC5252"/>
        <ellipse cx="18.0005" cy="4" rx="4.00001" ry="4" fill="#D6985E"/>
        <ellipse cx="4.00001" cy="4" rx="4.00001" ry="4" fill="#8ECF4E"/>
      </svg>
    </figcaption>
    <pre>
      <code>
<T c="p">from</T> pincer <T c="p">import</T> Client, command
<T c="p">from</T> pincer.objects <T c="p">import</T> MessageContext, Embed


<T c="p">class</T> <T c="y">Bot</T>(Client)<T c="p">:</T>

  <T c="b">@command</T>(<T c="k">name</T><T c="p">=</T><T c="g">"say"</T>, <T c="k">description</T><T
  c="p">=</T><T c="g">"Send a custom message!"</T>)
  <T c="p">async def</T> <T c="b">say_command</T>(<T c="r">self</T>, <T c="k">ctx</T><T c="p">:</T> MessageContext, <T c="k">message</T><T c="k">:</T> <T c="b">str</T>)<T c="p">:</T>
    <T c="p">return</T> <T c="b">Embed</T>(
      <T c="k">description</T>=(
        <T c="g">f"</T>{<T c="k">ctx</T>.author.mention}<T c="g"> said:\n"</T>
        <T c="g">f"`</T>{<T c="k">message</T>}<T c="g">`"</T>
      )
    )


<T c="p">if</T> __name__ <T c="p">==</T> <T c="g">"__main__"</T>:
  bot = <T c="b">Bot</T>(<T c="k">token</T><T c="p">=</T><T c="g">"<span id="token">super.secret.token</span>"</T>)
  bot.<T c="b">run</T>()
      </code>
    </pre>
  </figure>
</template>
<script>
const base64 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789_-'

const getTokenPart = (length) => {
  let token = ''
  for (let i = 0; i < length; i++) {
    token += base64[Math.floor(Math.random() * base64.length)]
  }
  return token
}

const getToken = () => {
  return getTokenPart(24) + '.' + getTokenPart(6) + '.' + getTokenPart(27)
}


window.onload = () => {
  const token = document.getElementById("token");
  const x = window.matchMedia("(min-width: 720px)")

  if (!x.matches) return

  // Take 24 random char from base64
  const tokenValue = Array.from({ length: 24 }, () => base64[Math.floor(Math.random() * base64.length)]).join('')


  setInterval(() => {
        token.innerHTML = getToken();
      }, 3000
  );
}
</script>
<style lang="scss" scoped>
figure {
  margin: 0;
  padding: 0;
  width: min(640px, calc(100vw - 40px));

  figcaption {
    display: flex;
    justify-content: space-between;
    align-items: center;

    background: #2B3448;
    box-shadow: 0 1px 1px rgba(0, 0, 0, 0.33);
    padding: 10px 20px;

    border-top-left-radius: .5em;
    border-top-right-radius: .5em;

    p {
      margin: 0;
    }
  }

  pre {
    margin: 0;
    padding: 0 20px;
    background: #363D4E;
    overflow: scroll;
    border-bottom-left-radius: .5em;
    border-bottom-right-radius: .5em;
  }

  code {
    white-space: pre;
    color: #B3BDDF;
  }
}
</style>
