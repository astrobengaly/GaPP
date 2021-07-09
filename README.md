# GaPP
This Gaussian Processes GaPP code auxiliary repository, replacing the original link [http://www.acgc.uct.ac.za/~seikel/GAPP/index.html] which seems to be broken.  

GaPP was written by Seikel, Clarkson, Smith 2012 (https://arxiv.org/abs/1204.2832, JCAP06(2012)036). The algorithm Gaussian processes can reconstruct a function from a sample of data without assuming a parameterization of the function. The GaPP code can be used on any dataset to reconstruct a function. It handles individual error bars on the data and can be used to determine the derivatives of the reconstructed function. The data sample can consists on observations of the function and of its first derivative. 

After downloading and unziping the GaPP file, GaPP can be set up following the documentation in the same folder. 

Questions about GaPP can be addressed to carlosap87@gmail.com or carlosbengaly@on.br

ps: some people have previously reported a bug when running the gp and dgp modules. Some possible solutions are: 

if (self.alpha == None): in dpg.py
had to be changed to
if (np.any(self.alpha) == None):

Thanks Shantanu Desai for that. 

Please change if (self.alpha == None): to 'if (self.alpha == None).all():' in gapp/gp.py and gapp/dgp.py

Thanks to Ian Jhon for verifying this. 
