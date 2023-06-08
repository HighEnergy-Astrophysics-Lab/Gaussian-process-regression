# Gaussian-process-regression
(attached notebook deals with "Application of GPR on yearly averaged sunspot prediction")
Change the file_path to your local system's file path.




# some useful resources for GPR : 
#1 https://scikit-learn.org/stable/modules/gaussian_process.html                              :   FOR GPR SCIKIT LEARN CODE
#2 https://www.dominodatalab.com/blog/fitting-gaussian-process-models-python                  :   FOR BUILDING GPR CODE FROM SCRATCH 
#3 https://youtu.be/92-98SYOdlY                                                               :  FOR BASIC UNDERSTANDING OF THEORY OF GPR





# some useful changes in scikit-learn code (already implemented in the attached notebook) : 

#1   It is important to normalize the y variable, so as to maintain consistency with the GPR model, "normalize_y" parameter in "gaussian_process = GaussianProcessRegressor(kernel=kernel,alpha=          (np.array(y_err).flatten())**2, normalize_y=True , n_restarts_optimizer=100)" does not normalise the errors. Hence, y_err is divided by standard deviation of the training data.

#2   "bounds for hyper-parameters" are usually set as default between  1e5 - 1e-5  in scikit-learn. It has been changed to, MINIMUM BOUND = minimum resolution of the time-series, and , MAXIMUM           BOUND= total time span of the time-series. Refer to https://betanalpha.github.io/assets/case_studies/gaussian_processes.html  for more details.
