# PySpark Word Count Using RDD

## Overview

This project demonstrates the implementation of a Word Count program using **Apache PySpark** in **Google Colab**. The program processes the text of the book *War and Peace* and calculates the frequency of each word using Resilient Distributed Datasets (RDDs).

## Technologies Used

- Python
- Apache PySpark
- Google Colab
- RDD (Resilient Distributed Dataset)

## Dataset

- **Input File:** `book-war-and-peace.txt`
- **Source:** Text of the book *War and Peace*
- **Format:** Plain text file (`.txt`)

## Implementation Steps

The program is implemented using the following steps:

1. **Install PySpark:** Install the PySpark library in Google Colab.
2. **Create SparkContext:** Initialize SparkContext using `getOrCreate()`.
3. **Upload Input File:** Upload the text file using Google Colab's file upload functionality.
4. **Create RDD:** Read the text file using `textFile()` and create an RDD.
5. **Remove Empty Lines:** Use `filter()` to remove empty lines.
6. **Split Words:** Use `flatMap()` to split each line into individual words.
7. **Convert to Uppercase:** Use `map()` to convert words into uppercase.
8. **Create Word-Count Pairs:** Assign a count of 1 to each word, creating key-value pairs.
9. **Calculate Word Frequency:** Use `reduceByKey()` to calculate the total occurrence of each word.

## PySpark Operations Used

| Operation | Description |
|---|---|
| `textFile()` | Reads the input text file and creates an RDD. |
| `filter()` | Removes empty lines. |
| `flatMap()` | Splits lines into individual words. |
| `map()` | Converts words into uppercase and creates word-count pairs. |
| `reduceByKey()` | Combines counts of identical words. |
| `take()` | Retrieves the first five word-count pairs. |
| `count()` | Returns the total number of lines in the RDD. |

## Execution

The notebook is implemented and executed in Google Colab using PySpark. The final output displays the words along with their corresponding frequencies.

## How to Run

1. Open the notebook using Google Colab.
2. Run the cells sequentially.
3. Upload the `book-war-and-peace.txt` input file when prompted.
4. Execute the remaining cells to generate the word-count results.

## Learning Outcomes

- Understanding the fundamentals of Apache Spark.
- Learning how to create and work with RDDs.
- Understanding RDD transformations and actions.
- Applying `filter()`, `flatMap()`, `map()`, and `reduceByKey()` for text processing.
- Implementing a basic Word Count program using PySpark.
