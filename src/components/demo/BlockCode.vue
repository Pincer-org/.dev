<template>
	<figure class="code" :class="{'closed': closed, 'hide': hide}">
		<figcaption>
			<p>bot.py</p>
			<svg width="36" height="8" viewBox="0 0 36 8" fill="none" xmlns="http://www.w3.org/2000/svg">
				<ellipse cx="32" cy="4" rx="4.00001" ry="4" fill="#DC5252" @click="close()"/>
				<ellipse cx="18.0005" cy="4" rx="4.00001" ry="4" fill="#D6985E"/>
				<ellipse cx="4.00001" cy="4" rx="4.00001" ry="4" fill="#8ECF4E"/>
			</svg>
		</figcaption>
		<pre><code>
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

</code></pre>
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
	if (window.innerWidth < 580) {
		return
	}

	const token = document.getElementById("token");

	setInterval(() => {
				token.innerHTML = getToken();
			}, 3000
	);
}

import T from './T.vue'

export default {
	name: 'BlockCode',
	components: {
		T
	},
	data() {
		return {
			closed: false,
			hide: false
		}
	},
	methods: {
		close() {
			this.closed = true

			setTimeout(() => {
				this.hide = true
			}, 1000)
		}
	}
}
</script>

<style lang="scss" scoped>
figure {
	padding: 0;
	width: calc(100vw - 40px);
	margin: 2em 0 0;

	figcaption {
		display: flex;
		justify-content: space-between;
		align-items: center;

		background: #2B3448;
		box-shadow: 0 1px 1px rgba(0, 0, 0, 0.33);
		padding: 10px 20px;
		border-radius: .5em .5em 0 0;

		p {
			margin: 0;
			font-size: .6em;
		}
	}

	pre {
		margin: 0;
		padding: 0 20px;
		background: #363D4E;
		border-bottom-left-radius: .5em;
		border-bottom-right-radius: .5em;
		line-height: .75em;
	}

	code {
		font-family: "Fira Code", monospace;
		font-size: .55em;
		color: #B3BDDF;
	}

	&.closed {
		animation: windowClose .5s ease-in-out forwards;
	}

	&.hide {
		animation: windowClose 1s cubic-bezier(.35, -0.21, .04, 1.52) reverse forwards;

		& > figcaption, pre {
			display: none;
		}

		&::after {
			content: "Ooops...";
		}
	}
}

@media (max-width: 580px) {
	pre {
		overflow-x: scroll;
	}
}

@media screen and (min-width: 720px) and (max-width: 979px) {
	figure {
		width: 100%;
	}
}

@media screen and (min-width: 980px) {
	.code {
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
