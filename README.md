# tiddly-dark
A themed version of TiddlyWiki5 focussed on managing programmers notes

## This repository is no longer maintained

Tiddly-Dark has been replaced with [Tiddly Dark Desktop](https://github.com/ahanniga/tiddly-dark-desktop). This is an Electron app that installs the server-side components locally in `~/.tiddly-dark` when first run.

The wiki directory can be used for server-only installations if required, local or remote.

## Using Just the Server Component locally

- Install [Node JS](https://nodejs.org/)
- Install Tiddlywiki: `npm install -g tiddlywiki`
- Download and run the [desktop app](https://github.com/ahanniga/tiddly-dark-desktop/releases)
- Open a terminal and `cd` into `~/.tiddly-dark`
- Run `tiddlywiki . --listen`
- Open http://localhost:8080 in a browser

## Hosting on a Remote Server

- Upload the wiki directory to the remote server
- Install Tiddlywiki and Node, similar to the above steps
- Take steps to secure the wiki, preferably with authentication and https
- One approach might be:

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

This gives read/write access only to the specified user/pass.

### Other Options

See [this Gist](https://gist.github.com/ahanniga/ab87b066273d6d494880510116f531a4) 

