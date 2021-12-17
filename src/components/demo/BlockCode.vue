<script setup>
import T from './T.vue'
</script>
<template>
  <figure>
    <figcaption>
      <p></p>
    </figcaption>
    <pre>
      <code>
<T c="p">from</T> pincer <T c="p">import</T> Client, command
<T c="p">from</T> pincer.objects <T c="p">import</T> MessageContext, Embed


<T c="p">class</T> <T c="y">Bot</T>(Client)<T c="p">:</T>

  <T c="b">@command</T>(<T c="k">name</T><T c="p">=</T><T c="g">"say"</T>, <T c="k">description</T><T
  c="p">=</T><T c="g">"Send a custom message!"</T>)
  <T c="p">async def</T> <T c="b">say_command</T>(<T c="r">self</T>, <T c="k">ctx</T><T c="p">:</T> MessageContext, <T
  c="k">message</T><T c="k">:</T> <T c="b">str</T>)<T c="p">:</T>
    <T c="p">return</T> <T c="b">Embed</T>(
    <T c="k">description</T>=(
      <T c="g">f"</T>{<T c="k">ctx</T>.author.mention}<T c="g"> said:\n"</T>
      <T c="p">f"</T>`{<T c="k">message</T>}<T c="g">`"</T>
    )
  )


<T c="p">if</T> __name__ <T c="p">==</T> <T c="g">"__main__"</T>:
  bot = <T c="b">Bot</T>(<T c="k">token</T><T c="p">=</T><T c="g">"<span id="token">WfVc18N6kJAbMzMqGTE1NhT5.YVCuNA.5OrfKz5KADVhIlxMgXjSs4aQcMk</span>"</T>)
  bot.<T c="b">run</T>()
      </code>
    </pre>
  </figure>
</template>
<script>
window.onload = () => {
  const token = document.getElementById("token");

  setInterval(() => {
        token.innerHTML = (
            Math.random().toString(24).substring(2)
            + Math.random().toString(6).substring(1)
            + Math.random().toString(27).substring(1)
        );
      }, 3000
  );
}
</script>
<style scoped>
code {
  white-space: pre;
  color: #B3BDDF;
}
</style>
