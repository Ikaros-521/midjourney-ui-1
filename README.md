# midjourney-ui

Midjourney UI is an open source txt2img UI for AI draw

<div align="center">
	<p>
		<a href="https://discord.gg/GavuGHQbV4"><img src="https://img.shields.io/discord/1082500871478329374?color=5865F2&logo=discord&logoColor=white" alt="Discord server" /></a>
		<a href="https://hub.docker.com/r/erictik/midjourney-ui/tags">
		    <img src="https://img.shields.io/docker/v/erictik/midjourney-ui?color=5865F2&logo=docker&logoColor=white" alt="Docker" />
		</a>
	</p>
</div>

[discord bot example](https://github.com/erictik/midjourney-discord-wrapper/)

See [README.dev.md](README.dev.md) for development instructions.
See a screenshot of the UI
![screenshot](images/Screenshot.png)

## Deploy

#### Vercel

Host your own live version of Midjourney UI with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Ferictik%2Fmidjourney-ui)

![image](https://github.com/Ikaros-521/midjourney-ui-1/assets/40910637/cc80c517-a203-43fa-b8a6-8c5b12a7a6dd)
![image](https://github.com/Ikaros-521/midjourney-ui-1/assets/40910637/c66cea0c-302f-4e11-903e-9af6d52624a1)
![image](https://github.com/Ikaros-521/midjourney-ui-1/assets/40910637/12dded51-aa33-4329-b7e9-ab14a4ef09db)
![image](https://github.com/Ikaros-521/midjourney-ui-1/assets/40910637/6f4fdd34-1f39-4939-9479-46e6f2504dae)



在`settings/environment-variables`这，配置你的环境变量  
![image](https://github.com/Ikaros-521/midjourney-ui-1/assets/40910637/f688f967-54a4-41bc-a6ea-629e141280dd)


#### Docker

```bash
docker run --env-file .env -p 3000:3000 erictik/midjourney-ui
```

or

```bash
docker run -e SALAI_TOKEN=xxxxxxxx  -e SERVER_ID=xxxxxxxx -e CHANNEL_ID=xxxxxxxx -p 3000:3000 erictik/midjourney-ui
```

## Runnning locally

1. clone the repo

```bash
git clone https://github.com/erictik/midjourney-ui.git
cd midjourney-ui
```

2. 安装依赖/install dependencies 

```bash
npm install
```

or

```bash
yarn
```

3. 设置环境变量/set the environment variables [How to get your Discord SALAI_TOKEN:](https://www.androidauthority.com/get-discord-token-3149920/)

SALAI_TOKEN就是请求`https://discord.com/api/v9/interactions`抓包，请求头中的`authorization`，CHANNEL_ID在请求体中可以找到。
![image](https://github.com/Ikaros-521/midjourney-ui-1/assets/40910637/2aa0d935-26c6-4aaa-ae4d-2a8a8589d343)

```bash
export SALAI_TOKEN=xxxxxxxx
export SERVER_ID=xxxxxxxx
export CHANNEL_ID=xxxxxxxx
```


如果你是win，请在运行cmd或powershell后，使用set命令设置环境  
```
set SALAI_TOKEN=xxxx.xxxxxxxxx
set SERVER_ID=110111111204
set CHANNEL_ID=11041111113207
set SESSION_ID=b1111111111113
```

4. 运行开发版服务/run the development server

```bash
npm run dev
```

or

```bash
yarn dev
```

5. open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

看cmd日志，会打印运行的IP 端口，浏览器访问即可。

## Route map

- [x] upsclae & variation
- [ ] chatgpt prompt generation
- [ ] history of generated images
