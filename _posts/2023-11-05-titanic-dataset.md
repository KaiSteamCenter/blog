# Exploring the Titanic Dataset


## **Introdcution**

The Titanic is one of the most recognizable tragedies to ever happen. On its voyage, the RMS Titanic, a British passenger ship, struck an iceberg, resulting in a terrible tragedy that has been talked about ever since. There was a great deal of loss in the tragic event and it left an indelible mark on history. In this blog, we will delve into the Titanic dataset to uncover insights and answer  questions about the passengers on board this voyage.


## **The Data**

``This is a example of the type of data I had worked with throughout this whole project:``


| PassengerId | Survived | Pclass | Name | Sex | Age | SibSp | Parch | Ticket | Fare | Cabin | Embarked 
|------------|----------|--------|------|-----|-----|-------|-------|--------|------|-------|----------|
| 4 | 1 | 1 | Futrelle, Mrs. Jacques Heath (Lily May Peel) | female | 35  | 1 | 0 | 113803 | 53.1 | C123| S |

## **Question 1: What is the percentage of people who had survived?**

To answer our first question, we want to find out the percentage of passengers who survived the disaster. We will visualize this data to make it more understandable.

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("titanic.csv")

died = df[df['Survived'] == 0]
survived = df[df['Survived'] == 1]

died_count = died.shape[0]
survived_count = survived.shape[0]
labels = ['Died', 'Survived']
sizes = [died_count, survived_count]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title('Distribution of Passengers')
plt.show()
```
![Pie Chart](assets\download.png)
This graph is a pie chart that visually represents the distribution of passengers who survived and those who did not. It provides a clear visualization of the proportion of survivors and non-survivors among the Titanic passengers.


