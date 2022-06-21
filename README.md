# High Performance Machine Learning with NVIDIA CUDA API Parallelization
This repository provides a Google Colab with an ML pipeline to simulate concurrency. 

## Requirements

**Direct Setup** <br>
To run the code in Colab follow the **RAPIDS cuML API - Colab Setup** section. <br>
<br>

## TODO

1.   Setup python logger in Colab
2.   Change logs from <code>print</code> to <code>logger.INFO</code>
3.   In the <code>main</code> function, add a <code>is_simulation</code> boolean parameter
4.   Turn off logger in the simulation pipeline
5.   Append pipeline results to a DataFrame and display results in a tabular format with the following schema:
     ```python
     is_gpu_accelerated (boolean)
     ml_runtime (float64)
     optimization_runtime (float64)
     sample_size (str)
     gpu_cpu_ratio (float64)
     ```
     
 ## Next Steps
 
 


