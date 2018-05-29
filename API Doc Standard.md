**_Python API Definition_**

```python
def fc(input,
       size,
       num_flatten_dims=1,
       param_attr=None,
       bias_attr=None,
       use_cudnn=False,
       use_mkldnn=False,
       act=None,
       is_test=False,
       name=None):
 ```

**_Name_**

```python
    **Fully Connected Layer**
```

**_Function Description_**

```python
   The fully connected layer takes multiple tensors as input. For each tensor,
   the fully connected layer creates "weights", a fully connected weight matrix from
   input units to output units. Then, the layer produces an output tensor by
   multiplying the input tensors to their corresponding weights and adding up the
   results. If bias_attr is not "None", a bias variable will be created and added
   to the output. If activation is not "None", the bias variable will be added to
   the output as well.
```

**_Reference(Optional)_**


   Set use_peepholes to False to disable peephole connection. The formula is
   omitted here, please refer to the paper
   http://www.bioinf.jku.at/publications/older/2604.pdf for details.

**_Formula(Optional)_**

```python
    This process can be formulated as follows:
    .. math::
        Out = Act({\sum_{i=0}^{N-1}X_iW_i + b})
    In the above equation:
    * :math:`N`: Number of the input.
    * :math:`X_i`: The input tensor.
    * :math:`W`: The weights created by this layer.
    * :math:`b`: The bias parameter created by this layer (if needed).
    * :math:`Act`: The activation function.
    * :math:`Out`: The output tensor.
```

**_Args(optional)_**

```python
    Args:
        input (Variable|list of Variable): The input tensor(s) of this layer, and the dimension of
            the input tensor(s) is at least 2.
        size(int): The number of output units in this layer.
        num_flatten_dims (int, default 1): The fc layer can accept an input tensor with more than
            two dimensions. If this happens, the multidimensional tensor will first be flattened
            into a 2-dimensional matrix. The parameter `num_flatten_dims` determines how the input
            tensor is flattened: the first `num_flatten_dims` (inclusive, index starts from 1)
            dimensions will be flatten to form the first dimension of the final matrix (height of
            the matrix), and the rest `rank(X) - num_flatten_dims` dimensions are flattened to
            form the second dimension of the final matrix (width of the matrix). For example, suppose
            `X` is a 6-dimensional tensor with a shape [2, 3, 4, 5, 6], and `num_flatten_dims` = 3.
            Then, the flattened matrix will have a shape [2 x 3 x 4, 5 x 6] = [24, 30].
        param_attr (ParamAttr|list of ParamAttr, default None): The parameter attribute for learnable
            parameters/weights of this layer.
        bias_attr (ParamAttr|list of ParamAttr, default None): The parameter attribute for the bias
            of this layer. If it is set to None, no bias will be added to the output units.
        act (str, default None): Activation to be applied to the output of this layer.
        is_test(bool): A flag indicating whether execution is in test phase.
        use_mkldnn(bool): Use mkldnn kernel or not, it is valid only when the mkldnn
            library is installed. Default: False
        name (str, default None): The name of this layer.
```

**_Returns(Optional)_**

```python
    Returns:
        A tensor variable storing the transformation result.
```
**_Raises(Optional)_**
```python
    Raises:
        ValueError: If rank of the input tensor is less than 2.
```
**_NOTE_**
```python
    NOTE:
        1. When num_heads > 1, three linear projections are learned respectively
        to map input queries, keys and values into queries', keys' and values'.
        queries', keys' and values' have the same shapes with queries, keys
        and values.
        1. When num_heads == 1, scaled_dot_product_attention has no learnable
        parameters.
```

**_Examples_**
```python
    Examples:
        .. code-block:: python
          data = fluid.layers.data(name="data", shape=[32, 32], dtype="float32")
          fc = fluid.layers.fc(input=data, size=1000, act="tanh")
···
