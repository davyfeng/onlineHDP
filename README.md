onlineHDP
=========

ONLINE VARIATIONAL BAYES FOR HIERARCHICAL DIRICHLET PROCESS

Cheng Zhang, chengz@kth.se
Xavi Gratal, javiergm@kth.se

(C) Copyright 2013, Cheng Zhang and Xavi Gratal

This is free software, you can redistribute it and/or modify it under
the terms of the GNU General Public License.

The GNU General Public License does not permit this software to be
redistributed in proprietary programs.

This software is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307
USA
________________________________________________________________________

This C++ code implements the online variational bayes for hierachical dirichlet process presented in paper "Online Variational Inference for the Hierarchical Dirichlet Process", Chong Wang John Paisley David M. Blei. This C++ version of the code is implemented based on the python version of the code released by Chong Wang. 


This code requires
Eigen 3 and Boost library

Eigen 3 could be downloaded here:
http://eigen.tuxfamily.org/

Boost could be found here:
http://www.boost.org/



Build instructions:

cd build
cmake ..
make


Example data are provided in the data/ folder. This is the preprocessed Reuters R8 data set. 
Data are presented as wordid:counts, and each line is a document.

Example command line to run the code:

./onlinehdp -t 100 -k 10 -d 5485 -w 23587 -eta 0.1 -alpha 0.1 -gamma 0.1 -tau 0.3 -batchsize 10 -max_time 10000000000 -max_iter 1000 -corpus_name R3 -data_path YOURPATH/data/R8_train_all_terms.dat -test_path YOURPATH/data/R8_test_all_terms.dat -res YOUR_RES_PATH -seq_mode 1 -kappa 0.3 




