# Optimization
# Energy
![equation](http://latex.codecogs.com/gif.latex? E(\\boldsymbol{x})= \\sum_{x=0}^m [f_i(\\boldsymbol{x})]^2 =\\|\\boldsymbol{F}(\\boldsymbol{x})\\|_2^2 \\qquad where \\qquad  \\boldsymbol{F}(\\boldsymbol{x}) = [f_1(\\boldsymbol{x}),...,f_m(\\boldsymbol{x})]^T )

![equation](http://latex.codecogs.com/gif.latex? \\boldsymbol{J}(\\boldsymbol{x}) =\\frac{\\partial\\boldsymbol{F}}{\\partial{\\boldsymbol{x}}} =  [\\frac{\\partial{f_1}}{\\partial{\\boldsymbol{x}}},...,\\frac{\\partial{f_m}}{\\partial{\\boldsymbol{x}}}]^T  )

![equation](http://latex.codecogs.com/gif.latex? \\boldsymbol{F}(\\boldsymbol{x}) =\\boldsymbol{F}(\\boldsymbol{x}_0) +\\boldsymbol{J}(\\boldsymbol{x}_0) \\cdot \\delta_{\\boldsymbol{x}}  )

![equation](http://latex.codecogs.com/gif.latex? \\boldsymbol{Grad}(\\boldsymbol{E(x)}) = \\frac{\\partial\\boldsymbol{E}}{\\partial{\\boldsymbol{x}}} =\\frac{\\partial{(\\boldsymbol{F}^T\\cdot\\boldsymbol{F}} )}{\\partial{\\boldsymbol{x}}} =  \\boldsymbol{F}^T\\cdot\\frac{\\partial\\boldsymbol{F}}{\\partial{\\boldsymbol{x}}} 
= f_1(\\boldsymbol{x})\\cdot\\frac{\\partial{f_1}}{\\partial{\\boldsymbol{x}}}+...+f_m(\\boldsymbol{x})\\cdot\\frac{\\partial{f_m}}{\\partial{\\boldsymbol{x}}} )

# Gauss-Newton method:
   
   ![equation](http://latex.codecogs.com/gif.latex?  \\delta_{\\boldsymbol{x^*_k}} = \\underset{\\boldsymbol{x}_k}{\\mathrm{argmin}}  \\| \\boldsymbol{F}(\\boldsymbol{x}_k) +\\boldsymbol{J}(\\boldsymbol{x}_k) \\cdot \\delta_{\\boldsymbol{x}_k} \\|_2^2  )
   
  ![equation](http://latex.codecogs.com/gif.latex? 2 \\cdot  \\boldsymbol{J}(\\boldsymbol{x^*_k}) \\boldsymbol{J}(\\boldsymbol{x^*_k}) \\delta_{\\boldsymbol{x^*_k}}  =  -2 \\cdot \\boldsymbol{J}(\\boldsymbol{x^*_k})^T \\boldsymbol{F}(\\boldsymbol{x^*_k}) )
  
#Levenberg-Marquardt method:
  ![equation](http://latex.codecogs.com/gif.latex? 2 \\cdot  ( \\boldsymbol{J}(\\boldsymbol{x^*_k}) \\boldsymbol{J}(\\boldsymbol{x^*_k})+
  \\lambda diag (\\boldsymbol{J}(\\boldsymbol{x^*_k}) \\boldsymbol{J}(\\boldsymbol{x^*_k}) ) )
  \\delta_{\\boldsymbol{x^*_k}}  =  -2 \\cdot \\boldsymbol{J}(\\boldsymbol{x^*_k})^T \\boldsymbol{F}(\\boldsymbol{x^*_k}) )
