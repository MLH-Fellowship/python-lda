# python-lda

Latent Dirichlet Allocation in Python and Cython.

* The python2 code was written by `hannawallach`
* The Cython implementation and benchmarking were written by `joshuacwnewton`
* The code was converted to python3 and the instructions were written by `parthivc`

## Instructions

Clone the repository by entering the following command: `git clone git@github.com:MLH-Fellowship/python-lda.git`

Then, run 'pip install Cython numpy matplotlib sklearn`

To benchmark the pure NumPy implementation versus the Cython implementation, run the following code (please note that the benchmark can take several minutes depending on the performance of your computer):

```
cd cython_testing/
./build_and_move.sh 
cd ..
python3 src/preprocess.py newsgroups --output-file data/newsgroups.pkl --remove-stopwords data/stopwords.txt
python3 src/experiment.py -input_file data/newsgroups.pkl -S 100 -T 10
```
