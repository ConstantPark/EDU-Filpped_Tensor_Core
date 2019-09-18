이 게시물은 모두의 연구소 풀잎스쿨 8기 CUDA 강의에서 사용되었습니다.  
(https://github.com/NVIDIA-developer-blog/code-samples/tree/master/posts/tensor-cores 자료를 참고하였습니다.)  

사전에 설치되어야 하는 것들 (Prerequisites)
=============

* C++11을 지원하는 컴파일러가 필요합니다 (Visual Studio, GCC)
* CUDA (9.0 이상) 
* 텐서 코어를 내장하고 있는 GPU

컴파일 방법 (How to build)
===========

* Nvcc를 사용하여 컴파일 합니다.

컴파일 하는 과정은 다음과 같습니다.
```bash
: $ nvcc -o TCGemm -arch=sm_70 -lcublas -lcurand simpleTensorCoreGEMM.cu
```
실행 결과는 다음과 같습니다.
```bash
wmma took 689.984497ms, cublas took 96.523262ms
```

