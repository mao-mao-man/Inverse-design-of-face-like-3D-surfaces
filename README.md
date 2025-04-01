# Inverse-design-of-face-like-3D-surfaces

**Parameterized Polynomial Mask Dataset** is designed for training deep learning models (Fully Convolutional Networks) to establish the relationship between **2D grid design (DesignMatrix5)** and **3D thin-shell structures (Depth Image)**, accelerating the **inverse design** process for geometrically complex and highly personalized objects.

## Dataset Structure

The **`Parameterized Polynomial Mask Dataset`** folder contains **100,000 mask design records**, with **50 records** publicly available for use. Each `.npy` file corresponds to **a unique mask design**, indicated by the filename.

Each `.npy` file includes **both 2DImage and DesignMatrix5** data.

## Dataset Content

Each `.npy` file contains **two main components**:

### 1. 2DImage (Depth Image)
- Format: **2D array (height, width)**
- Data type: `float`
- Content: Each pixel value represents depth information in the image, stored as a **grayscale image**.
- Value range: Depends on the image encoding method.

### 2. DesignMatrix5 (Design Matrix)
- Format: **3D array (height, width, 5)**
- Data type: `float`
- Content: Each pixel location is represented by a **5D one-hot encoded vector**, indicating the corresponding design category.
- Design categories (0~4):
  - `[1., 0., 0., 0., 0.]` represents **no grid unit** (design category 0)
  - `[0., 1., 0., 0., 0.]` represents **grid unit for freely deformation** (design category 1)
  - `[0., 0., 1., 0., 0.]` represents **grid unit for shrinkage** (design category 2)
  - `[0., 0., 0., 1., 0.]` represents **grid unit for curve down** (design category 3)
  - `[0., 0., 0., 0., 1.]` represents **grid unit for curve up** (design category 4)



## Primary Applications

- **Deep learning modeling** (FCN)
- **Image-based inverse design**
- **Machine learning analysis**
- **Research on combining depth images with 3D design matrices**

This dataset enhances **data usability and storage efficiency**, making it suitable for **machine learning** and **design analysis** tasks.

