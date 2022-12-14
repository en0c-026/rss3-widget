# RSS3 Widget

Integrate an RSS3 widget in your web application

[https://en0c-026.github.io/rss3-widget/](https://en0c-026.github.io/rss3-widget/)

## What is RSS3?

RSS3 is an information dissemination protocol for Web3 with the core elements of feed and search. [Learn more.](https://blog.rss3.io)

## Usage


### Dev

```bash
git clone https://github.com/en0c-026/rss3-widget
cd rss3-widget
npm start
```

### Build
```bash
npm build
```

## Insert the widget in your web app

Paste the following code snippet into the html index.
```html
<script>
  (function (w, d, s, o, f, js, fjs) {
      w[o] = w[o] || function () { (w[o].q = w[o].q || []).push(arguments) };
      js = d.createElement(s), fjs = d.getElementsByTagName(s)[0];
      js.id = o; js.src = f; js.async = 1; fjs.parentNode.insertBefore(js, fjs);
  }(window, document, 'script', '_hw', 'https://djgn4fxgb4icu.cloudfront.net/index.js'));
  _hw(
    'init',
    // Options object, here you must setup the feed options
    { 
      accounts: ["vitalik.eth"],
    }
    );
</script>

```

To render the widget there must be an html element with the id "rss3-widget".
```html
<div id="rss3-widget"></div>
```


## Options

| **option**      | **type** | **description**                                                                                                                    | default                    |
|-----------------|----------|------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| disableDarkMode | boolean  | Turn off dark mode                                                                                                                 | false                      |
| debug           | boolean  | Enable debug mode for API calls                                                                                                    | false                      |
| serviceBaseUrl  | string   | Base url for RSS3 API                                                                                                              | https://pregod.rss3.dev/v1 |
| accounts        | string[] | List of addresses or ENS handles to obtain the feeding data                                                                        |                            |
| limit           | number   | Limit number of items to get per call                                                                                              | 10                         |
| networks        | string[] | List of platforms to filter the data. Accepted values: ethereum, ethereum_classic, binance_smart_chain, polygon, zksync, xdai, arweave, arbitrum, optimism, fantom, avalanche.                   |                            |
| tags            | string[] | List of tags to filter the data. Accepted values: transaction, exchange, collectible, social, donation, governance.                |                            |
| platforms       | string[] | List of platforms to filter the data. Accepted values: mirror, gitcoin, snapshot, uniswap, binance. |                            |
