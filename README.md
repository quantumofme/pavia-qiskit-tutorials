# Pavia Quantum Computing, Quantum Simulations & Qiskit Tutorial - Version 1.0.0

(c) 2019, F. Tacchino, C. Macchiavello, D. Gerace

These Jupyter notebooks were originally designed as support materials for courses in Quantum Computing and Quantum Simulations at the University of Pavia (Department of Physics).
No prior knowledge or experience in quantum computing is assumed, but standard linear algebra, basic quantum mechanics and some acquaintance with
python are required to make these tutorials more useful and interesting.

## Requirements

These notebooks were created and tested under Python 3.6.3 using the Anaconda distribution and the following modules:  
```
qiskit==0.7.0
matplotlib==2.2.2
numpy==1.14.3
scipy==1.1.0
```
To use the latex-based circuit drawing tool, you will also need the `pdflatex` compiler and the Poppler library appropriate for your operating system (see the documentation of the official Qiskit tutorials for more details).
Notice that qiskit is currently under active and fast development, and it might undergo some restyling in the future. Compatibility of 
these tutorials with future releases is attempted but cannot currently be assured.

In order to have access to the cloud-based real IBM quantum processors, you will need an account and an API key on the IBM Quantum Experience 
(https://quantumexperience.ng.bluemix.net/qx/experience).

## Installation

In order to use these notebooks, we suggest you take the following steps.

### Anaconda distribution

Download and install the Anaconda python distribution for your operating system (e.g. from the website <https://www.anaconda.com/>).
This will automatically provide you with most scientific python libraries and the Jupyter notebook editor. For advanced users, we recommend creating
a virtual environment.

### Installing qiskit

Activate your Ananconda distribution from a terminal. In bash, this is usually done by typing
```
source activate
```
In Windows, make sure you have added the Anaconda installation to your `PATH` and use the cmd terminal instead of PowerShell. Usually, in cmd
there is no need to `source` (i.e. the above command is just `activate`). You sould also find a dedicated Anaconda prompt within 
your installation which is already activated.

After activating Anaconda (optionally, your virtual environment), you can install qiskit v0.7.0 by typing
```
pip install qiskit==0.7.0
```
If you do not specify a version, the most recent release will be installed.

### Opening the notebooks in Jupyter

To read these notebooks, just do
```
cd Your/Path/To/pavia-qiskit-tutorials
```
and then
```
jupyter notebook
```
You will be redirected to the Jupyter interface via your browser and you will be able to open the notebook of your interest.

## Usage tips

Here are a few suggestions on how to use these notebooks.

### Interaction with the code 

As any Jupyter notebook, these materials contain interactive code. You are strongly encouraged to run and play with
it to get familiar both with quantum computing concepts and with the qiskit functionalities. In any of the notebooks, if you place your cursor in a cell 
containing code, you can run it by hitting `SHIFT+ENTER`. Remember that the notebooks are written in a sequential fashion, so some of the cells may depend on the successful
execution of some others above them. We suggest you run cells in `Introduction.ipynb` and `Part2.ipynb` one by one, since these notebooks contain interaction with
the IBMQ servers wich can possibly fail or take a long time. On the other hand, `Part1.ipynb` is probably best read after running all cells first.

### Creating a Qconfig.py

Together with the notebooks, you should find a Qconfig_template.py file. Just fill the required fields with your data from the IBM Quantum Experience,
in particular add your personal API key, to be able to connect remotely to the IBMQ services. Rename the file to Qconfig.py before using the notebooks.

### Known bugs

* Some commands, depending on your platform, may raise warnings from the python kernel. They disappear if you run the corresponding cell twice, but you 
can also filter them with the python  `warnings` module.
* The  `execute`/`JobMonitor` part for execution on real backends in  `Introduction.ipynb` and `Part2.ipynb` (Bonus track 2) may raise an error like this 
when ran for the first time on a kernel: 
    ```
    AttributeError: module 'ipywidgets' has no attribute 'GridBox'
    ```
  The error should disappear if you run the cell again on the same kernel.

## References & useful materials

Here we provide a (non exhaustive) list of references that can be useful before, during and after using these notebooks.

__Qiskit references__
1. https://qiskit.org/ [Official qiskit website, with links to tutorials, documentation and other resources.]  
2. https://github.com/Qiskit/ibmq-device-information [GitHub repository with technical details about the IBMQ real backends.]  

__Quantum computation and quantum algorithms__

3. M. A. Nielsen and I. L. Chuang, _Quantum Computation and Quantum Information_ , Cambridge University
Press (2004).  
    [The best place to start your journey in Quantum Computing. Covers both basic and advanced topics.] 
4. A. Barenco _et al._, _Elementary gates for quantum computation_, Phys. Rev. A __52__ 3457, arXiv:quant-ph/9503016 (1995).
5. G. Vidal and C. M. Dawson, _Universal quantum circuit for two-qubit transformations with three controlled-NOT gates_, Phys. Rev. A __69__, 010301(R) (2004).
6. P. J. Coles _et al._, _Quantum Algorithm Implementations for Beginners_, arXiv:1804.03719 (2018).
7. <http://math.nist.gov/quantum/zoo/> (mirrored also at <http://quantumalgorithmzoo.org/>).

__Quantum simulations__

7. R. Feynman, _Simulating physics with computers_, Int. J. Theor. Phys. __21__, 467 (1982). [Feynman's seminal paper on quantum simulations.]
8. S. Lloyd, _Universal Quantum Simulators_, Science __273__, 1073 (1996). [Lloyd's seminal paper on digital quantum simulations.]
9. G. Ortiz _et al._, _Quantum algorithms for fermionic simulations_, Phys. Rev. A __64__, 022319 (2001).
10. R. Somma _et al._, _Simulating Physical Phenomena by Quantum Networks_, Phys. Rev. A __65__, 042323 (2002), arXiv:quant-ph/0108146.
11. I. Buluta and F. Nori, _Quantum Simulators_, Science __326__, 108-111 (2009).
12. U. Las Heras _et al._, _Digital Quantum Simulation of Spin Systems in Superconducting Circuits_ Phys. Rev. Lett. __112__, 200501 (2014).
13. Y. Salathé _et al._, _Digital Quantum Simulation of Spin Models with Circuit Quantum Electrodynamics_, Phys. Rev. X __5__, 021027 (2015).
14. R. Barends _et al._, _Digital quantum simulation of fermionic models with a superconducting circuit_, Nature Communications __6__, 7654 (2015).
15. A. Chiesa _et al._, _Quantum hardware simulating four-dimensional inelastic neutron scattering_, arXiv:1809.07974 (2018).

## Support

For suggestions, errors/bug reporting or any other reasonable request, feel free to open an issue on the GitHub project page. If you use these materials 
for educational purposes, we would appreciate if you could acknowledge it during your classes or on the course website and provide us with your feedback.

## Disclaimer

The views expressed in these notebooks are those of the authors and do not reflect the official policy or position of IBM or the IBM Q team.
