<template>
  <figure class="window" :class="{ closed: closed, hide: hide }">
    <figcaption class="window-header">
      <p>bot.py</p>
      <svg
        width="36"
        height="8"
        viewBox="0 0 36 8"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <ellipse cx="32" cy="4" rx="4" ry="4" fill="#DC5252" @click="close()" />
        <ellipse cx="18" cy="4" rx="4" ry="4" fill="#D6985E" />
        <ellipse cx="4" cy="4" rx="4" ry="4" fill="#8ECF4E" />
      </svg>
    </figcaption>
    <pre class="window-container"><code id="bot-code">
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
  bot = <T c="b">Bot</T>(<T c="k">token</T><T c="p">=</T><T c="g">"<span id="token">{{token}}</span>"</T>)
  bot.<T c="b">run</T>()

</code></pre>
  </figure>
</template>

<script>
import T from "./T.vue";

const base64 =
  "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789_-";

export default {
  name: "BlockCode",
  components: {
    T,
  },
  data() {
    return {
      token: "super.secret.token",
      closed: false,
      hide: false,
    };
  },
  mounted() {
    if (window.innerWidth < 580) {
      return;
    }

    setInterval(() => {
      this.token = this.getToken();
    }, 3000);
  },
  methods: {
    getTokenPart(length) {
      let token = "";
      for (let i = 0; i < length; i++) {
        token += base64[Math.floor(Math.random() * base64.length)];
      }
      return token;
    },
    getToken() {
      return (
        this.getTokenPart(24) +
        "." +
        this.getTokenPart(6) +
        "." +
        this.getTokenPart(27)
      );
    },

    close() {
      this.closed = true;

      setTimeout(() => {
        this.hide = true;
      }, 1000);
    },
  },
};
</script>

<style lang="scss">
.window {
  padding: 0;
  width: calc(100vw - 40px);
  margin: 2em 0 0;

  &-header {
    display: flex;
    justify-content: space-between;
    align-items: center;

    background: #2b3448;
    box-shadow: 0 1px 1px rgba(0, 0, 0, 0.33);
    padding: 10px 20px;
    border-radius: 0.5em 0.5em 0 0;

    p {
      margin: 0;
      font-size: 0.6em;
    }
  }

  &-container {
    margin: 0;
    padding: 0 20px;
    background: #363d4e;
    border-bottom-left-radius: 0.5em;
    border-bottom-right-radius: 0.5em;
    line-height: 0.75em;
  }

  &.closed {
    animation: windowClose 0.5s ease-in-out forwards;
  }

  &.hide {
    animation: windowClose 1s cubic-bezier(0.35, -0.21, 0.04, 1.52) reverse
      forwards;

    & > .window-header,
    pre {
      display: none;
    }

    &::after {
      content: "Ooops...";
    }
  }
}

#bot-code {
  font-family: "Fira Code", monospace;
  font-size: 0.55em;
  color: #b3bddf;
}

@media (max-width: 580px) {
  .window-container {
    overflow-x: scroll;
  }
}

@media screen and (min-width: 720px) and (max-width: 979px) {
  .window {
    width: 100%;
  }
}

@media screen and (min-width: 980px) {
  .window {
    animation: slideInTopFade 1s ease;
    width: min(640px, 40vw);
  }

  .hide {
    height: 32px;

    &::after {
      padding-left: 55%;
    }
  }
}
</style>
