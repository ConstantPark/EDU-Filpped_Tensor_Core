이 게시물은 모두의 연구소 풀잎스쿨 8기 CUDA 강의에서 사용되었습니다.  
(https://github.com/NVIDIA-developer-blog/code-samples/tree/master/posts/tensor-cores 자료를 참고하여 수정하였습니다.)  
(This git page is based on this git page, https://github.com/NVIDIA-developer-blog/code-samples/tree/master/posts/tensor-cores)

사전에 설치되어야 하는 것들 (Prerequisites)
=============

* C++11을 지원하는 컴파일러가 필요합니다 (Visual Studio, GCC)
* CUDA (9.0 이상) 
* 텐서 코어를 내장하고 있는 GPU

컴파일 방법 (How to build)
===========

* CMake를 사용하여 컴파일 합니다.

CMake를 사용하여 컴파일 하는 과정은 다음과 같습니다.
```bash
~: $ nvcc -o TCGemm -arch=sm_70 -lcublas -lcurand simpleTensorCoreGEMM.cu
```

Running
=======

* build 폴더 내부에 MNIST의 데이터를 넣어두었습니다. 그냥 실행하시면 됩니다.  
* 컴파일 후에 생성된 바이너리가 있는 폴더 (build)에 MNIST의 데이터가 필요합니다.
* 이후 자동적으로 실행이 됩니다.
* Volta (V100) 기준으로 0.76ms, TitanX에서 1.54ms, P100에서 1.14ms가 소요됩니다.
