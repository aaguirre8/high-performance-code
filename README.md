[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]




## High Performance Machine Learning with NVIDIA CUDA API Parallelization
This repository provides a Google Colab with an ML pipeline to simulate concurrency. 

### Prerequisites

1.   Set *Runtime Type* to *GPU*
2.   Check if the allocated GPU is Tesla T4, P4, or P100. If not, reset the runtime until one of those GPUs have been allocated.
     ```python
     !nvidia-smi
     ```
3.   Get RAPIDS-Colab files
     ```python
     # This get the RAPIDS-Colab install files and test check your GPU.  Run this and the next cell only.
     # Please read the output of this cell.  If your Colab Instance is not RAPIDS compatible, it will warn you and give you remediation steps.
     !git clone https://github.com/rapidsai/rapidsai-csp-utils.git
     !python rapidsai-csp-utils/colab/env-check.py
     ```
4.   Update the Colab environment
     ```python
     # This will update the Colab environment and restart the kernel.  Don't run the next cell until you see the session crash.
     !bash rapidsai-csp-utils/colab/update_gcc.sh
     import os
     os._exit(00)
     ```
5.   Install CondaColab
     ```python
     # This will install CondaColab.  This will restart your kernel one last time.  Run this cell by itself and only run the next cell once you see the session crash.
     import condacolab
     condacolab.install()
     ```
6.   Install RAPIDS
     ```python
     # NOTE: THIS PROCESS MAY TAKE BETWEEN 15 MINS TO 30 MINS

     # Installing RAPIDS is now 'python rapidsai-csp-utils/colab/install_rapids.py <release> <packages>'
     # The <release> options are 'stable' and 'nightly'.  Leaving it blank or adding any other words will default to stable.
     !python rapidsai-csp-utils/colab/install_rapids.py stable
     import os
     os.environ['NUMBAPRO_NVVM'] = '/usr/local/cuda/nvvm/lib64/libnvvm.so'
     os.environ['NUMBAPRO_LIBDEVICE'] = '/usr/local/cuda/nvvm/libdevice/'
     os.environ['CONDA_PREFIX'] = '/usr/local'
     ```
<p align="right">(<a href="#top">back to top</a>)</p>

## TODO

- [ ] Setup python logger in Colab
- [ ] In the <code>main</code> function, add a <code>is_simulation</code> boolean parameter
- [ ] Change logs from <code>print</code> to <code>logger.INFO</code>
    - [ ] Turn off logger in the simulation pipeline
- [ ] Append pipeline results to a DataFrame and display results in a tabular format with the following schema:
     *   is_gpu_accelerated (boolean)
     *   ml_runtime (float64)
     *   optimization_runtime (float64)
     *   sample_size (str)
     *   gpu_cpu_ratio (float64)

See the [open issues](https://github.com/github_username/repo_name/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>


 ## Next Steps
- [ ] Test the pipeline with [Numba CUDA](https://numba.readthedocs.io/en/stable/cuda/index.html)
- [ ] Refactorize pipeline for Spark ML and test pipeline

<p align="right">(<a href="#top">back to top</a>)</p>


## Contributing

Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/FeatureName`)
3. Commit your Changes (`git commit -m 'Add some FeatureName'`)
4. Push to the Branch (`git push origin feature/FeatureName`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>


## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>


## Contact

Alejandro Aguirre 
Project Link: [https://github.com/aaguirre8/high-performance-code.git](https://github.com/aaguirre8/high-performance-code.git)

<p align="right">(<a href="#top">back to top</a>)</p>


## Acknowledgments

* [Noah Gift](https://www.linkedin.com/in/noahgift/)
* [Duke University](https://duke.edu/)
* [Duke Master in Interdisciplinary Data Science (MIDS)](https://www.linkedin.com/school/dukedatascience/)

<p align="right">(<a href="#top">back to top</a>)</p>

 
 

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/aaguirre8/high-performance-code.git)/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/aaguirrealv


