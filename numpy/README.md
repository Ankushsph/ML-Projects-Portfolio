# NumPy Learning Repository

A comprehensive collection of NumPy tutorials, exercises, and examples for learning array operations and numerical computing in Python.

## 📚 Overview

This repository contains educational materials for mastering NumPy, the fundamental package for scientific computing in Python. It includes practical examples, exercises, and detailed explanations of NumPy's core functionality.

## 📁 Contents

### 1. [numpy.ipynb](numpy.ipynb)
**Comprehensive NumPy Tutorial**
- Basic array creation and manipulation
- Array attributes and methods
- Mathematical operations and functions
- Indexing and slicing techniques
- Boolean indexing
- Reshaping and resizing operations

### 2. [numpy_exercises.ipynb](numpy_exercises.ipynb)
**Hands-on Exercises**
- Practice problems for NumPy concepts
- Step-by-step solutions
- Real-world applications
- Performance optimization techniques

### 3. [array_ops.ipynb](array_ops.ipynb)
**Array Operations Deep Dive**
- Advanced array operations
- Broadcasting concepts
- Memory optimization
- Performance comparisons

## 🎯 Learning Objectives

After completing these tutorials, you will be able to:

- ✅ Create and manipulate NumPy arrays
- ✅ Perform mathematical operations on arrays
- ✅ Use advanced indexing and slicing
- ✅ Apply boolean indexing for data filtering
- ✅ Reshape and resize arrays efficiently
- ✅ Understand array broadcasting
- ✅ Optimize NumPy code for performance

## 🚀 Key Topics Covered

### Basic Array Operations
```python
# Array creation
arr = np.array([1, 2, 3, 4])
arr = np.zeros((4, 8))
arr = np.ones((6, 6))
arr = np.linspace(0, 1, 100)

# Random generation
np.random.rand(10)
np.random.randn(10)
np.random.randint(10, 20, 6)
```

### Array Attributes & Methods
```python
# Array properties
arr.shape    # Dimensions
arr.size     # Total elements
arr.dtype    # Data type

# Mathematical operations
arr.min()    # Minimum value
arr.max()    # Maximum value
arr.sum()    # Sum of elements
arr.mean()   # Mean value
arr.std()    # Standard deviation
```

### Indexing & Slicing
```python
# Vector indexing
arr[9]           # Single element
arr[1:4]         # Slice
arr[3::2]        # Step slicing

# Matrix indexing
arr[0, 0]        # Single element
arr[0:2, 1]      # Row and column slice
arr[:, 2]        # All rows, specific column
```

### Boolean Indexing
```python
# Conditional filtering
bool_index = arr % 2 == 0
arr = arr[bool_index]
```

### Reshaping Operations
```python
# Reshape arrays
arr = np.arange(1, 31)
arr = arr.reshape(6, 5)
```

## 🛠️ Prerequisites

```bash
pip install numpy jupyter matplotlib
```

## 📖 How to Use

1. **Start with Basics**: Begin with `numpy.ipynb` for fundamental concepts
2. **Practice**: Work through `numpy_exercises.ipynb` for hands-on experience
3. **Advanced Topics**: Explore `array_ops.ipynb` for deeper understanding

## 🎓 Educational Structure

### Beginner Level
- Array creation and basic operations
- Simple indexing and slicing
- Basic mathematical functions

### Intermediate Level
- Advanced indexing techniques
- Boolean indexing and filtering
- Array reshaping and manipulation

### Advanced Level
- Broadcasting concepts
- Performance optimization
- Memory-efficient operations

## 📊 Example Applications

### Data Analysis
```python
# Statistical analysis
data = np.random.randn(1000)
mean_val = np.mean(data)
std_val = np.std(data)
```

### Image Processing
```python
# Image manipulation
image = np.random.rand(100, 100, 3)
grayscale = np.mean(image, axis=2)
```

### Scientific Computing
```python
# Mathematical operations
x = np.linspace(0, 2*np.pi, 100)
y = np.sin(x)
```

## 🔧 Performance Tips

1. **Vectorization**: Use NumPy operations instead of loops
2. **Memory Management**: Be mindful of array copying vs. views
3. **Data Types**: Choose appropriate dtypes for memory efficiency
4. **Broadcasting**: Leverage broadcasting for efficient operations

## 📈 Learning Path

```
1. Basic Array Creation → 2. Indexing & Slicing → 3. Mathematical Operations
                                    ↓
4. Boolean Indexing → 5. Reshaping → 6. Advanced Operations
                                    ↓
7. Broadcasting → 8. Performance Optimization → 9. Real-world Applications
```

## 🎯 Target Audience

- **Beginners**: New to NumPy and scientific computing
- **Data Scientists**: Wanting to strengthen NumPy fundamentals
- **Students**: Learning Python for data analysis
- **Developers**: Transitioning to numerical computing

## 📝 Additional Resources

- [NumPy Official Documentation](https://numpy.org/doc/)
- [NumPy User Guide](https://numpy.org/doc/stable/user/index.html)
- [NumPy Tutorial](https://numpy.org/doc/stable/user/quickstart.html)

## 🔗 Related Projects

- [Pandas Data Analysis](../panadas/)
- [Machine Learning Projects](../)

## 📄 License

This educational content is part of the ML Projects Portfolio. See main README for license information.

---

**Author**: Ankushsph  
**GitHub**: [https://github.com/Ankushsph](https://github.com/Ankushsph)  
**Purpose**: Educational resource for NumPy learning
