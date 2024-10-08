# Pastebin-worker

This is a pastebin that can be deployed on Cloudflare workers. Try it on [shz.al](https://shz.al). 

**Philosophy**: effortless deployment, friendly CLI usage, rich functionality. 

**Features**:

1. Share your paste with as short as 4 characters
2. Customize the paste URL
4. **Update** and **delete** your paste as you want
5. **Expire** your paste after a period of time
6. **Syntax highlighting** powered by PrismJS
7. Display **markdown** file as HTML
8. Used as a URL shortener
9. Customize returned mimetype

## Usage

1. You can post, update, delete your paste directly on the website (such as [shz.al](https://shz.al)). 

2. It also provides a convenient HTTP API to use. See [API reference](doc/api.md) for details. You can easily call API via command line (using `curl` or similar tools). 

3. [pb](/scripts) is a bash script to make it easier to use on command line.

## Limitations

1. If deployed on Cloudflare Worker free-tier plan, the service allows at most 100,000 reads and 1000 writes, 1000 deletes per day. 
2. Due to the size limit of Cloudflare KV storage, the size of each paste is bounded under 25 MB.
   
## 快速部署

部署前请将wrangler.toml文件里的域名修改成自己的

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/eorendel/pastebin-worker)

