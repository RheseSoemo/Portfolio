From May 2021 to January 2022, I worked as a developer on a project in Grand Canyon University's Research and Development Program under one of my professors, [Dr. Isaac Artzi](https://www.linkedin.com/in/isacartzi/). 

This project was based off of a publication by Dr. Artzi on the possibility of AI's usage within the medical field. Since AI's basic premise is designed on reading massive quantities of data and detecting patterns, it could be useful in helping speed up medical expert's diagnosis time for patients.

Our test implementations of this idea were based on a few different Python libraries and frameworks, including Jupyter Notebooks and SpaCY.io.


```python
# gets the master list of Diagnosis
with open('Master_Diagnosis_List.txt') as my_file:
    master_diagnosis_list = my_file.readlines()


def get_diagnoses(diagnosis_array):
    """
    :param diagnosis_array: diagnosis string array
    :return: diagnosis list array
    """
    run_tests(diagnosis_array)
    return current_diagnosis_list
```
<p align="center">
  <i>Our main test implementation gave possible diagnoses based off of information it was provided</i>
</p>
