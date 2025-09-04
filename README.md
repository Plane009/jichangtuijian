QQMusicApi

快速上手
Node 服务
git clone git@github.com:jsososo/QQMusicApi.git

yarn

yarn start
Docker
yarn build:docker

yarn start:docker
npm
yarn add qq-music-api

const qqMusic = require('qq-music-api');

// 部分接口依赖 cookie, 这里穿参可以使用字符串或对象
qqMusic.setCookie('xxx=xxx; xxx=xxx;');
// or
qqMusic.setCookie({ a: 'xxx', b: 'xxx' });

qqMusic.api('search', { key: '周杰伦' })
    .then(res => console.log(res))
    .catch(err => console.log('接口调用出错'))

qqMusic.api('search', { key: '周杰伦' })
    .then((res) => console.log('搜索周杰伦：', res))
    .catch(err => console.log('接口调用出错'))

qqMusic.api('search/hot')
    .then((res) => console.log('热搜词：', res))
    .catch(err => console.log('接口调用出错'))//

// 刷新登陆
qqMusic.api('user/refresh')
