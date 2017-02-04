This program was written by Jonathon Galsurkar and Meredith Lancaster under the supervision of Prof. William Sakas
at Hunter College, Computer Science and the Graduate Center, Linguistics and Computer Science of the City University
of New York. It is written in Python 3.5.1.

sakas@hunter.cuny.edu

The program implements a learner that learns multiple abstract, human-like languages grounded in Chomsky's principles
and parameters framework. The learning model is one of first language acquisition, i.e., acquisition by a child of approximately
2 years of age.

The learner and the abstract domain over which it operates is described in detail in:

Sakas, W.G. & Fodor, J.D. (2012) Disambiguating Syntactic Triggers, Language Acquisition (19) pp 83-143.

The paper and domain and other relevant information are downloadable here:

http://www.colag.cs.hunter.cuny.edu/downloadables.html

-----

8/9/2016: The program is currently being maintained by Meredith Lancaster

Meredith.Lancaster88@myhunter.cuny.edu

The most recent data generated by the program are currently available in the results folder.

###Running the program
The program must be run with a Python interpreter that supports Python 3.5. It can run with
`python main.py <number of learners> <number of sentences to be processed> <language code> [-c, --convergence] [-p, --plots]`

###Language Code
The file EngFrJapGerm.txt contains 3522 sentences, corresponding to fake languages which represent (and mimic the grammatical structure of) either English, French, Japanese, or German. Each language has a code associated with it, allowing the user to specify which language the learners should be trained on.

###Optional Arguments
There are two optional arguments represented by the -c/--c and -p/--plot flags. Using these flags will cause the program to produce additional results

####Plot Flag
The flag will cause the program to produce two plots, one recording the psets of each parameter (the order in which each converged) and the other showing at what time (represented in sentences) the parameters converged.

####Convergence Flag
This flag will cause the program to find convergence patterns between parameters. For example, it will record the number of times parameter 4 converged before parameter 1.

French=584, English=611, German=2253, and Japanese=3856

###Output
The program will write simulation results to several csv and png files to a folder whose name starts with the used language followed by the number of learners, and a timestamp. For example:
English_100_32016-06-09T14.17.54.747187 will contain the results of simulation using 100 learners with English.

###Port
I wrote a port of this program in Clojure as introduction to functional programming and concurrency, which can be found [here](https://github.com/malancas/Language-Acquisition)
