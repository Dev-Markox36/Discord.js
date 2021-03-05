<div id="file-viewer" class="docs-page"><div class="source-button"><a href="https://github.com/discordjs/discord.js/blob/stable/docs/general/welcome.md" title="Source"><em class="fa fa-code"></em></a></div><div><div align="center">
  <br>
  <p>
    <a href="https://discord.js.org"><img src="/static/logo.svg" width="546" alt="discord.js" id="djs-logo"></a>
  </p>
  <br>
  <p>
    <a href="https://discord.gg/bRCvFy9"><img src="https://img.shields.io/discord/222078108977594368?color=7289da&amp;logo=discord&amp;logoColor=white" alt="Discord server"></a>
    <a href="https://www.npmjs.com/package/discord.js"><img src="https://img.shields.io/npm/v/discord.js.svg?maxAge=3600" alt="NPM version"></a>
    <a href="https://www.npmjs.com/package/discord.js"><img src="https://img.shields.io/npm/dt/discord.js.svg?maxAge=3600" alt="NPM downloads"></a>
    <a href="https://travis-ci.org/discordjs/discord.js"><img src="https://travis-ci.org/discordjs/discord.js.svg" alt="Build status"></a>
    <a href="https://david-dm.org/discordjs/discord.js"><img src="https://img.shields.io/david/discordjs/discord.js.svg?maxAge=3600" alt="Dependencies"></a>
    <a href="https://www.patreon.com/discordjs"><img src="https://img.shields.io/badge/donate-patreon-F96854.svg" alt="Patreon"></a>
  </p>
  <p>
    <a href="https://nodei.co/npm/discord.js/"><img src="https://nodei.co/npm/discord.js.png?downloads=true&amp;stars=true" alt="NPM info"></a>
  </p>
</div>

<h1 id="welcome">Welcome!</h1>
<p>Welcome to the discord.js v12 documentation.</p>
<h2 id="about">About</h2>
<p>discord.js is a powerful <a href="https://nodejs.org">Node.js</a> module that allows you to easily interact with the
<a href="https://discord.com/developers/docs/intro">Discord API</a>.</p>
<ul>
<li>Object-oriented</li>
<li>Predictable abstractions</li>
<li>Performant</li>
<li>100% coverage of the Discord API</li>
</ul>
<h2 id="installation">Installation</h2>
<p><strong>Node.js 12.0.0 or newer is required.</strong><br>Ignore any warnings about unmet peer dependencies, as they're all optional.</p>
<p>Without voice support: <code>npm install discord.js</code><br>With voice support (<a href="https://www.npmjs.com/package/@discordjs/opus">@discordjs/opus</a>): <code>npm install discord.js @discordjs/opus</code><br>With voice support (<a href="https://www.npmjs.com/package/opusscript">opusscript</a>): <code>npm install discord.js opusscript</code></p>
<h3 id="audio-engines">Audio engines</h3>
<p>The preferred audio engine is @discordjs/opus, as it performs significantly better than opusscript. When both are available, discord.js will automatically choose @discordjs/opus.
Using opusscript is only recommended for development environments where @discordjs/opus is tough to get working.
For production bots, using @discordjs/opus should be considered a necessity, especially if they're going to be running on multiple servers.</p>
<h3 id="optional-packages">Optional packages</h3>
<ul>
<li><a href="https://www.npmjs.com/package/zlib-sync">zlib-sync</a> for WebSocket data compression and inflation (<code>npm install zlib-sync</code>)</li>
<li><a href="https://github.com/discord/erlpack">erlpack</a> for significantly faster WebSocket data (de)serialisation (<code>npm install discord/erlpack</code>)</li>
<li>One of the following packages can be installed for faster voice packet encryption and decryption:<ul>
<li><a href="https://www.npmjs.com/package/sodium">sodium</a> (<code>npm install sodium</code>)</li>
<li><a href="https://www.npmjs.com/package/libsodium-wrappers">libsodium.js</a> (<code>npm install libsodium-wrappers</code>)</li>
</ul>
</li>
<li><a href="https://www.npmjs.com/package/bufferutil">bufferutil</a> for a much faster WebSocket connection (<code>npm install bufferutil</code>)</li>
<li><a href="https://www.npmjs.com/package/utf-8-validate">utf-8-validate</a> in combination with <code>bufferutil</code> for much faster WebSocket processing (<code>npm install utf-8-validate</code>)</li>
</ul>
<h2 id="example-usage">Example usage</h2>
<pre><code class="language-js hljs javascript"><span class="hljs-keyword">const</span> Discord = <span class="hljs-built_in">require</span>(<span class="hljs-string">'discord.js'</span>);
<span class="hljs-keyword">const</span> client = <span class="hljs-keyword">new</span> Discord.Client();

client.on(<span class="hljs-string">'ready'</span>, () =&gt; {
  <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`Logged in as <span class="hljs-subst">${client.user.tag}</span>!`</span>);
});

client.on(<span class="hljs-string">'message'</span>, msg =&gt; {
  <span class="hljs-keyword">if</span> (msg.content === <span class="hljs-string">'ping'</span>) {
    msg.reply(<span class="hljs-string">'pong'</span>);
  }
});

client.login(<span class="hljs-string">'token'</span>);</code></pre>
<h2 id="links">Links</h2>
<ul>
<li><a href="https://discord.js.org/">Website</a> (<a href="https://github.com/discordjs/website">source</a>)</li>
<li><a href="https://discord.js.org/#/docs/main/master/general/welcome">Documentation</a></li>
<li><a href="https://discordjs.guide/">Guide</a> (<a href="https://github.com/discordjs/guide">source</a>) - this is still for stable<br>See also the WIP <a href="https://discordjs.guide/additional-info/changes-in-v12.html">Update Guide</a> also including updated and removed items in the library.</li>
<li><a href="https://discord.gg/bRCvFy9">Discord.js Discord server</a></li>
<li><a href="https://discord.gg/discord-api">Discord API Discord server</a></li>
<li><a href="https://github.com/discordjs/discord.js">GitHub</a></li>
<li><a href="https://www.npmjs.com/package/discord.js">NPM</a></li>
<li><a href="https://discordapi.com/unofficial/libs.html">Related libraries</a></li>
</ul>
<h3 id="extensions">Extensions</h3>
<ul>
<li><a href="https://www.npmjs.com/package/discord-rpc">RPC</a> (<a href="https://github.com/discordjs/RPC">source</a>)</li>
</ul>
<h2 id="contributing">Contributing</h2>
<p>Before creating an issue, please ensure that it hasn't already been reported/suggested, and double-check the
<a href="https://discord.js.org/#/docs">documentation</a>.  
See <a href="https://github.com/discordjs/discord.js/blob/master/.github/CONTRIBUTING.md">the contribution guide</a> if you'd like to submit a PR.</p>
<h2 id="help">Help</h2>
<p>If you don't understand something in the documentation, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join our official <a href="https://discord.gg/bRCvFy9">Discord.js Server</a>.</p>
</div></div>
