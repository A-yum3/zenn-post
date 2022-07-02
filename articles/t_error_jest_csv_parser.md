---
title: "csv-parseをimportするとjest実行時にModuleが見つからない問題"
emoji: "🃏"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["Jest"]
published: true
---

## 問題

```ts
import {parse} from "csv-parse/sync";
```

以上のようなimportを行うと`Cannot find module 'csv-parse/sync' from ...`が起こる問題

`Cannot find module 'csv-stringify/sync' from ...`でも同様（というかnode-csvがよくなさそう？）

https://github.com/adaltas/node-csv/issues/309

## 発現環境

- `"ts-jest": "^27.1.4"`
- `"jest": "^27.5.1"`
- `"@types/jest": "^27.5.0"`
- `"csv-parse": "^5.0.4"`
- `"@types/csv-parse": "^1.2.2"`
- `"ts-node": "^9.1.1"`
- `"@types/node": "^14.18.12"`
- `"typescript": "^4.6.3"`

## 解決策

`jest.config.js`にMappingを追加する

```js
module.exports = {  
	...
    "moduleNameMapper": {  
        "^csv-parse/sync": '<rootDir>/node_modules/csv-parse/dist/cjs/sync.cjs'  
    },  
}
```