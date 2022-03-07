# Movies-ETL

## Purpose
The purpose of our analysis was to determine whether or not there was positivity bias in relation to 5 star ratings between paid vine reviews and non paid vine reviews. To do so we created a set of paid for vine reviews and non paid for vine reviews, then took the 5 star average of each one respectively the resulting percentages reflected below

### This new assignment consists of two technical analysis deliverables and a written report.

* Deliverable 1: Perform ETL on Amazon Product Reviews
* Deliverable 2: Determine Bias of Vine Reviews
* Deliverable 3: A Written Report on the Analysis README.md

## Deliverable 1 Requirements:
* An ETL function is written to read in the three data files

* The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

* The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

* The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

<img width="523" alt="image" src="https://user-images.githubusercontent.com/87340105/156967382-74f530a3-62e0-4cda-9a10-e72a7cc96a04.png">

<img width="509" alt="image" src="https://user-images.githubusercontent.com/87340105/156967336-be69413f-d07e-4cad-a585-bc46d0337053.png">

<img width="799" alt="image" src="https://user-images.githubusercontent.com/87340105/156967789-680cbf7c-1568-4822-b5cb-9a6074c4f3cf.png">

<img width="818" alt="image" src="https://user-images.githubusercontent.com/87340105/156967804-97eafde6-094f-4e57-b166-bb5566940d63.png">

<img width="250" alt="image" src="https://user-images.githubusercontent.com/87340105/156967830-d8b78fbe-a1ea-4598-ba84-a0f4c06dbdec.png">


## Deliverable 2 Requirements:
* The TV shows are filtered out, and the wiki_movies_df DataFrame is created.

<img width="473" alt="image" src="https://user-images.githubusercontent.com/87340105/156968101-22dcc92f-bca3-4e1b-842a-59ea638e8b9d.png">

* A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.

<img width="658" alt="image" src="https://user-images.githubusercontent.com/87340105/156968205-5516be2f-6149-452e-9af3-728567264759.png">

* The extraction and transformation of the Wikipedia data in the ETL function does the following:
  * A list comprehension is used to keep columns with non-null values.

<img width="644" alt="image" src="https://user-images.githubusercontent.com/87340105/156968558-a1d18fb7-19af-43f3-8f69-377dccd9a462.png">

  * The non-null box office data is converted to string values using the lambda and join functions.

<img width="592" alt="image" src="https://user-images.githubusercontent.com/87340105/156968600-dac0e50e-e2a7-47b9-8892-a03b4d9f36aa.png">

  * A regular expression is used to match the six elements of "form_one" of the box office data.

<img width="545" alt="image" src="https://user-images.githubusercontent.com/87340105/156968627-97e05f47-cfa1-4ac0-b949-a2e3f341b4b2.png">

  * A regular expression is used to match the three elements of "form_two" of the box office data.

<img width="556" alt="image" src="https://user-images.githubusercontent.com/87340105/156968674-990f2459-7616-4389-913b-f400e814460c.png">

<img width="479" alt="image" src="https://user-images.githubusercontent.com/87340105/156968736-cf65d6bc-f0eb-48f1-9fc8-8dd298be3035.png">

  * The following columns are cleaned in the Wikipedia DataFrame:
    * The box office column 
    * The budget column

<img width="643" alt="image" src="https://user-images.githubusercontent.com/87340105/156969161-23893666-655f-4aba-bcc3-c209ce185fa3.png">

    * The release date column
    * The running time column
    
<img width="682" alt="image" src="https://user-images.githubusercontent.com/87340105/156969212-39501dea-224c-40ca-b64f-0f15b876a6e5.png">

 * The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file.

<img width="742" alt="image" src="https://user-images.githubusercontent.com/87340105/156969352-6b51bc24-1bbf-431e-bf66-c0e8e3c38f3d.png">


