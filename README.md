    in progress
    
    Train with validation (details in tran.py):
    
    Optimizer= adam for at most 3000 epochs or until target values are achieved (accuracy=1, loss=0) with batch size 128. 
    max_size:the maximum size of X_train, size: minimun size of x_train and increment size. 
    target_loss_value is a proxy for minimun
    
    python train.py --random_labels=False --opt=Adam --max_epcs=3000 --bs=128 --max_size=1024 --size=128 --target_loss_value=0.00001 --seed=False --path='/home/mariele/PycharmProjects/generalization/'

# Generalization of Neural Networks

### Studying the L2-norm and the Loss curvature in experiments with correct and random labeling of MNIST data.


Neural Networks generalize unreasonably well. They can have very high capacity, but some inner mechanism greatly prevents it from overfitting. In other words, NN's exhibit intrinsic regularization. While this phenomeon is not completely understood, there have been attempts in identifying Neural Networks' properties which, at least, trace its *effective* capacity. 

An experiment which highlights key features of NN's generalization (1611.03530) compares the performance in classification of a NN trained with correct labels versus a NN trained with randomized labels. When labels are randomized, training can be successfull as long as there are as many parameters as data points, and the NN uses its capacity to memorize the data set. Naturally, performance on the test set is as good as random guess. This shows that intrinsic regularization of NN's cannot be explained by uniform stability of Stochastic Gradient Descent, or some capacity measure, as the Vapnik-Chervonenkis dimension. Here we look into to Neural Networks properties which differ with training with correct or random labels. In other words, we investigate which are proper quantities to describe the NN's *effective* complexity. 

Recent developments suggest that NN's effective capacity is described by properties of the loss function's, like the Jacobian and the Hessian (curvature). Here we will follow a somewhat historical route and also take a deeper look into the L2-norm, and compare those with results on the curvature in experiments with correct and random labels. 


## Experiment #1 - L2-norm:

MLP with a Flatten layer followed by 2 Dense layers with 16 nodes (followed by relu non-linearitoes), and a Softmax layer. 
We consider training sets with sizes: 112, 224, 384, 672, 1024, and train until training accuracy achieves 100%. 

In the following graphs we compare metrics in the correctly labeled case (blue) and randomly labeled one (orange). The weights have the same initialization in both cases.


 <p align="center">
 <img src="https://github.com/mfmotta/deep_learning_generalization_experiments/blob/master/generalization_1.png"  width=900">
 </p>
