---
author: prashant
comments: false
date: 2017-08-30 00:00:00+00:00
layout: post
slug: installing-cuda
title: Installing CUDA on Mac OSX
---

For OSX 10.12, you will have to use Xcode 8.2 which comes with Apple LLVM 8.0.0. You can get it installed from [https://developer.apple.com/](https://developer.apple.com/).

Copy the XCode newer executable to the Applications folder. It will mostly create a version called Xcode copy.

Now download and install the Cuda Toolkit from the Nvidia website. You should find it here - [https://developer.nvidia.com/cuda-toolkit](https://developer.nvidia.com/cuda-toolkit).

```shell
sudo xcode-select -s /Applications/Xcode\ copy.app/Contents/Developer
```

The nvcc executable is installed in the `/Developer/NVIDIA/CUDA-8.0/bin/`. Add it to the path in the `~/.zshrc`.

```shell
export PATH="/Developer/NVIDIA/CUDA-8.0/bin/:$PATH"
```

Run a `source ~/.zshrc`, and check if it works.

```shell
nvcc --version
```

Hope this worked!


