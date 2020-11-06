# A neural network for elastography

> This repo contains models built in the blog posts: *A neural network for elastography [part 1](https://lucas-almeida-r.github.io/blog/neural%20networks/elastography/2020/10/08/elastography_1.html) and [part 2](https://lucas-almeida-r.github.io/blog/neural%20networks/elastography/2020/10/09/elastography_2.html)*.

[Elastography](https://en.wikipedia.org/wiki/Elastography) is a medical imaging modality that informs us about the stiffness of soft tissue. This information is relevant because many diseases form hard tissues. For instance, tumors, thrombus, and diseased liver tissue are usually stiffer than their surrounding tissues.

The basic idea of elastography is to:
1. Apply some deformation in the tissue.
2. Measure how much the tissue displaces. 
3. Calculate the stiffness of the tissue.

Motivated by this application, our goal is to build a model that calculates the stiffness throughout a heterogeneous body given a noisy displacement field generated by uniaxial extension. We use the [Mechanical MNIST](https://open.bu.edu/handle/2144/39371), which is a collection of datasets composed of finite element simulations. The bodies used in the simulations are composed of a hard inclusion immersed in soft material. The inclusions have the form of a handwritten digit from the [MNIST dataset](http://www.pymvpa.org/datadb/mnist.html), which motivates the name Mechanical MNIST.

By the end of [part 2](https://lucas-almeida-r.github.io/blog/neural%20networks/elastography/2020/10/09/elastography_2.html), we have built a model, such as illustrated below. The neural network (a CNN) receives the displacement field as input and outputs the predicted stiffness. In this example, we see that the model was able to outline the inclusion with a good resolution, despite the noise in the displacement field.

<p align="center">
  <img src="https://github.com/lucas-almeida-r/elastography/blob/master/models/model.png" width="500" />
</p>
