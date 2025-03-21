# HW 3: Prompting and Imitative Falsehoods
**Due:** March 31, 5:00 PM

For this assignment, please complete the _problem set_ found in `hw3-pset.ipynb`. The problem set includes coding
problems as well as written problems.

For the coding problems, you will implement functions defined in the Python file `truthfulqa.py`, replacing the existing code (which raises a `NotImplementedError`) with your own code. **Please write all code within the relevant files and function definitions**; failure to do this may break the rest of your code.

For some of the coding problems, you will be asked to run your code (preferably on HPC). This will cause a language model from 🤗 Transformers to be evaluated on the [TruthfulQA benchmark](https://huggingface.co/datasets/EleutherAI/truthful_qa_mc) ([Lin et al., 2021](https://arxiv.org/abs/2109.07958)). When the evaluation is complete, the results will be saved as a `.csv` file in the `results` folder. Please submit the `.csv` results files for all evaluations you are asked to perform in this assignment.

For the written problems, please submit your answers in PDF format, using the filename `hw3-written.pdf`. Make sure to clearly mark each problem in order to minimize the chances of grading errors.

You do not need to submit anything for Problems 1d, 2a, or 2b.

You are free to use any resources to help you with this assignment, including books, websites, and AI assistants such as ChatGPT. You are also free to collaborate with any other student or students in this class. However, you must write and submit your own answers to the problems, and merely copying another student's answer will be considered cheating on the part of both students. If you choose to collaborate, please list your collaborators at the top of your `hw3-written.pdf` file. If you choose to use ChatGPT or a similar AI assistant to help you with this assignment in any way, please include a file called `hw3-chatgpt-logs.txt` with a full transcript of all prompts and responses used for this assignment. Your use of AI assistants cannot involve generating images or any other content that cannot be included in a `.txt` file.

## Setup

You will need to complete your code problems in Python 3, preferably Python 3.8 or later. Apart from the standard Python libraries, you will need the following dependencies:

* [NumPy](https://numpy.org)
* [tqdm](https://tqdm.github.io/)
* [PyTorch](https://pytorch.org/)
* [🤗 Datasets](https://huggingface.co/docs/datasets/index)
* [🤗 Transformers](https://huggingface.co/docs/transformers/index)
* [🤗 Evaluate](https://huggingface.co/docs/evaluate/index)

Please refer to their websites for installation instructions.

These dependencies will need to be installed on HPC, in addition to your personal computer. You should have Miniconda installed inside a Singularity overlay, and after activating your Singularity container, you should use Miniconda to install the dependencies above. Please consult the Week 5 lab materials for guidance on how to do this.

## Submission

For your submission, please upload the following files to [Gradescope](https://www.gradescope.com):

* `truthfulqa.py`
* `.csv` files generated by the `truthfulqa.py` script during Problems 3a and 3b (8 in total)
* `extra_credit.csv` (if Problem 3c is attempted)
* `hw3-written.pdf`
* `hw3-chatgpt-logs.txt` (if ChatGPT or another AI assistant is used).

The `.csv` files are not provided in this repository; they will be generated by your code when you run it. Please use the exact file names described above, and do not upload any other files to Gradescope. Please do not upload the `results` folder or otherwise include any form of directory structure in your submission. Failure to follow the
submission instructions may result in a penalty of up to 5 points.

## Grading

The point values for each problem are given below. Problem 3c is worth 10 extra credit points, and the maximum possible grade on this assignment is 110 points. 

| Problem | Problem Type | Points |
|---|---|---|
| 1a: Understand the Experimental Setup | Written | 10 |
| 1b: Understand the Evaluation Paradigms | Written | 10 |
| 1c: Understand the Multiple Choice Paradigms | Written | 10 |
| 2c: Implement the MC1 Paradigm | Code | 10 |
| 2d: Implement Pipeline Methods | Code | 30 |
| 3a: Scaling Laws | Code and Written | 15 |
| 3b: Prompt Engineering | Code and Written | 15 |
| 3c: Extra Credit | Code and Written | 10 EC |
| **Total** | | **100** |

### Rubric for Code Problems

Code questions will be graded using a series of [Python unit tests](https://realpython.com/python-testing/). Each
function you implement will be tested on a number of randomly generated inputs, which will match the specifications
described in the function docstrings. **You will be able to see the results of the unit tests on
[Gradescope](https://www.gradescope.com) as soon as the unit tests are released.** Therefore, you are encouraged to debug and resubmit your code if one or more unit tests fail.

For code problems, you will receive:

* full points if your code runs and passes all test cases
* at least 5 points if your code runs but fails at least one test case
* 0 points if your code does not run.

Partial credit may be awarded at the graders' discretion, depending on the correctness of your logic and the severity of
bugs or other mistakes in your code. All code problems will be graded **as if all other code problems had been answered
correctly**. Therefore, an incorrect implementation of one function should (in theory) not affect your grade on other
problems that depend on that function.

### Rubric for Written Problems

For written problems, you will receive:

* full points for Problems 1a, 1b, and 1c if all questions are answered correctly
* full points for Problem 3a and 3b if results are reported accurately and are accompanied by at least 1 to 2 sentences of thoughtful analysis
* at least 2 points if a good-faith effort (according to the graders' judgement) has been made to answer the question
* 0 points if your answer is blank.

Partial credit may be awarded at the graders' discretion.
