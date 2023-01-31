#############################
### Training with Pytorch ###
#############################
# Joshuha Thomas-Wilsker
##############################
# A few notes made while
# writing code to create data
# and train DNN in PyTorch


# Tensors
- Specialised data struct similar to arrays and matrices
- Used for model parameters, inputs and outputs
- Similar to ndarrays but can be run on a GPU or other hardware accelerators
- Optimised for automatic differentiation

## Creating data sets
- Data sets are saved as parquet files
- You can not preserve dtypes with a csv. Limitation of using the .csv format
- Parquet preserve dtypes
- also faster to save/load, less disk space, cross platform support (unlike pythons pickle)

- Custom dataset for files needs to implement:
  __init__
      Runs once when instantiating the object to initialise directory with input, target and transforms
  __len__
      Number f entries in our sample
  __getitem__
      Loads and returns a sample from the dataset. Will only be called when we iterate the object


# Models
- Passing input data to model automatically executes models forward method
