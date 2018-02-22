<div align="center">
	<h1>locate.now</h1>
	<p>A simple API for IP address & geolocation lookup.</p>
</div>

---

<p align="center">
	<sub>Visit <a href="https://locate.now.sh"><code>locate.now.sh</code></a> for a live demo. Check out my <a href="https://nikolaskama.me">blog</a> and follow me on <a href="https://twitter.com/nikolaskama">Twitter</a>.</sub>
</p>

<br/>
<p align="center">
	<code>~ ❯❯❯ curl 'https://locate.now.sh/ip/json'<br/>
	{"ip":"127.0.0.1"}</code>
</p>


<br>

# Usage

### IP address lookup

<u>Format:</u>

```
https://locate.now.sh/ip/:type
```

| API URI                                | Type    | Sample Response
| -------------------------------------- | ------- | -------------  
| `https://locate.now.sh`                | `text`  | `127.0.0.1`
| `https://locate.now.sh/json`           | `json`  | `{"ip":"127.0.0.1"}`
| `https://locate.now.sh/jsonp`          | `jsonp` | `callback({"ip":"127.0.0.1"})`
| `https://locate.now.sh/jsonp/lookupip` | `jsonp` | `lookupip({"ip":"127.0.0.1"})`

<u>Examples:</u>

```
~ ❯❯❯ curl https://locate.now.sh/ip
127.0.0.1

~ ❯❯❯ wget -qO- https://locate.now.sh/ip/json
{"ip":"127.0.0.1"}
```

### Geolocation lookup

<u>Format:</u>

```
https://locate.now.sh/geo
```

| API URI                                | Type    | Sample Response
| -------------------------------------- | ------- | -------------  
| `https://locate.now.sh/geo`            | `json`  | `{"range":[532553667,543523605],"country":"GB","region":"H8","city":"Liverpool","ll":[51.4157,-3],"metro":0,"zip":0}`

<u>Examples:</u>

```
~ ❯❯❯ curl https://locate.now.sh/geo
{"range":[532553667,543523605],"country":"GB","region":"H8","city":"Liverpool","ll":[51.4157,-3],"metro":0,"zip":0}`

~ ❯❯❯ wget -qO- https://locate.now.sh/geo
{"range":[532553667,543523605],"country":"GB","region":"H8","city":"Liverpool","ll":[51.4157,-3],"metro":0,"zip":0}`
```


<br>

# Installation & Configuration

Clone the repository and install all dependencies by running:

```
~ ❯❯❯ git clone https://github.com/k4m4/locate.now
~ ❯❯❯ cd locate.now/
~/locate.now ❯❯❯ npm install
```

Subsequently, create a `.env` file and declare a variable called `SECRET` (for session security purposes):

```
~/locate.now ❯❯❯ echo "SECRET=[your-secret-goes-here]" > .env
~/locate.now ❯❯❯ npm start
```

You can then access the service by navigating to [`localhost:3000`](http://localhost:3000/).


<br>

# Deployment

First, [download `now`](https://zeit.co/download):

```
~ ❯❯❯ npm install -g now
```

Then, run `now` from *within* the directory of locate.now:

```
~/locate.now ❯❯❯ now
```


<br>

# Credits

- locate.now was developed as part of my Node.js learning experience. I have uploaded the code with the intention of helping out others who are also trying to learn the node environment.
- Most of the styling was adapted from [Evil Rabbit](https://twitter.com/evilrabbit_)'s [front site](https://github.com/evilrabbit/front).


<br>

# License

Copyright (c) 2018 by Nikolaos Kamarinakis. Some rights reserved.

`locate.now` is under the terms of the **MIT License**, following all clarifications stated in the [license file](license.md).

For more information on this project you can go ahead and email me anytime at **nikolaskam{at}gmail{dot}com**.