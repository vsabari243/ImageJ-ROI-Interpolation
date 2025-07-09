# ImageJ-ROI-Interpolation
Macro for interpolating ROIs across slices in ImageJ

# ImageJ Macro: Interpolate ROIs Across Slices

This ImageJ macro loops through all slices in an image stack and checks whether each slice contains any non-empty content (i.e., maximum pixel value = 255). If so, it creates a selection and adds it to the ROI Manager. At the end, it automatically interpolates ROIs across slices with empty gaps in between.

## 🔧 Features

- Automatically scans all slices in the stack.
- Selects slices with content (max pixel = 255).
- Adds those selections as ROIs to the ROI Manager.
- Interpolates between added ROIs to fill in gaps across slices.

## 🖥 Usage Instructions

1. Open your image stack in **ImageJ** or **Fiji**.
2. Ensure your image is thresholded or binarised if needed (i.e., areas of interest should have pixel values of 255).
3. Open the macro file (`interpolate_slices.ijm`) in the macro editor.
4. Run the macro (`Run > Run Macro`).
5. The ROIs will appear in the ROI Manager, and interpolated ROIs will be generated.

## 📌 Notes

- The macro assumes that slices with maximum pixel intensity of 255 contain meaningful content.
- ROIs are only added on slices where this condition is met.
- Interpolation occurs between all detected ROIs, even across multiple empty slices.
- If fewer than two ROIs are detected, interpolation is skipped.

## 📁 Files

- `interpolate_slices.ijm`: The main macro script for selection and interpolation.



