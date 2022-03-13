# Multi-djs [![npm](https://img.shields.io/npm/v/multi-djs.svg)](https://www.npmjs.com/package/multi-djs) [![npm](https://img.shields.io/npm/dt/multi-djs.svg?maxAge=3600)](https://www.npmjs.com/package/multi-djs)[![Gitlab code coverage (specific job)](https://img.shields.io/gitlab/coverage/multi-djs/multi-djs/README.md?color=green&job_name=multi-djs&label=github&logo=github)]

## Installation
[![NPM](https://nodei.co/npm/multi-djs.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/multi-djs/)

### Canvas

| Function  | Params |
| -------- | ------ |
| `triggered()` | `image` |
| `affect()` | `image` |
| `batslap()` | `image` `image2` |
| `beautiful()` | `image` |
| `blur()` | `image` `level (optional)` |
| `bnw()` | `image` |
| `bolsonaro()` | `image` |
| `brightness()` | `image` `amount` |
| `circle()` | `image` |
| `color()` | `color (optional)` |
| `colorfy()` | `image` `color` |
| `comunism()` | `image` |
| `createQrCode()` | `text` `options = { background: 'hexColor', color: 'hexColor' } (optional)` |
| `darkness()` | `image` `amount` |
| `del()` | `image` |
| `dither()` | `image` |
| `facepalm()` | `image` |
| `fuse()` | `image` `image2` |
| `gay()` | `image` |
| `invert()` | `image` |
| `jail()` | `image` |
| `kiss()` | `image` `image2` |
| `magik()` | `image` |
| `pixelate()` | `image` |
| `replaceColor()` | `image` `r` `g` `b` |
| `rip()` | `image` |
| `rotate()` | `image` `angle (optional)` |
| `sepia()` | `image` |
| `stickbug()` | `image` |
| `spank()` | `image` `image2` |
| `trash()` | `image` |
| `threshold()` | `image` `amount (optional)` |
| `wanted()` | `image` |
| `wasted()` | `image` |

### Gif

| Functions  |
| -------- |
| `cuddle()` `feed()` `hug()` `kiss()` `pat()` `poke()` `slap()` `tickle()` |

### Misc

| Function  | Params | Description |
| -------- | ------ | ----------- |
| `choose()` | `choices` | Faz uma decisão por você. |
| `pagination()` | `type` `message` `pages` `emojiList` `timeout` | Cria embeds com páginas. |
| `formatSizeUnits()` | `bytes` | Formata bytes para Yottabytes, Zettabytes, Exabytes, Petabytes, Terabytes, Gigabytes, Megabytes, Kilobytes, e Bytes. |
| `getRandomInt()` | `min` `max` | Escolhe um número de acordo com o número mínimo e o máximo. |
| `randomCharacters()` | `length` | Cria um texto com caracteres aleatórios. |
| `randomHex()` | `none` | Retorna um código hexadecimal aleatório. |
| `removeAcents()` | `text` | Remove acentos de um texto. |
| `shorten()` | `text` `length` | Reduz o comprimento de um texto. |
| `uptime()` | `message` | Mostra o uptime da sua aplicação. |

# Canvas Examples

### Triggered Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!triggered") {
    let image = await multi.canvas.triggered(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "triggered.gif");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/nrJ8tFz.gif)

### Affect Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!affect") {
    let image = await multi.canvas.affect(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "affect.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/xOZP7S9.png)

### Batslap Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!batslap") {
    
    let member = message.mentions.users.first()

    if(!member) return message.channel.send("Mencione alguém")

    let image = message.author.displayAvatarURL({ dynamic: false, format: 'png' })

    let image2 = member.displayAvatarURL({ dynamic: false, format: 'png' })

    let attach = await multi.canvas.batslap(image, image2);

    let attachment = new Discord.MessageAttachment(attach, "batslap.png");

    return message.channel.send(attachment);
}
})


client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/res817D.png)

