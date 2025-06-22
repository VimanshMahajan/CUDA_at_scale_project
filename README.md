# Gaussian Filtering Tool

A lightweight Python utility to apply **Gaussian blur** to grayscale `.tiff` images using custom kernel convolution via OpenCV and NumPy.

---

## Project Description

This script provides a clean and modular implementation of **Gaussian filtering** — a widely-used image processing technique for **smoothing, denoising, and pre-processing** images before further analysis.
The program automatically processes all TIFF images from a specified input folder, applies a **5×5 manually-defined Gaussian kernel**, and saves the blurred results in an output folder.

---

## Features

* ✅ Batch processing of `.tiff` and `.tif` images
* ✅ Custom 5x5 Gaussian kernel (normalized)
* ✅ Grayscale image conversion
* ✅ Modular function design for loading, filtering, and saving
* ✅ Automatic folder creation for outputs
* ✅ Clear console feedback for each processed image

---

## Project Structure

```
GaussianFilter/
│
├── input_images/             # Input directory for TIFF images
├── output_images/            # Auto-created output folder for processed images
├── gaussian_filter.py        # Main script file
├── HOW_TO_RUN.txt            # Basic usage instructions
└── README.md                 # You're here!
```

---

## Requirements

* Python 3.6+
* Libraries:

  * `opencv-python`
  * `numpy`

Install dependencies via:

```bash
pip install -r requirements.txt
```

> You can create a `requirements.txt` with:
>
> ```
> numpy
> opencv-python
> ```

---

## ▶How to Run

### 1. Place Input Images

Put your `.tiff` or `.tif` grayscale images inside the `input_images/` folder.

### 2. Run the Script

```bash
python gaussian_filter.py
```

### 3. View Output

Processed and blurred images will be saved in the `output_images/` folder with `_gaussian.tiff` suffix.

---

## Example

| Original (grayscale)                                    | Gaussian Blurred                                         |
| ------------------------------------------------------- | -------------------------------------------------------- |
| ![original](https://via.placeholder.com/150?text=Input) | ![blurred](https://via.placeholder.com/150?text=Blurred) |

*(Replace with real images if available)*

---

## Under the Hood

The Gaussian kernel used:

```
1  4  7  4  1
4 16 26 16  4
7 26 41 26  7
4 16 26 16  4
1  4  7  4  1
```

* Kernel normalized by dividing by 273
* Convolution handled via `cv2.filter2D`

---

## Notes

* Only `.tiff` and `.tif` formats are supported (by design).
* If any image fails to load or save, the error will be shown in the terminal.
