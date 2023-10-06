.. _kw_lambda_1:
.. index::
   single: lambda_1 (keyword in nep.in)

:attr:`lambda_1`
================

This keyword sets the weight :math:`\lambda_1` of the :math:`\mathcal{L}_1`-norm regularization term in the :ref:`loss function <nep_loss_function>`.
The syntax is::

  lambda_1 <weight>

Here, :attr:`<weight>` represents :math:`\lambda_1`, which can be set to any non-negative values. 
However, the default value is :math:`\lambda_1 = -1`, which means that it will be automatically determined based on the actual loss terms for the physical quantities. 
We have tested that the default is quite optimal, but the users can also test manually chosen values. 
In practice, one can first estimate the weighted sum of the loss terms for the target quantities upon convergence and then set :math:`\lambda_1` to that value. 
For example, if one estimates the weighted sum of the loss terms for energy, force, and virial to be :math:`0.01 + 0.1 + 0.01`, then it is reasonable to set :math:`\lambda_1 = 0.12`.
