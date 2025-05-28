# ContentAwareResize

A C# implementation of the Seam Carving algorithm for content-aware image resizing. Intelligently resizes images by removing or inserting low-energy seams while preserving important content.

## ✨ Features

- ✂️ **Content-aware resizing** (horizontal/vertical)  
- 🎯 **Object removal** with optional masking  
- ⚡ **Efficient dynamic programming** (O(W×H) per seam)  
- 📊 **Customizable energy maps** (gradient-based)  

## 🛠️ Installation

```bash
git clone https://github.com/Dowiny/ContentAwareResize.git
cd ContentAwareResize
```

1. Open the solution in **Visual Studio** (requires **.NET 6.0+**).  
2. Install NuGet dependency: `System.Drawing.Common`  
3. Build the project.

## 🚀 Usage

```csharp
using ContentAwareResize;

// Initialize with image
var carver = new SeamCarver("input.jpg");

// Reduce width by 100 pixels
carver.Resize(width: carver.Width - 100);

// Save output
carver.Save("output.jpg");
```

## ✅ Requirements

- .NET 6.0 or higher  
- NuGet: `System.Drawing.Common`  
- **Windows** (for `System.Drawing.Common` compatibility)  

## 🖼️ Example

**Input → Output** 

| Before (`Dolphin.bmp`) | After (`ta.bmp`) |
|------------------------|------------------|
| ![Before](ContentAwareResize/ImgsTestCases/Dolphin.bmp) | ![After](ContentAwareResize/ImgsTestCases/ta.bmp) |


## 📄 License

[MIT License](LICENSE)
