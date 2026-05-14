# study-three.js

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A collection of Three.js experiments exploring WebGL rendering, custom shaders, and GPU-accelerated computation techniques.

## Experiments

Each experiment is a self-contained HTML file. Click the "Live Demo" link to see it in action.

### #1 Simple Particles
A CPU-based particle system where thousands of particles are attracted to a central, rotating icosahedron.

[Live Demo](https://aadebdeb.github.io/study-three.js/simple-particles.html)


![Animation of particles swarming around a central geometric shape](https://aadebdeb.github.io/study-three.js/screenshots/simple-particles.png)


### #2 ShaderMaterial with Lighting
Demonstrates a custom `ShaderMaterial` that correctly interacts with Three.js lighting. A dynamic, wave-like color pattern animates across the surfaces of various geometric shapes.

[Live Demo](https://aadebdeb.github.io/study-three.js/shadermaterial-with-lighting.html)


![Geometric shapes with a yellow and green wavy pattern reacting to light](https://aadebdeb.github.io/study-three.js/screenshots/shadermaterial-with-lighting.png)


### #3 GPGPU Life Game
A GPU-accelerated implementation of Conway's Game of Life, simulating the cellular automaton's rules entirely within a fragment shader for high performance.

[Live Demo](https://aadebdeb.github.io/study-three.js/gpgpu-life-game.html)


![A grid showing green cells evolving according to the rules of Conway's Game of Life](https://aadebdeb.github.io/study-three.js/screenshots/gpgpu-life-game.png)


### #4 Background Shader
A full-screen animated background created with a single fragment shader, producing a colorful, flowing, and seamless procedural texture.

[Live Demo](https://aadebdeb.github.io/study-three.js/background-shader.html)


![A colorful, abstract, fluid-like pattern in motion](https://aadebdeb.github.io/study-three.js/screenshots/background-shader.png)


### #5 GPGPU Particles with Curl Noise
A large-scale particle system where movement is driven by curl noise calculated on the GPU. This technique creates complex, turbulent, and natural-looking fluid motion.

[Live Demo](https://aadebdeb.github.io/study-three.js/gpgpu-particles-with-curl-noise.html)


![A dense field of white particles flowing in complex, swirling patterns against a dark background](https://aadebdeb.github.io/study-three.js/screenshots/gpgpu-particles-with-curl-noise.png)


### #6 Smoke Advection with Curl Noise
A GPGPU simulation of smoke, where the velocity field is driven by curl noise. This demonstrates a texture-based advection technique to create realistic swirling smoke patterns.

[Live Demo](https://aadebdeb.github.io/study-three.js/smoke-advection-with-curl-noise.html)


![Wispy, colorful smoke-like patterns swirling against a dark background](https://aadebdeb.github.io/study-three.js/screenshots/smoke-advection-with-curl-noise.png)


### #7 Interaction with GPGPU Particles and Mouse
An interactive GPGPU particle system that reacts to mouse movement. The cursor "pushes" the particles, creating trails and disturbances in the swarm in real-time.

[Live Demo](https://aadebdeb.github.io/study-three.js/interaction-with-gpgpu-particles-and-mouse.html)


![A swarm of particles being pushed and swirled by an unseen mouse cursor](https://aadebdeb.github.io/study-three.js/screenshots/interaction-with-gpgpu-particles-and-mouse.png)


### #8 Raymarching with three.js Camera
A custom raymarching renderer implemented in a fragment shader. The scene is rendered twice for comparison: the top view uses standard Three.js rasterization, while the bottom view uses raymarching. The camera is synchronized between both.

[Live Demo](https://aadebdeb.github.io/study-three.js/raymarching-with-threejs-camera.html)


![A split-screen view showing a 3D scene rendered with both rasterization and raymarching](https://aadebdeb.github.io/study-three.js/screenshots/raymarching-with-threejs-camera.png)


### #9 Interaction with Smoke and Mouse
An interactive fluid simulation where the user's mouse stirs and injects "dye" into the fluid, creating colorful, swirling patterns reminiscent of ink in water.

[Live Demo](https://aadebdeb.github.io/study-three.js/interaction-with-smoke-and-mouse.html)


![Colorful smoke being swirled and mixed by an unseen mouse cursor](https://aadebdeb.github.io/study-three.js/screenshots/interaction-with-smoke-and-mouse.png)


### #10 Fluid Webcam with Mouse Interaction
A real-time fluid simulation that uses live webcam input as its color source. The fluid can be disturbed with the mouse, causing the webcam image to warp and flow.

[Live Demo](https://aadebdeb.github.io/study-three.js/fluid-webcam-with-mouse-interaction.html)

## Running Locally

No build step is required. To run these experiments on your local machine:

1.  Clone the repository:
    ```sh
    git clone https://github.com/aadebdeb/study-three.js.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd study-three.js
    ```
3.  Start a simple local web server. For example, using Python 3:
    ```sh
    python -m http.server
    ```
4.  Open your browser and navigate to `http://localhost:8000`, then click on any of the `.html` files.

## Core Libraries & Utilities

This project relies on several key libraries and helper files, all included in the `/js` directory:

*   **[three.js](https://threejs.org/)**: The core 3D graphics library.
*   **GPUComputationRenderer.js**: A helper class from the Three.js examples for performing GPGPU computations.
*   **OrbitControls.js**: A camera controller for interactive 3D navigation.
*   **[dat.GUI](https://github.com/dataarts/dat.gui)**: A lightweight GUI for changing parameters in real-time.
*   **[Stats.js](https://github.com/mrdoob/stats.js/)**: A simple performance monitor.
