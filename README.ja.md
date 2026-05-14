# study-three.js

Three.jsを用いたWebGLレンダリング、カスタムシェーダー、GPUを活用した計算技術を探求する実験のコレクションです。

## Experiments

各実験は独立したHTMLファイルになっています。「ライブデモ」のリンクをクリックして実際の動作を確認してください。

### #1 Simple Particles
CPUベースのパーティクルシステムです。数千のパーティクルが中央の回転する二十面体に引き寄せられます。

[Live Demo](https://aadebdeb.github.io/study-three.js/simple-particles.html)

![中央の幾何学的な形状の周りに群がるパーティクルのアニメーション](https://aadebdeb.github.io/study-three.js/screenshots/simple-particles.png)

### #2 ShaderMaterial with Lighting
Three.jsのライティングと正しく相互作用するカスタム `ShaderMaterial` のデモです。さまざまな幾何学的な形状の表面で、波のような動的なカラーパターンがアニメーションします。

[Live Demo](https://aadebdeb.github.io/study-three.js/shadermaterial-with-lighting.html)

![光に反応する黄色と緑の波状パターンを持つ幾何学的な形状](https://aadebdeb.github.io/study-three.js/screenshots/shadermaterial-with-lighting.png)

### #3 GPGPU Life Game
コンウェイのライフゲームをGPUアクセラレーションで実装したものです。高いパフォーマンスを実現するため、セルオートマトンのルールをすべてフラグメントシェーダー内でシミュレーションしています。

[Live Demo](https://aadebdeb.github.io/study-three.js/gpgpu-life-game.html)

![コンウェイのライフゲームのルールに従って進化する緑色のセルを示すグリッド](https://aadebdeb.github.io/study-three.js/screenshots/gpgpu-life-game.png)

### #4 Background Shader
単一のフラグメントシェーダーで作成されたフルスクリーンのアニメーション背景です。カラフルで流れるような、シームレスなプロシージャルテクスチャを生成します。

[Live Demo](https://aadebdeb.github.io/study-three.js/background-shader.html)

![動いているカラフルで抽象的な流体のようなパターン](https://aadebdeb.github.io/study-three.js/screenshots/background-shader.png)

### #5 GPGPU Particles with Curl Noise
GPU上で計算されたカールノイズによって動きが制御される大規模なパーティクルシステムです。この手法により、複雑で乱れのある、自然な流体の動きを作り出します。

[Live Demo](https://aadebdeb.github.io/study-three.js/gpgpu-particles-with-curl-noise.html)

![暗い背景に対して複雑に渦巻くパターンで流れる白いパーティクルの密集したフィールド](https://aadebdeb.github.io/study-three.js/screenshots/gpgpu-particles-with-curl-noise.png)

### #6 Smoke Advection with Curl Noise
カールノイズによって速度場が制御される煙のGPGPUシミュレーションです。テクスチャベースのアドベクション（移流）技術を用いて、リアルに渦巻く煙のパターンを生成するデモです。

[Live Demo](https://aadebdeb.github.io/study-three.js/smoke-advection-with-curl-noise.html)

![暗い背景に対して渦巻く、かすかでカラフルな煙のようなパターン](https://aadebdeb.github.io/study-three.js/screenshots/smoke-advection-with-curl-noise.png)

### #7 Interaction with GPGPU Particles and Mouse
マウスの動きに反応するインタラクティブなGPGPUパーティクルシステムです。カーソルがパーティクルを「押しのける」ことで、群れの中に軌跡や乱れをリアルタイムに作り出します。

[Live Demo](https://aadebdeb.github.io/study-three.js/interaction-with-gpgpu-particles-and-mouse.html)

![見えないマウスカーソルによって押し流され、渦巻くパーティクルの群れ](https://aadebdeb.github.io/study-three.js/screenshots/interaction-with-gpgpu-particles-and-mouse.png)

### #8 Raymarching with three.js Camera
フラグメントシェーダーで実装されたカスタムレイマーチングレンダラーです。比較のため、シーンは2回レンダリングされます。上部のビューは標準のThree.jsのラスタライゼーションを使用し、下部のビューはレイマーチングを使用しています。両方のビューでカメラは同期されています。

[Live Demo](https://aadebdeb.github.io/study-three.js/raymarching-with-threejs-camera.html)

![ラスタライゼーションとレイマーチングの両方でレンダリングされた3Dシーンを示す分割画面ビュー](https://aadebdeb.github.io/study-three.js/screenshots/raymarching-with-threejs-camera.png)

### #9 Interaction with Smoke and Mouse
ユーザーがマウスで流体をかき混ぜたり「染料」を注入したりできる、インタラクティブな流体シミュレーションです。水中に広がるインクを思わせる、カラフルで渦巻くパターンを作り出します。

[Live Demo](https://aadebdeb.github.io/study-three.js/interaction-with-smoke-and-mouse.html)

![見えないマウスカーソルによって渦巻き、混ざり合うカラフルな煙](https://aadebdeb.github.io/study-three.js/screenshots/interaction-with-smoke-and-mouse.png)

### #10 Fluid Webcam with Mouse Interaction
ウェブカメラのライブ入力をカラーソースとして使用する、リアルタイムの流体シミュレーションです。マウスで流体をかき乱すことができ、ウェブカメラの映像が歪んで流れるような効果を生み出します。

[Live Demo](https://aadebdeb.github.io/study-three.js/fluid-webcam-with-mouse-interaction.html)

## Running Locally

ビルドステップは不要です。ローカルマシンでこれらの実験を実行するには、以下の手順に従ってください。

1.  リポジトリをクローンします:
    ```sh
    git clone https://github.com/aadebdeb/study-three.js.git
    ```
2.  プロジェクトディレクトリに移動します:
    ```sh
    cd study-three.js
    ```
3.  シンプルなローカルウェブサーバーを起動します。たとえばPython 3を使用する場合:
    ```sh
    python -m http.server
    ```
4.  ブラウザを開いて `http://localhost:8000` にアクセスし、任意の `.html` ファイルをクリックします。

## Core Libraries & Utilities

このプロジェクトは、いくつかの主要なライブラリとヘルパーファイルに依存しており、すべて `/js` ディレクトリに含まれています。

*   **[three.js](https://threejs.org/)**: コアとなる3Dグラフィックスライブラリ。
*   **GPUComputationRenderer.js**: GPGPU計算を実行するための、Three.jsのサンプルに含まれるヘルパークラス。
*   **OrbitControls.js**: インタラクティブな3Dナビゲーションのためのカメラコントローラー。
*   **[dat.GUI](https://github.com/dataarts/dat.gui)**: パラメータをリアルタイムで変更するための軽量GUI。
*   **[Stats.js](https://github.com/mrdoob/stats.js/)**: シンプルなパフォーマンスモニター。
