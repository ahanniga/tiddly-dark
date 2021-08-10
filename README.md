# tiddly-dark
A themed version of TiddlyWiki5 focussed on managing programmers notes

## Introduction

If you're not already familiar with TiddyWiki I recommend you checkout the official page at [TiddlyWiki.com](https://tiddlywiki.com/). **Tiddy Dark** is a themed version of [Jeremy Rushton's](https://tiddlywiki.com/#JeremyRuston) wonderful creation with pre-installed plugins especially useful for developer notes. In summary:

- Uses the server edition
- Images and binary files managed with the *importToExternalFile* plugin
- Markdown syntax by default
- Syntax-highlighted code blocks
- Search Highlighting
- CodeMirror editor

## Prerequisites

- [Node JS](https://nodejs.org/)

## Install Quick Start

- Install [Node](https://nodejs.org/) on your local PC
- Install Tiddlywiki: `npm install -g tiddlywiki`
- Download the repo zipfile and unpack it into a directory
- Open a terminal and `cd` into the KBX directory
- Run `tiddlywiki . --listen`
- Open http://localhost:8080 in a browser

## Hosting on a Remote Server

To make the wiki available to other devices, I self-host TiddlyWiki on a another machine with a username/password and https. The easiest way to achieve this is to use the options already built into tiddywiki:

```bash
export USERNAME=yourname
export PASSWORD=yourpassword
tiddlywiki . --listen \
    host=0.0.0.0 \
    port=8181 \
    tls-cert=/path/to/cert.pem \
    tls-key=/path/to/privkey.pem \
    username=$USERNAME \
    password=$PASSWORD
```

A second, possibly more secure method is to use NGINX with a `proxy_pass` configuration. An example `server` section of `/etc/nginx/nginx.conf` example [here](https://gist.github.com/ahanniga/eec61a152b7e41687452a1f5535d6636).