### Beautiful Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!beautiful") {
    let image = await multi.canvas.beautiful(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "beautiful.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/o88gs7M.png)

### Blur Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!blur") {
    let image = await multi.canvas.blur(message.author.displayAvatarURL({ dynamic: false, format: 'png' }), 2);

    let attachment = new Discord.MessageAttachment(image, "blur.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/CC5uxxS.png)

### Bnw Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!bnw") {
    let image = await multi.canvas.bnw(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "bnw.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/AY8NIQJ.png)

### Bolsonaro Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!bolsonaro") {
    let image = await multi.canvas.bolsonaro(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "bolsonaro.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/kbQn9gG.png)

### Brightness Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!brightness") {
    let amount = 100
    let image = await multi.canvas.brightness(message.author.displayAvatarURL({ dynamic: false, format: 'png' }), amount);

    let attachment = new Discord.MessageAttachment(image, "brightness.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/Yk2ArtP.png)

### Circle Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!circle") {
    let image = await multi.canvas.circle(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "circle.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/o4QEPeO.png)

### Color Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!color") {
    let color = "#8572da";

    let image = await multi.canvas.color(color);

    let attachment = new Discord.MessageAttachment(image, "color.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/kiNeJpk.png)

### Colorfy Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!colorfy") {
    let image = message.author.displayAvatarURL({ dynamic: false, format: 'png' })
    
    let color = "#8572da";

    let image = await multi.canvas.colorfy(image, color);

    let attachment = new Discord.MessageAttachment(image, "colorfy.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/x81fNM6.png)

### Comunism Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!comunism") {
    let image = await multi.canvas.comunism(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "comunism.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/HletIvI.png)

### createQrCode Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!createqrcode") {
    let text = 'www.youtube.com/watch?v=dQw4w9WgXcQ'
    
    let image = await multi.canvas.createQrCode(text);

    let attachment = new Discord.MessageAttachment(image, "createqrcode.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/SuBP08c.png)

### Darkness Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!darkness") {
    let amount = 100
    let image = await multi.canvas.darkness(message.author.displayAvatarURL({ dynamic: false, format: 'png' }), amount);

    let attachment = new Discord.MessageAttachment(image, "darkness.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/vBv9CB5.png)

### Del Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!del") {
    let image = await multi.canvas.del(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "del.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/o8zMRO9.png)

### Dither Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!dither") {
    let image = await multi.canvas.dither(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "dither.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/lIouUyx.png)

### Facepalm Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!facepalm") {
    let image = await multi.canvas.facepalm(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "facepalm.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/0g7vQRj.png)

### Fuse Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!fuse") {
    
    let member = message.mentions.users.first()

    if(!member) return message.channel.send("Mencione alguém")

    let image = message.author.displayAvatarURL({ dynamic: false, format: 'png' })

    let image2 = member.displayAvatarURL({ dynamic: false, format: 'png' })

    let attach = await multi.canvas.fuse(image, image2);

    let attachment = new Discord.MessageAttachment(attach, "fuse.png");

    return message.channel.send(attachment);
}
})

client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/C4qmOiD.png)

### Gay Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!gay") {
    let image = await multi.canvas.gay(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "gay.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/t6R2OUA.png)

### Invert Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!invert") {
    let image = await multi.canvas.invert(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "invert.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/BPNfYyE.png)

### Jail Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!jail") {
    let image = await multi.canvas.jail(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "jail.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/3xoREL2.png)

### Kiss Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!kiss") {
    
    let member = message.mentions.users.first()

    if(!member) return message.channel.send("Mencione alguém")

    let image = message.author.displayAvatarURL({ dynamic: false, format: 'png' })

    let image2 = member.displayAvatarURL({ dynamic: false, format: 'png' })

    let attach = await multi.canvas.kiss(image, image2);

    let attachment = new Discord.MessageAttachment(attach, "kiss.png");

    return message.channel.send(attachment);
}
})

client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/QfNd6za.png)

### Magik Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!magik") {
    let image = await multi.canvas.magik(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "magik.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/oIRJnhF.jpg)

### Pixelate Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!pixelate") {
    let image = await multi.canvas.pixelate(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "pixelate.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/3gONJZo.png)

### ReplaceColor Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!replaceColor") {
    let r = "1";
    let g = "100";
    let b = "200";

    let image = await multi.canvas.replaceColor(message.author.displayAvatarURL({ dynamic: false, format: 'png' }), r, g,b);

    let attachment = new Discord.MessageAttachment(image, "replaceColor.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/llpdguM.png)

### Rip Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!rip") {
    let image = await multi.canvas.rip(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "rip.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/qa4QksF.png)

### Rotate Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!rotate") {
    let angle = 10

    let image = await multi.canvas.rotate(message.author.displayAvatarURL({ dynamic: false, format: 'png' }), angle);

    let attachment = new Discord.MessageAttachment(image, "rotate.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/CiEbq2n.png)

### Sepia Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!sepia") {
    let image = await multi.canvas.sepia(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "sepia.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/0bbbsoi.png)

### Stickbug Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!stickbug") {
    let image = await multi.canvas.stickbug(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "stickbug.mp4");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://imgur.com/jOFTFC1.mp4)

### Spank Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!spank") {
    
    let member = message.mentions.users.first()

    if(!member) return message.channel.send("Mencione alguém")

    let image = message.author.displayAvatarURL({ dynamic: false, format: 'png' })

    let image2 = member.displayAvatarURL({ dynamic: false, format: 'png' })

    let attach = await multi.canvas.spank(image, image2);

    let attachment = new Discord.MessageAttachment(attach, "spank.png");

    return message.channel.send(attachment);
}
})

client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/rrSNW5v.png)

### Trash Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!trash") {
    let image = await multi.canvas.trash(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "trash.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/1picHOu.png)

### Threshold Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!threshold") {
    let image = await multi.canvas.threshold(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "threshold.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/4CymXsX.png)

### Wanted Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!wanted") {
    let image = await multi.canvas.wanted(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "wanted.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/Bh9kX7Y.png)

### Wasted Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!wasted") {
    let image = await multi.canvas.wasted(message.author.displayAvatarURL({ dynamic: false, format: 'png' }));

    let attachment = new Discord.MessageAttachment(image, "wasted.png");

    return message.channel.send(attachment);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/jih1Xmm.png)

# Gif Examples

### Cuddle Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!cuddle") {
    let image = await multi.gif.cuddle();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/cuddle/cuddle_025.gif)

### Feed Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!feed") {
    let image = await multi.gif.feed();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/feed/feed_007.gif)

### Hug Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!hug") {
    let image = await multi.gif.hug();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/hug/hug_032.gif)

### Kiss Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!kiss") {
    let image = await multi.gif.kiss();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/kiss/kiss_102.gif)

### Pat Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!pat") {
    let image = await multi.gif.pat();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/pat/pat_065.gif)

### Poke Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!poke") {
    let image = await multi.gif.poke();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/poke/poke_008.gif)

### Slap Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!slap") {
    let image = await multi.gif.slap();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/slap/slap_004.gif)

### Tickle Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!tickle") {
    let image = await multi.gif.tickle();

    return message.channel.send(image);
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://cdn.nekos.life/tickle/tickle_001.gif)

# Misc Examples

### Choose Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!choose") {
    
    let choices = 'multi, Loritta'

    let choose = multi.choose(choices)

    console.log(choose)
}
})
~~~
![image](https://imgur.com/a/dcJyBNV.png)

### Pagination Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!pagination") {
    const embed = new Discord.MessageEmbed()
    .setTitle('Title')
    .setDescription('Description')

    const embed2 = new Discord.MessageEmbed()
    .setTitle('Title 2')
    .setDescription('Description 2')

    const embed3 = new Discord.MessageEmbed()
    .setTitle('Title 3')
    .setDescription('Description 3')
        
    const type = 'guild' // 'dm'

    const pages = [ embed, embed2, embed3 ]

    const emojiList = ["⏪", "⏩"];

    const timeout = '120000';

    multi.pagination(type, message, pages, emojiList, timeout)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/ODmYBXI.gif)

### FormatSizeUnits Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!format") {
    let format = multi.formatSizeUnits(1000000000) // 1 GB

    console.log(format)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/nBfqA7b.png)

### getRandomInt Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!getRandomInt") {

    let min = 1
    let max = 10 
    let result = multi.getRandomInt(min, max)

    console.log(result)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/ZuoSRW8.png)

### RemoveAcents Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!removeacents") {
    let text = "ã ê î ò û ń ž ş đ ģ ķ ł ý ț ř ç";

    let removedAcents = multi.removeAcents(text)

    console.log(removedAcents)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/iPq32rk.png)

### Shorten Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!shorten") {

    let text = 'A npm multi é a melhor npm de manipulção de imagem de todas!';
    let length = '25';

    let removedAcents = multi.shorten(text, length)

    console.log(removedAcents)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/2f89S7M.png)

### RandomCharacters Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!randomCharacters") {
    let length = 5;

    let random = multi.randomCharacters(length)

    console.log(random)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/R4VtP5w.png)

### RandomHex Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!randomHex") {

    let randomHex = multi.randomHex()

    console.log(randomHex)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/ffcnGT3.png)

### Uptime Example 
~~~javascript
const Discord = require("discord.js");
const client = new Discord.Client({ intents: 32767})
const multi = require("multi-djs");

client.on("message", async (message) => {
  if (message.content === "!uptime") {

    let uptime = multi.uptime(message)

    console.log(uptime)
}
})
 
client.login("Your_Bot_Token_here");
~~~
![image](https://i.imgur.com/CvQf5sc.png)
