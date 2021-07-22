### Section 5 - Pytorch Basics

#### 5.20 & 5.21 - Tensor Basics

    - `torch.from_numpy(arr)` or `torch.as_tensor(arr)` keep a link to the `arr` data underlying, so any modifications to the array are reflected. An alternative is `torch.tensor(arr)`
    - `torch.Tensor` with capital T automatically converts to float (it is an alias for `torch.FloatTensor`), while `torch.tensor` infers the datatype
    - Placeholder tensors with `torch.empty`
    - Tensor of zeros with  `torch.zeros`
    - 64 precision may bog down training time, or some functionalities may not be available for high precision
    - `my_tensor.type(torch.<dtype>)` changes the datatype of a tensor
    - `torch.rand(<shape>)` returns random uniform distributed numbers between 0 and 1
    - `torch.randn(<shape>)` returns random standard normally dstributed numbers, with mean 0 and stddev 1
    - `torch.randint()` returns random integers between low and high
    - `torch.rand_like(<input_tensor>)`, `torch.randn_like(<input_tensor>)`, torch.randint_like(<input_tensor>)` create a tensor with shape of the incoming tensor
    - `torch.manual_seed` sets the seed

#### 5.22 & 5.23 Tensor Operations
    - `Tensor.view()` works similarly to reshape. the view is not a copy of the data, it keeps the underlying data
    - `Tensor.view()` can infer dimensions, sucha as reshape
    - Arithmetic operations in pytorch have a shorthand to assignment, with the `_` at the end. For instance, if we have two tensors `a` and `b`, we can add them by calling `a.add(b)`, which will just return `a + b`, or `a.add_(b)` as a shorthand to `a = a + b`
    - `torch.mm` for matrix multiplication