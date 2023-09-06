# プロジェクトの概要

- 以下の初期設定を行ったプロジェクト。
- ESLint
- TailwindCSS
-

# TailwindCSS の設定

`yarn add -D tailwindcss@latest postcss@latest autoprefixer@latest`
`npx tailwindcss --init -p`

tailwind.config.js の設定

- content の設定を以下のように変更

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

index.css に以下のコードを追加

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

`yarn run dev`を実行
App.js で TailwindCSS が使えるか試す

```
function App() {
  return (
    <div className="App">
      <h1 className="test-white bg-blue-200">hello</h1>
    </div>
  );
}
```

## TailwindCSS のテスト

ダークモードの実装で試す

-

## ESLint の設定

`npx eslint --init`
