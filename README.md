# Real-Time-Filtering

A C++ OpenCV application for exploring real-time and image filters with manually implemented computer vision operations (no built-in filter APIs for the core effects).

## Overview

- **vidDisplay.cpp** — Live webcam feed with keyboard-toggled filters.
- **imgDisplay.cpp** — Same filters applied to a single image (for testing).
- **Filter.cpp / Filter.h** — Filter implementations: grayscale, 5×5 blur, Sobel X/Y, magnitude, blur+quantize, cartoon, negative.

## Building

Requires OpenCV (with `highgui`, `imgproc`, `imgcodecs`). Build with your preferred C++ build system (e.g. CMake or compiler command line), linking OpenCV.

## Running

- **Video:** Run the binary that uses `vidDisplay.cpp` (e.g. main from that file). Use keyboard keys to toggle filters; `q` to quit.
- **Image:** Run the binary that uses `imgDisplay.cpp` (ensure the image path in code or via argument points to a valid image).

## Keyboard shortcuts (video / image)

| Key | Effect        |
|-----|---------------|
| `g` | Grayscale (OpenCV) |
| `w` | Grayscale (custom) |
| `b` | Blur 5×5      |
| `x` | Sobel X       |
| `y` | Sobel Y       |
| `m` | Gradient magnitude |
| `i` | Blur + quantize |
| `n` | Negative     |
| `c` | Cartoon      |
| `s` | Save image   |
| `q` | Quit         |

## Filters (brief)

- **Grayscale** — Luminosity: `0.11*B + 0.59*G + 0.3*R`
- **Gaussian blur** — Separable 1×5 horizontal and 5×1 vertical (weights 1,2,4,2,1, normalized).
- **Sobel** — 3×3 Sobel X and Y as separable 1×3 filters; gradient magnitude via `sqrt(sx² + sy²)`.
- **Blur + quantize** — 5×5 blur then color quantization by levels.
- **Cartoon** — Blur+quantize plus edge mask from gradient magnitude threshold.
- **Negative** — Per channel: `255 - pixel`.

![Grayscale](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/9bab7ea3-0486-478e-b638-5325a5b7b968)
![Gaussian](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/d5d42f42-2c9d-4ec9-9b14-167d1bd64d64)
![Sobel](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/d64e21c6-078d-482b-b0f6-4cf0243c6cd3)
![Blur & Quantize](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/6aa0b838-1f98-4fb6-98c0-e6411e894a74)
![Cartoon](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/ead59db0-8adb-43b2-b9b7-324ec769150a)
![Negative](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/2ca6f1cb-db5f-495b-9d0b-d3c16156207b)

